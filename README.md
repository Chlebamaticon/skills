# Skills

Agent skills for shipping a Plan as numbered Waves of pull requests, then running an evidence-backed validation cycle on each PR. Compatible with the [skills](https://www.npmjs.com/package/skills) CLI (`npx skills`).

[![skills.sh](https://skills.sh/b/jakubchlebowicz/skills)](https://skills.sh/jakubchlebowicz/skills)

## Install

After this repository is on GitHub:

```bash
npx skills add jakubchlebowicz/skills
```

Install every skill in this repo:

```bash
npx skills add jakubchlebowicz/skills --skill '*'
```

Install only the coordinator:

```bash
npx skills add jakubchlebowicz/skills --skill validate
```

From a local clone:

```bash
npx skills add /Users/jakubchlebowicz/Workspace/GitHub/skills
```

## Skills

| Skill | Role |
| --- | --- |
| `wave` | Cut a Plan into numbered Waves of parallel PRs; validate each PR; advance on merge |
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
