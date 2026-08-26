# GitHub report templates

Fill placeholders from `synthesis.json` and `context.json`. Do not include dismissed findings. Post the summary with `gh pr comment <number> --body-file ...`. Post inline comments with `gh api repos/{owner}/{repo}/pulls/{pr}/comments`.

## PR summary comment

Head the comment with `## Validation`. Group final findings by severity in this order: `blocking`, `important`, `minor`. When there are no final findings, keep the change summary and write `No findings.` under **Findings**.

```markdown
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

```markdown
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
## Validation

**PR:** #42
**Head:** `a1b2c3d4e5f6789012345678901234567890abcd`

### Change summary

Docs-only update to the deployment runbook.

### Findings

No findings.
```

## Inline review comment

Post only for `blocking` or `important` findings that have a `location` present in the PR diff. Body must start with `[validation:{id}]` on its own line.

```markdown
[validation:{id}]

**{title}**

{body}
```

Keep the body short: evidence, impact, and one concrete fix. Do not repeat metadata already in the PR summary.

### Inline example

```markdown
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
  "inline_comments": [
    { "id": "sec-001", "url": "https://github.com/{owner}/{repo}/pull/{pr}#discussion_r{id}" }
  ],
  "unpublished": [
    { "id": "code-003", "reason": "not-in-diff" }
  ]
}
```
