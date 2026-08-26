# Validation artifact contract

A validation run is identified by `RUN_DIR`, created by the coordinator:

```bash
HEAD_SHA=$(git rev-parse HEAD)
RUN_DIR=$(git rev-parse --git-path "validate/$HEAD_SHA")
mkdir -p "$RUN_DIR"
```

Every artifact is JSON encoded as UTF-8, has a trailing newline, and is written atomically (`file.tmp`, then `mv`). Reviewers must use only changed lines in the three-dot PR diff. A location is `{ "path": "relative/path", "line": 42 }`; omit it when the concern has no changed-line anchor.

## Files

| Writer | File |
| --- | --- |
| coordinator | `context.json`, `changes.json` |
| code reviewer | `code-review.json` |
| security reviewer | `security-review.json` |
| code challenger | `challenge-code-review.json` |
| security challenger | `challenge-security-review.json` |
| synthesizer | `synthesis.json` |
| GitHub reporter | `github-report.json` |

Each reviewer or challenger reads only its own source artifacts. It must not read sibling worker outputs.

`context.json` contains `pr`, `base`, `head`, `head_sha`, `diff_command`, and `run_dir`. `changes.json` contains an array of `{path, status, additions, deletions}` plus a concise `summary` string.

A reviewer artifact is an array of findings. Each finding has:

```json
{
  "id": "code-001",
  "source": "code",
  "severity": "blocking|important|minor",
  "title": "short imperative or diagnosis",
  "body": "evidence, impact, and concrete fix",
  "location": { "path": "src/x.ts", "line": 42 },
  "evidence": "quoted code, rule, or trace",
  "confidence": "high|medium|low"
}
```

Use `[]` for no findings. A challenge artifact has one record per source finding: `{id, verdict: "upheld|dismissed|reframed", rationale, revised_finding?}`. It must not invent a new finding.

`synthesis.json` is a JSON array. Its first object is `{ "kind": "change-summary", "summary": "..." }`; its remaining objects are final findings using the reviewer schema plus `challenge_verdict`. It contains only upheld or reframed findings; reframed items use `revised_finding` as their final content. IDs stay stable.

The reporter only posts inline comments for `blocking` or `important` findings with a location that is present in the PR diff. It posts all final findings in the PR summary. It never reports dismissed findings.
