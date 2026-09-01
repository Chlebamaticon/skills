# Entry format

Every **entry** in the **memory-bank** uses this shape. Read [`GLOSSARY.md`](GLOSSARY.md) for term meanings.

```markdown
# <Short title>

## Correlated decisions

- [../decisions/<slug>.md](../decisions/<slug>.md) — <one-line why linked>
- _none_

## Derived from

- `<repo-relative-path>` — <what it evidenced>
- _none_

## Body

<Brief, precise outcome. Prefer decisions and constraints over narrative.
One idea per entry. Link out instead of pasting large excerpts.>

## Changelog

| Date | Change | Why |
| --- | --- | --- |
| YYYY-MM-DD | Created | <why this entry exists> |
```

## Rules

- Title is the meaning in a few words — same idea as the kebab-case filename.
- **Correlated decisions** and **Derived from** are always present; use `_none_` rather than omitting the section.
- **Changelog** is always last; append a row on every edit (`Updated | <why>`).
- Keep the body short enough that **recall** can load several entries without drowning the task.
