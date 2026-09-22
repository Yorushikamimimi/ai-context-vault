# Source-First Conversation Handoff

Use this template when work must continue in a new AI conversation or tool.

## Principle

Read the current source of truth first. An older conversation supplies only the material that has not yet been captured there. Do not migrate an entire transcript by default.

## Handoff record

- Task or project: `{{TASK_OR_PROJECT}}`
- Current source of truth: `{{EXACT_PATH}}`
- Current status document: `{{PROJECT_STATUS_PATH_OR_NOT_APPLICABLE}}`
- Last verified evidence: `{{EVIDENCE_OR_UNKNOWN}}`
- Scope and privacy boundary: `{{BOUNDARY}}`

## Confirmed unpersisted delta

- `{{CONFIRMED_DECISION_OR_ARTIFACT}}`

## Inferred or unverified items

- `{{INFERENCE_OR_UNKNOWN}}`

## Open question or blocker

- `{{BLOCKER_OR_NONE}}`

## Next entry point

- `{{SMALLEST_NEXT_READ_OR_ACTION}}`

## Migration procedure

1. Verify that the named current source and status document exist in the new workspace.
2. Read the minimum context route in `AI_CONTEXT.md`, then the listed source.
3. Use the unpersisted delta only to fill documented gaps; mark unsupported items as unverified.
4. If an authorized write is needed, read `SYNC_RULES.md` and update the existing owner first.
5. Do not create, rename, archive, commit, publish, or contact anyone merely because a handoff was prepared.
