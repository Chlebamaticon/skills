---
name: validate-github-reporter
description: Publish a synthesized validation report as a Pull Request summary and inline GitHub comments on eligible changed code. Use during a validation cycle after synthesis completes.
---

# Validate GitHub reporter

Read [the shared validation contract](../validate/validation-contract.md). The caller supplies `RUN_DIR` containing `context.json` and `synthesis.json`.

## Publish the summary

Parse `synthesis.json`; reject malformed data or a missing change summary. Using the PR in `context.json`, post one Markdown PR comment headed `## Validation`. Include the change summary, final findings grouped by severity, each finding ID/title/body/location, and an explicit `No findings` when applicable. Use `gh pr comment <number> --body-file ...` and capture the resulting comment URL. Resolve `owner/repo` once with `gh repo view --json nameWithOwner --jq .nameWithOwner`.

## Publish eligible inline comments

For each final `blocking` or `important` finding with a location, verify that exact path and line are in the PR's changed-file diff. Post one inline comment using `gh api repos/{owner}/{repo}/pulls/{pr}/comments` with the pinned `head_sha`, `path`, `line`, and `side: RIGHT`. The body starts with `[validation:<id>]` and contains the finding title and concrete fix. If GitHub rejects the location, retain the summary-only report and record the rejection; never guess a nearby line.

Write `github-report.json` atomically with `summary_url`, `inline_comments` (`id`, `url`), and `unpublished` (`id`, `reason`).

**Done when:** one summary comment URL is recorded, every eligible finding has either an inline-comment URL or a recorded GitHub rejection, and `github-report.json` is valid JSON.
