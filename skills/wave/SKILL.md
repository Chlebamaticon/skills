---
name: wave
description: >-
  Wave a Plan into numbered parallel PRs. Use when the user asks to proceed
  with a Plan.
---

# Wave

Cut the Plan into numbered **Waves**. A Wave is one moment: every task in it is merge-independent and can run in parallel. Tasks inside a Wave are letters (`1A`, `1B`). Each task ships as its own pull request. Start the next Wave only after every PR in the current Wave is merged and none of the halt labels below are present.

Dependencies belong in a later Wave. If `B` needs `A` merged first, `A` and `B` are different Waves.

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

Show the board, then run Wave `1`:

```text
Wave 1
  1A  <title>  — <one-line scope>
  1B  <title>
Wave 2
  2A  <title>
```

**Done when:** every Plan item appears exactly once, same-Wave tasks have no merge-order dependency, and the board is visible to the user.

## 2. Run the current Wave

Base every task on the default branch as it is *after* prior Waves merged.

Launch **one Cursor Task per task**, all in **one message**, `subagent_type: best-of-n-runner` (isolated worktree and branch). If that type is not exposed, create one `git worktree` and branch per task yourself and still keep one PR per task.

Each worker prompt includes all of:

- Task id and title (`1A`, …)
- Only that task's Plan scope (no sibling tasks, no later Waves)
- Base branch / SHA to branch from
- Instruction to implement, commit, push, and open one PR
- Instruction to stop after the PR URL exists

Subagents have no parent history — put all of that in the prompt.

**Done when:** every task in this Wave has a worker (or worktree) and none of the next Wave's work has started.

## 3. Collect PRs

Take each task's PR URL. If a worker returned without a PR, finish that task's PR before touching the gate.

**Done when:** every task id in this Wave maps to an open PR URL.

## 4. Validate and iterate

For each Wave PR, follow **validate**. Then read checks and labels:

- Halt label present → apply the halt row of the gate (end the turn).
- Checker present → keep working that PR; validate again after the push.
- Checks green and no halt label → leave the PR for merge; do not start the next Wave yet.

**Done when:** every Wave PR is either halted (user notified) or still iterating on a checker, or waiting for merge with validate already run and checks green.

## 5. Advance

When every PR in this Wave is merged and no halt label is present, repeat from step 2 with the next Wave. After the last Wave merges, show the board with every task id and its merged PR URL.

**Done when:** every board row has a merged PR URL, or the run is stopped on a halt label.
