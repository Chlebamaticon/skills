---
name: wave
description: >-
  Wave a Plan into numbered parallel PRs, write each task under .waves/, and
  ask for worker models before launch. Use when the user asks to proceed
  with a Plan.
---

# Wave

Cut the Plan into numbered **Waves**. A Wave is one moment: every task in it is merge-independent and can run in parallel. Tasks inside a Wave are letters (`1A`, `1B`). Each task ships as its own pull request. Start the next Wave only after every PR in the current Wave is merged and none of the halt labels below are present.

Dependencies belong in a later Wave. If `B` needs `A` merged first, `A` and `B` are different Waves.

Every run **must** break the Plan into tasks and write each task to a markdown file before launching workers. Do not keep the breakup only in chat. Prefer tasks small enough for **Composer 2.5**. Before any worker starts, ask which models to use (step 3).

## Halt, checker, merge

Treat these three as the only gate:

| Signal | What it is | What to do |
| --- | --- | --- |
| Halt labels | `needs-human`, `needs-decision`, `blocked` on a Wave PR | Stop. Report the PR URLs and labels. Wait for the user. |
| Checker | A GitHub check run failed, or a bot requested changes | Keep working that task: fix, push, re-run **validate**. |
| Merge | Every PR in this Wave is merged, and no halt label is present | Start the next Wave. |

Follow **validate** on each open Wave PR (give it the PR number or URL). After a checker fix, validate that PR again.

**Done when (gate):** halt labels are acted on as a stop, checker failures are still in iteration, and the next Wave starts only on the merge row.

## 1. Cut the Plan

Read the Plan in this conversation. Assign every Plan item to exactly one task id `{wave}{letter}` (Wave `1`, `2`, …; letters `A`, `B`, …). Put two items in the same Wave only when they can merge in any order onto the same base.

Mark each task **Kind** as `implementation` or `research`. Split work so most tasks are `implementation` and small enough for Composer 2.5. Use `research` only when the work is investigation, docs, or API facts with little or no product-code ship.

Derive `<topic>` as a kebab-case slug from the Plan title. If the Plan has no title, ask the user for a short topic slug before writing files.

Show the board, then write the task files (step 2), then ask models (step 3), then run Wave `1`:

```text
Wave 1
  1A  implementation  <title>  — <one-line scope>
  1B  research        <title>
Wave 2
  2A  implementation  <title>
```

**Done when:** every Plan item appears exactly once, same-Wave tasks have no merge-order dependency, each row has a Kind, and the board is visible to the user.

## 2. Write task files

On every run (including when advancing to a later Wave), write or overwrite one markdown file per task. Paths are relative to the repo root:

```text
.waves/<topic>-<wave-no>/<kebab-title>-<task-no>.md
```

Default root is `.waves/` at the repo root. Do not write under `waves/` unless the user names a different root.

- `<topic>` — kebab-case Plan title
- `<wave-no>` — Wave number (`1`, `2`, …)
- `<kebab-title>` — kebab-case of that task's title
- `<task-no>` — full board id (`1A`, `1B`, `2A`, …)

Example: `.waves/checkout-redesign-1/add-login-1A.md`

Each file is the **full task brief**. Use this shape:

```markdown
# <task-no> <title>

- Task id: <task-no>
- Wave: <wave-no>
- Topic: <topic>
- Kind: implementation | research
- Model: <set in step 3; leave blank until then>
- Base: <branch or SHA>

## Scope

<only this task's Plan scope>

## Ship

- Implement, commit, push, and open one PR
- Stop after the PR URL exists
- Do not implement sibling tasks or later Waves
```

Write **every** Wave's files when cutting the Plan. When a Wave starts, rewrite that Wave's files if the board or base SHA changed.

**Done when:** every board row has a file at that path, and the files match the current board.

## 3. Ask models

Before launching any worker in this Wave, ask with `pi__cursor_ask_question` (or the host AskQuestion tool). Do not assume models. Ask **once per Wave**, then write the answers into that Wave's task files.

1. **Implementation tasks** (default): confirm Composer 2.5 for every `implementation` task in this Wave. Prefer that default; the user may override.
2. **Research tasks** (only if this Wave has any `research` Kind): ask which model to use — **GPT Luna**, **Terra**, or **Sol**. Allow a custom answer.

Record the chosen display name on the `Model:` line of each task file in this Wave.

Map the display name to a `model` slug from this run's Task allow-list. Composer 2.5 is `composer-2.5-fast` when that slug is listed. For GPT Luna, Terra, and Sol, use the listed slug whose name matches; do not invent a slug.

If the chosen name has no matching slug in this run's Task allow-list, do **not** substitute another model. Skip that worker, tell the user which models are available, and wait. Workers do not pick models — the parent sets `model` on the Task call.

**Done when:** every task file in this Wave has a `Model:` value, and research tasks were asked about when present.

## 4. Run the current Wave

Base every task on the default branch as it is *after* prior Waves merged. Put that base into each task file before launching workers.

Launch **one Cursor Task per task**, all in **one message**, `subagent_type: best-of-n-runner` (isolated worktree and branch). Pass `model` using the slug recorded for that task. If that type is not exposed, create one `git worktree` and branch per task yourself and still keep one PR per task.

Each worker prompt includes:

- The **absolute path** of that task's markdown file
- Instruction to read that file and follow only its brief
- Instruction not to open sibling task files or later Wave directories
- Instruction to implement, commit, push, and open one PR
- Instruction to stop after the PR URL exists

Do not paste sibling scopes or later Waves into the prompt. The task file is the source of scope. Subagents have no parent history — the path and those instructions must be in the prompt.

**Done when:** every task in this Wave has a worker (or worktree) and none of the next Wave's work has started.

## 5. Collect PRs

Take each task's PR URL. If a worker returned without a PR, finish that task's PR before touching the gate.

**Done when:** every task id in this Wave maps to an open PR URL.

## 6. Validate and iterate

For each Wave PR, follow **validate**. Then read checks and labels:

- Halt label present → apply the halt row of the gate (end the turn).
- Checker present → keep working that PR; validate again after the push.
- Checks green and no halt label → leave the PR for merge; do not start the next Wave yet.

**Done when:** every Wave PR is either halted (user notified) or still iterating on a checker, or waiting for merge with validate already run and checks green.

## 7. Advance

When every PR in this Wave is merged and no halt label is present, repeat from step 2 with the next Wave (rewrite files, ask models again, then run). After the last Wave merges, show the board with every task id and its merged PR URL.

**Done when:** every board row has a merged PR URL, or the run is stopped on a halt label.
