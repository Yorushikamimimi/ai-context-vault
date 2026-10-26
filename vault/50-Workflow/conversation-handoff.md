# Source-First Conversation Handoff

Use this template when work must continue in a new AI conversation or tool.

## Principle

Read the current source of truth first. An older conversation supplies only the material that has not yet been captured there. Do not migrate an entire transcript by default.

If several AI tools share this vault as a steady state rather than moving work once, see `advanced/multi-tool-sharing.md`. The acceptance gates below still apply when a tool takes on a responsibility for the first time.

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

## Cross-tool acceptance procedure

This transfers current facts, decisions, constraints, and next entry points, not the entire chat history. Preparing these documents does not start a migration.

1. **Fix the scope.** Confirm the target tool, actual workspace path, responsibilities, user-selected model, and permitted material. Do not guess model names or assume a desktop app loads CLI instruction files.
2. **Persist and reconcile.** With existing write authority, each responsible agent updates its own current source. The coordinator verifies actual files and missing increments; a delivered notification is not a completed update.
3. **Freeze a baseline.** Record a cutoff, files or sections and their current writers, evidence, pending changes, and separately authorized commits. Inventory necessary local-only dependencies without reading unauthorized private files. A Git commit is not a complete backup.
4. **Check access and tools.** On the same machine and folder, verify access rather than copying the vault. For a different machine, agree an exact file allowlist and path mapping. External global rules, Skills, and integrations require their own source/version and capability checks; never copy credentials or browser sessions implicitly.
5. **Accept one coordinator first.** The user manually creates the target conversation. Begin read-only: report two relevant current facts with exact sources, distinguish a superseded state if one exists, and disclose a tool or permission limitation. Correct answers and self-reported reads are not proof that no out-of-scope access occurred. Keep that gap explicit if access traces are unavailable.
6. **Restore responsibilities individually.** After user acceptance, provide only the next requested responsibility's minimal prompt. The user creates it and accepts it separately. Do not automatically create all conversations, resume business, archive old ones, or assume coordinator acceptance covers every responsibility.

Keep gates distinct: documents reconciled; read-only recovery accepted; necessary tools checked; an explicitly authorized small write/readback verified; a real bounded task accepted; writer ownership transferred. A read-only test cannot pass a write gate. Use passed / unverified / deferred with reasons, not a single confidence score.

If validation fails, stop target writes, reconcile actual changes against the latest sources, and return to the recorded fallback. Do not reset, delete, restore backups, or overwrite new progress automatically. Preparing or using a handoff does not authorize a commit or push.

Use the [portable prompt templates](prompts/cross-tool-handoff.md). Record a real migration in its existing task or project document; do not create a report per conversation.
