# Skills

Agent skills for shipping a Plan as numbered Waves of pull requests, then running an evidence-backed validation cycle on each PR. Compatible with the [skills](https://www.npmjs.com/package/skills) CLI (`npx skills`).

[![skills.sh](https://skills.sh/b/Chlebamaticon/skills)](https://skills.sh/Chlebamaticon/skills)

## Install

After this repository is on GitHub:

```bash
npx skills add Chlebamaticon/skills
```

Install every skill in this repo:

```bash
npx skills add Chlebamaticon/skills --skill '*'
```

Install only the coordinator:

```bash
npx skills add Chlebamaticon/skills --skill validate
```

From a local clone:

```bash
npx skills add /Users/jakubchlebowicz/Workspace/GitHub/skills
```

## Skills

| Skill | Role |
| --- | --- |
| `demoable-visually-testable-ui-components` | Frontend component design rules for deterministic demos, fixtures, and visual tests |
| `wave` | Cut a Plan into numbered Waves of parallel PRs; write each task under `.waves/<topic>-<wave-no>/`; ask for worker models before launch; validate each PR; advance on merge |
| `validate` | Coordinator: pin the PR, run reviews and challenges, synthesize, report |
| `validate-with-code-review` | Diff review against repo standards and simplification |
| `validate-with-security-review` | Diff review for trust-boundary and security defects |
| `validate-by-challenge` | Independent pressure-test of each review finding |
| `validate-synthentizer` | Canonical JSON report from challenged findings |
| `validate-github-reporter` | PR summary plus eligible inline comments |

Worker skills share `skills/validate/validation-contract.md`. The coordinator launches Cursor Task subagents; it reports and does not modify product code.

## Layout

The CLI discovers `SKILL.md` files one level under `skills/`:

```text
skills/
  validate/
    SKILL.md
    validation-contract.md
  validate-with-code-review/
    SKILL.md
  ...
```

## License

Use and redistribute these skills as you see fit for your own agent setup.
