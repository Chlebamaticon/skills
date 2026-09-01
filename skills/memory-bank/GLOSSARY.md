# Glossary — Memory-Bank

The domain model for the **memory-bank**: durable, brief, precise notes from agent sessions that later runs can **recall**. This is the disclosed reference for [`remember`](../remember/SKILL.md), [`recall`](../recall/SKILL.md), and [`memory-bank`](SKILL.md).

**Bold terms** in any definition are themselves defined here.

## Memory-Bank

The on-disk store of durable session outcomes — decisions, patterns, practices, domains, and sessions — under a **bank root**. Agents **remember** into it and **recall** from it. Predictability comes from the same layout and entry shape every run, not from identical prose.

_Avoid_: knowledge base, wiki, notes dump

## Bank Root

A directory that _is_ one memory-bank. Two roots exist; **repo-centric** is the default write target.

| Root | Path | Holds |
| --- | --- | --- |
| **Repo** | `<project>/.memory/` | Repository-centric outcomes (default) |
| **Global** | `$HOME/.memory/` | Cross-repo agreements that apply beside any repository |

Create category folders lazily on first write. Never invent a third root without updating this glossary.

_Avoid_: workspace memory, personal vault (unless you mean Global)

## Scope

Where an **entry** belongs.

- **Repo** — true for this codebase only, or unclear → write under the repo bank root.
- **Global** — explicitly agreed to apply across repositories → write under `$HOME/.memory/`.

**Recall** reads the repo bank first, then the global bank for applicable cross-cutting entries.

_Avoid_: local/remote, shared/private

## Category

A first-level folder under a **bank root**. The live set:

| Category | Folder | What crystallises here |
| --- | --- | --- |
| **Decision** | `decisions/` | A choice we will treat as binding until superseded |
| **Pattern** | `patterns/` | A recurring shape observed or adopted in code/process |
| **Practice** | `practices/` | How we work — habits, rituals, agent conventions |
| **Domain** | `domains/` | Stable domain facts or ubiquitous-language notes |
| **Session** | `sessions/` | One brief note for an agent session's durable outcomes |

Add a category only when an existing one cannot hold the meaning; then update this table in the same change.

_Avoid_: tag, label, type (prefer **category**)

## Entry

One markdown file in a **category** folder. Filename: kebab-case, brief topic (`wave-gates-on-validate.md`). Body follows [`ENTRY-FORMAT.md`](ENTRY-FORMAT.md): correlated **decisions**, **derived-from** paths, precise body, **changelog** at the bottom.

Update an existing entry when the same meaning changes; create a new file only for a new meaning. Append the **changelog**; do not rewrite history silently.

_Avoid_: note, card, memo

## Correlated Decisions

Header links from an **entry** to related **decision** entries (same or other **bank root**). Use relative paths within a bank; use absolute paths when pointing across repo ↔ global. Write `_none_` when there are no links.

_Avoid_: see also, related (as a vague dump)

## Derived-From

Header links to the example files, PRs, or paths the **entry** was derived from — evidence the next agent can reopen. Prefer repo-relative paths.

_Avoid_: sources, references (unstructured)

## Changelog

The bottom section of every **entry**: dated rows of what changed and why. Newest last. Required on create (first row) and on every update.

_Avoid_: history, revisions (as free prose only)

## Crystallise

The gate for **remember**: an outcome is durable enough to write — a decision made, a pattern named, a practice adopted, a domain fact pinned, or a session closed with outcomes worth keeping. Ephemeral chatter and unfinished brainstorms do not crystallise.

_Avoid_: save everything, log the transcript
