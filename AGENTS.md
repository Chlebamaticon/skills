# AGENTS.md

Collection of agent skills for PR validation. Skills follow the [Agent Skills](https://agentskills.io/) format and are installable with `npx skills add`.

## Layout

```text
skills/
  {skill-name}/
    SKILL.md              # required
    *.md                  # optional references (one hop from SKILL.md)
```

Directory names are kebab-case and must match the `name` frontmatter field.

## Contract

`skills/validate/validation-contract.md` is the shared artifact schema. Worker skills (`validate-with-*`, `validate-by-challenge`, `validate-synthentizer`, `validate-github-reporter`) point at it with `../validate/validation-contract.md`. Keep those relative links valid when renaming or moving folders.

## Adding a skill

1. Create `skills/{name}/SKILL.md` with `name` and `description` frontmatter.
2. If it belongs in the Validation grouping, add the `name` to `skills.sh.json`.
3. Document it in `README.md`.
4. Verify discovery: `npx skills add . --list`
