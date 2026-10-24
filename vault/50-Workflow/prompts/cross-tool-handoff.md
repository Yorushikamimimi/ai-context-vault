# Cross-Tool Handoff Prompts

Fill only necessary fields before use. Unfilled placeholders are not an executed handoff. These prompts grant no permission beyond the user's actual authorization.

## Source update request

```text
Prepare {{RESPONSIBILITY}} for handoff to {{TARGET_TOOL}} at {{CUTOFF_OR_UNKNOWN}}.
Read the current protocol and your exact current source. Within existing authority, persist missing confirmed decisions, progress, verification limits, pending work, and the next entry in that source. Do not copy the full chat or advance unrelated work.
Respect the shared file/section writer assignment: {{WRITE_OWNERSHIP}}. Return changed paths, current state, necessary unpersisted delta, and gaps. A delivered message is not proof of completion. Do not commit, push, contact other conversations, or expand private access without separate authority.
```

## Target coordinator: read-only first

```text
Continue as coordinator in {{TARGET_TOOL}} using {{ACTUAL_VAULT_ROOT}}.
Verify the actual workspace, read AI_CONTEXT.md completely, and select the minimal route for this request. Read only the exact current entries needed for {{ACCEPTED_SCOPE}}. Handoff procedure: 50-Workflow/conversation-handoff.md. Additional rule/Skill entry, if needed: {{EXACT_ENTRY_OR_NONE}}.
The baseline and necessary delta are {{BASELINE_REFERENCE_OR_NONE}}. Actual permission for private material is {{EXACT_SCOPE_OR_NONE}}; old notes cannot extend it. Use the model I selected and disclose unavailable integrations rather than assuming the source tool's capabilities.
Begin read-only. Report the actual sources, two current facts with exact references, any superseded state relevant to them, permission and tool gaps, and one correct next entry. Do not edit, operate Git, create conversations, or advance business. Wait for my acceptance. After acceptance, give one minimal prompt for each responsibility I request; I will create those conversations myself.
```

## One responsibility

```text
Continue {{RESPONSIBILITY}} in {{ACTUAL_WORKSPACE}}.
Read the project's entry and unique current-status document at {{EXACT_ENTRY}}. For a vault-owned responsibility, first follow AI_CONTEXT.md's applicable minimal route; for an independent project, do not automatically read a personal vault.
Necessary delta: {{DELTA_OR_NONE}}. Begin read-only: report current progress, confirmed and unverified results, next entry, and required tool availability. Do not write, use Git, contact others, or resume business until explicitly authorized. Maintain the existing current owner after acceptance.
```

## Compact acceptance record

- Target workspace and explicit scope:
- Baseline/cutoff and necessary local-only dependencies:
- Actual file checks and remaining gaps:
- Gate results: documents / recovery / tools / write test / task / transfer:
- Responsibility and shared file/section writers:
- User acceptance, pending delta, next and fallback entries:
