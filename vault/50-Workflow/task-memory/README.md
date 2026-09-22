# Lightweight Task Memory

Use this directory only for a task that needs cross-session continuity and has no better current owner in a project or domain source of truth.

One task has one current file. Keep it brief, update it in place, and move important historical milestones to `../logs/` rather than building a chronological diary here.

## File template

```markdown
# {{TASK_NAME}}

Last verified: `{{YYYY-MM-DD_OR_UNKNOWN}}`
Status: `{{active|waiting|on_demand|blocked|completed|superseded|archive_candidate|archived}}`

## Long-lived context
- Why this task needs a separate memory file.

## Confirmed decisions
-

## Non-negotiable boundaries
- Scope, privacy, permission, and evidence limits.

## Current progress
- Keep at most five verified, concise items.

## Next actions
- Keep at most three actions with their trigger or smallest entry point.
```

Do not store credentials, raw transcripts, personal identifiers, sensitive third-party content, or a duplicate of an existing project status document.
