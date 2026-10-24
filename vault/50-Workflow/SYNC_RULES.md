# Sync and Persistence Rules

Read this file before a meaningful write, a source-of-truth move, or a handoff update. It routes information; it does not grant permission for external actions, commits, publishing, or deletion.

## Choose one current owner

Use the first applicable destination. Do not copy the same current fact into every layer.

| What changed | Current owner | Optional historical record |
|---|---|---|
| Stable fact, formal state, or domain-specific decision | the relevant domain source of truth | an important weekly log entry only when it changes future understanding |
| Project progress or a project-specific next step | the project's existing `README`, `WORKLOG`, `CURRENT_PROGRESS`, or equivalent | an important weekly log entry |
| Cross-session task context with no suitable project or domain owner | one focused file under `task-memory/` | an important weekly log entry |
| Important dated milestone, evidence, decision, or unresolved risk | keep current facts in their normal owner | one file under `logs/` |

`SYSTEM_STATUS.md` is a small index of current priorities and entry paths. It is not a duplicate project board or chronological diary.

## Write triggers

Route a change when it creates a reusable artifact, changes a confirmed decision or current state, produces a new verification result, or leaves a necessary next-session handoff. Do not persist casual discussion, full chat transcripts, repeated generated text, command output, or facts that already have a better current owner.

When there is no authorization to write, provide a concise proposed update and state that it has not been persisted.

## Focused task-memory rule

Create task memory only when all of these are true:

1. The work will continue across sessions or tools.
2. It has real decisions, constraints, progress, or a blocker worth recovering.
3. No project document or domain source already owns that state.
4. One small note materially lowers the cost of resuming.

Maintain one current file per task. Keep current progress to at most five concise items and next actions to at most three. See `task-memory/README.md` for the template.

## Weekly history rule

Use `logs/` only for milestones that need a dated audit trail: a material decision, an accepted artifact, a verified result, a failure that constrains future work, or a change of direction. Record the conclusion, artifact, verification coverage, what remains unproven, and the next entry point. A weekly log must never become the sole owner of the current state.

## Link and move integrity

When moving or retiring a current source:

1. update the prior index or entry file;
2. update the destination index or entry file;
3. update active Markdown links and documented paths;
4. retain historical paths in dated history unless changing them is necessary to avoid a false current instruction.

## Privacy and publication boundary

- Keep secrets, credentials, private identifiers, raw exports, private chat text, and sensitive third-party information out of public template files.
- Use placeholders such as `{{PROJECT_NAME}}`, `{{DATE}}`, and `{{UNKNOWN}}` in examples. Do not replace missing evidence with realistic-looking fabricated data.
- A filled private vault is not a publishable repository. Build and review a separate sanitized copy using the repository-root `docs/PRIVACY_CHECKLIST.md` and `docs/PUBLICATION_GUIDE.md`.

## Shared writing and ownership

The agent that did the work maintains its existing current document and, when justified, its milestone log. A coordinator checks cross-task conflicts rather than rewriting every report.

One writer per responsibility is not sufficient when different responsibilities share a file. Assign one current writer to each shared file or section, including linked cards and indexes. Before transferring that ownership, pause the prior writer, reread the latest content, reconcile pending changes, and update related entries serially. Preserve unrelated edits. Record post-cutoff changes and recheck the affected handoff.

`90-Inbox/` is not an automatic maintenance queue. Read or organize it only after the user explicitly authorizes the necessary subpath. A recurring checklist is not permission to inspect private material.
