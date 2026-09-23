# GitHub report templates

Fill placeholders from `synthesis.json` and `context.json`. Do not include dismissed findings. Post the summary with `gh pr comment <number> --body-file ...`. Post inline comments with `gh api repos/{owner}/{repo}/pulls/{pr}/comments`.

## Doom status-bar face prefix

Every posted comment (PR summary and each inline review comment) must start with one 48×48 Doom [status bar face](https://doom.fandom.com/wiki/Status_bar_face) image chosen from the **majority severity** among final findings in `synthesis.json` (exclude the change-summary object; ignore dismissed findings — they are already absent).

### Majority selection

Count final findings by severity (`blocking`, `important`, `minor`):

| Condition | Face asset | Alt text |
| --- | --- | --- |
| No final findings | `doom-face-god.png` | Doom status face: god |
| Majority `minor` | `doom-face-hurt-light.png` | Doom status face: hurt light |
| Majority `important` | `doom-face-hurt-heavy.png` | Doom status face: hurt heavy |
| Majority `blocking` | `doom-face-dead.png` | Doom status face: dead |

**Ties:** when two or more severities share the highest count, pick the worse severity (`blocking` > `important` > `minor`). Example: 2 blocking + 2 important → `blocking` → dead face.

Use the **same** face URL for the summary and every inline comment in that run.

### Image markup

Assets live under [`assets/`](assets/) in this skill. Published raw URLs (default branch `master`):

```
https://raw.githubusercontent.com/Chlebamaticon/skills/master/skills/validate-github-reporter/assets/{filename}
```

Prefix **exactly** this HTML line (forces 48×48 display), then a blank line, then the rest of the comment body:

```html
<img src="{face_url}" width="48" height="48" alt="{face_alt}">
```

Do not use Markdown image syntax for the face (GitHub may ignore size). Do not use faces larger than 48×48.

## PR summary comment

Head the comment with the Doom face prefix, then `## Validation`. Group final findings by severity in this order: `blocking`, `important`, `minor`. When there are no final findings, keep the change summary and write `No findings.` under **Findings**.

```markdown
<img src="{face_url}" width="48" height="48" alt="{face_alt}">

## Validation

**PR:** #{pr_number}
**Head:** `{head_sha}`

### Change summary

{change_summary}

### Findings

#### Blocking ({blocking_count})

<!-- Repeat this block for each blocking finding. Omit the entire section when blocking_count is 0. -->

**{id}** — {title}

{body}

- **Source:** {source}
- **Confidence:** {confidence}
- **Location:** `{path}:{line}` <!-- omit this bullet when location is absent -->

#### Important ({important_count})

<!-- Same block shape as Blocking. Omit section when important_count is 0. -->

**{id}** — {title}

{body}

- **Source:** {source}
- **Confidence:** {confidence}
- **Location:** `{path}:{line}`

#### Minor ({minor_count})

<!-- Same block shape. Omit section when minor_count is 0. -->

**{id}** — {title}

{body}

- **Source:** {source}
- **Confidence:** {confidence}
- **Location:** `{path}:{line}`

<!-- When every severity count is 0: -->

No findings.
```

### Summary example (with findings)

Majority here is `blocking` (1) vs `important` (1) → tie → worse → dead face.

```markdown
<img src="https://raw.githubusercontent.com/Chlebamaticon/skills/master/skills/validate-github-reporter/assets/doom-face-dead.png" width="48" height="48" alt="Doom status face: dead">

## Validation

**PR:** #42
**Head:** `a1b2c3d4e5f6789012345678901234567890abcd`

### Change summary

Adds JWT refresh handling and tightens cookie flags on the auth middleware.

### Findings

#### Blocking (1)

**sec-001** — Set HttpOnly on refresh token cookie

The refresh token is written without `HttpOnly`, so any XSS can read it and mint sessions.

- **Source:** security
- **Confidence:** high
- **Location:** `src/auth/cookies.ts:38`

#### Important (1)

**code-002** — Reuse shared token parser in refresh path

The refresh handler duplicates parsing logic from `parseAccessToken`, so expiry checks can drift.

- **Source:** code
- **Confidence:** medium
- **Location:** `src/auth/refresh.ts:19`

#### Minor (0)

<!-- omit this section when count is 0 -->
```

### Summary example (no findings)

```markdown
<img src="https://raw.githubusercontent.com/Chlebamaticon/skills/master/skills/validate-github-reporter/assets/doom-face-god.png" width="48" height="48" alt="Doom status face: god">

## Validation

**PR:** #42
**Head:** `a1b2c3d4e5f6789012345678901234567890abcd`

### Change summary

Docs-only update to the deployment runbook.

### Findings

No findings.
```

## Inline review comment

Post only for `blocking` or `important` findings that have a `location` present in the PR diff. Body must start with the Doom face prefix (same face as the summary for this run), then `[validation:{id}]` on its own line.

```markdown
<img src="{face_url}" width="48" height="48" alt="{face_alt}">

[validation:{id}]

**{title}**

{body}
```

Keep the body short: evidence, impact, and one concrete fix. Do not repeat metadata already in the PR summary.

### Inline example

```markdown
<img src="https://raw.githubusercontent.com/Chlebamaticon/skills/master/skills/validate-github-reporter/assets/doom-face-dead.png" width="48" height="48" alt="Doom status face: dead">

[validation:sec-001]

**Set HttpOnly on refresh token cookie**

`res.cookie('refresh', token, { secure: true })` exposes the token to `document.cookie`. Add `httpOnly: true` (and keep `secure` + `sameSite`) so XSS cannot exfiltrate refresh tokens.
```

## Unpublished inline comment reasons

Record these in `github-report.json` → `unpublished` when an inline comment cannot be posted:

| Reason | When to use |
| --- | --- |
| `not-in-diff` | Path or line is outside the PR changed-file diff |
| `github-rejected` | GitHub API rejected the location (do not guess a nearby line) |
| `no-location` | Finding has no `location` (summary only) |
| `severity-minor` | Finding severity is `minor` (summary only) |

## `github-report.json` shape

```json
{
  "summary_url": "https://github.com/{owner}/{repo}/pull/{pr}#issuecomment-{id}",
  "face": "dead",
  "inline_comments": [
    { "id": "sec-001", "url": "https://github.com/{owner}/{repo}/pull/{pr}#discussion_r{id}" }
  ],
  "unpublished": [
    { "id": "code-003", "reason": "not-in-diff" }
  ]
}
```

`face` is one of `god`, `hurt-light`, `hurt-heavy`, `dead` — the majority-selected face for the run.
