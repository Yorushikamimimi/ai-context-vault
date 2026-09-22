# Web Conversation Delta Template

Use this with a web AI tool that cannot access the local vault. Paste its output into a local review step; do not treat the output as an automatic write authorization.

```text
Create a concise, evidence-bound handoff delta from this conversation.

For each item, use one of: confirmed, inferred, unknown.

## Confirmed changes or decisions
-

## Artifacts and verification coverage
-

## Unresolved risks or unknowns
-

## Suggested destination
- Existing source of truth: {{PATH_OR_UNKNOWN}}
- Project status document: {{PATH_OR_NOT_APPLICABLE}}
- Task-memory file: {{PATH_OR_NOT_NEEDED}}
- Important weekly log: {{PATH_OR_NOT_NEEDED}}

## Next entry point
-

Rules:
- Do not invent file changes, successful tests, approvals, dates, people, or external outcomes.
- Do not include credentials, private identifiers, raw chat text, or confidential third-party information.
- Prefer an existing source of truth. Use task memory only when no current owner exists.
- Return only the delta required to resume, not a transcript or a general recap.
```
