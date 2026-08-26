---
name: validate
description: Validate a current Pull Request through code standards, security, adversarial challenge, synthesis, and GitHub reporting. Launches review and challenge workers as parallel Cursor Task subagents. Use when the user asks for a full validation cycle or to validate a PR.
---

# Validate

Coordinate one evidence-backed validation run. This skill reports; it does not modify product code.

Read [the validation artifact contract](validation-contract.md) before starting.

## Subagent dispatch

Workers are Cursor Task subagents (`subagent_type: generalPurpose`). Do not load-and-follow a worker skill in this conversation. Do not use the built-in `security-review` or `bugbot` types — they do not write these artifacts.

A wave is every Task call in **one message**. Independent workers in a wave run in parallel.

If this session is in Cursor Multitask Mode, set `run_in_background: true` on every Task call and end the turn. Do not poll. Start the next wave only after completion notifications and after each owned artifact exists and parses.

If not in Multitask Mode, omit `run_in_background` so the wave blocks until every Task returns.

Each worker prompt includes: the absolute `RUN_DIR`, instruction to follow the named skill and this contract, isolation (do not read sibling artifacts), the owned output file, and that file's done-when criterion. Subagents have no parent history — put all of that in the prompt. Do not paste another worker's findings into a prompt.

## 1. Pin the pull request and run

Resolve the PR from a number/URL supplied by the user, otherwise `gh pr view --json number,url,baseRefName,headRefName,headRefOid`. Fetch the head and base refs, verify the three-dot diff is non-empty, and create `RUN_DIR` exactly as the contract specifies. Write atomic `context.json` and `changes.json`; include the changed-file list and a concise change summary derived from the diff.

**Done when:** the PR identity, immutable head SHA, base, diff command, and both coordinator artifacts exist.

## 2. Run independent reviews

One message, two Task calls:

- Code: follow **validate-with-code-review** → `code-review.json`. Do not read `security-review.json`.
- Security: follow **validate-with-security-review** → `security-review.json`. Do not read `code-review.json`.

**Done when:** `code-review.json` and `security-review.json` both exist and each is a valid JSON array.

## 3. Challenge each review

One message, two Task calls:

- Code: follow **validate-by-challenge** with `source: code` → `challenge-code-review.json`. Read only `code-review.json`.
- Security: follow **validate-by-challenge** with `source: security` → `challenge-security-review.json`. Read only `security-review.json`.

**Done when:** both challenge artifacts exist and every source finding has exactly one verdict.

## 4. Synthesize

One Task call: follow **validate-synthentizer**. It reads coordinator, reviewer, and challenge artifacts from `RUN_DIR` on disk.

**Done when:** `synthesis.json` exists, is a valid JSON array, and contains the change summary plus every upheld or reframed finding exactly once.

## 5. Report to GitHub

Load and follow **validate-github-reporter**, giving it `RUN_DIR`.

**Done when:** `github-report.json` records the URLs of the posted PR summary and every eligible inline comment.

## 6. Return the result

Tell the user the PR URL, run directory, final finding counts by severity, and the PR comment URL. Link or quote the final summary without reintroducing dismissed findings.

**Done when:** the user can open the GitHub report and inspect the synthesized JSON artifact.
