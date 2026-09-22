# AI Context Protocol

Last updated: `{{YYYY-MM-DD}}`

## Purpose

This protocol helps a human or AI agent recover only the context needed for the current request. It does not authorize reads, writes, commits, sharing, or external actions on its own.

## Vault summary

- Owner label: `{{OWNER_LABEL_OR_LEAVE_BLANK}}`
- Stable summary: `{{SHORT_NON_SENSITIVE_SUMMARY}}`
- Current priority: `{{CURRENT_PRIORITY_OR_UNKNOWN}}`

Keep personal identifiers, credentials, private relationships, medical information, and operational details out of this public template.

## Minimal context routing

Choose one route before reading. Start narrow and stop once the requested fields have support from a current source.

| Route | Use for | Required reading | Do not read by default |
|---|---|---|---|
| A — self-contained task | translation, a narrow explanation, formatting, or a task whose facts are entirely in the request | this file | `SYSTEM_STATUS.md`, profile, logs, and unrelated folders |
| B — one domain | one project, knowledge area, career workflow, or workflow rule | this file, then that domain's source of truth | other domain folders; read `SYNC_RULES.md` only before a meaningful write or when asked where to write |
| C — cross-domain or vault governance | a decision that genuinely depends on current system-wide state | this file, `SYSTEM_STATUS.md`, then the exact sources needed | full-profile recovery, historical logs, and broad directory scans |
| D — explicit task or project continuation | the user names an existing responsibility, project, or handoff | this file, then the named project's current-status document or the named task-memory file | unrelated logs and old chats unless they fill a documented gap |

If a source does not answer one required field, open one additional, explicitly relevant source and reassess. A link, a keyword, or the ability to access a folder is not permission to read it.

## Search and privacy boundary

- Prefer an exact known path. Before searching, define the smallest allowed file or directory scope and the unanswered question it serves.
- Do not use broad repository-wide recursive search, directory enumeration, ignore-rule bypasses, or snippet collection as a substitute for a reading decision.
- Treat search results and filenames as content access. Exclude private, operational, inbox, export, and credential locations unless the user explicitly identifies the necessary scope.
- Do not read, copy, log, or place credentials, tokens, cookies, private keys, raw chat exports, or third-party confidential text into templates, task memory, or public repositories.
- Do not infer permission from an old note. Ask when a requested action would materially broaden scope, disclose data, or change an external system.

## Directory map and current owners

### `00-Profile/`

Purpose: stable preferences, goals, and non-sensitive constraints.

- Read only when the answer depends on them.
- Current sources: `identity.md`, `goals.md`, `skills.md`, `working-style.md`.

### `10-Knowledge/`

Purpose: reusable learning notes.

- Read only for the relevant topic or when the user explicitly requests it.

### `20-Projects/`

Purpose: project index and project-facing documentation.

- Each project should own its current state in its own `README`, `WORKLOG`, `CURRENT_PROGRESS`, or equivalent.
- A generic task-memory file must not duplicate an existing project status document.

### `30-Career/` (optional)

Purpose: resume, applications, interviews, job fairs, and growth notes.

- Application facts: `10-Applications/application-progress.md`
- Interview events: `20-Interviews/records.md`
- Preparation material: a focused file under `20-Interviews/`

### `50-Workflow/`

Purpose: the rules for AI collaboration, handoff, and persistence.

- Write routing: `SYNC_RULES.md`
- Source-first migration: `conversation-handoff.md`
- Lightweight task memory: `task-memory/README.md`
- Important weekly history: `logs/README.md`

### `90-Inbox/`

Purpose: temporary capture only. It is not a source of truth and should not be searched by default.

## Writing and evidence rules

- Prefer real current data, the relevant source of truth, and verified project evidence over an agent's memory or an old conversation.
- Mark unknown, inferred, and verified information distinctly. A file's existence, a passing static check, or an agent report is not proof of runtime behavior or an external outcome.
- Before a meaningful write, read `50-Workflow/SYNC_RULES.md`; update the smallest current owner and only the required links.
- Preserve history in a dated weekly log only for important milestones. Do not write routine chat summaries or complete transcripts into the vault.
- Moving a file requires updating the old entry point, the new entry point, and active links. Historical references may remain historical.

## Agent entry files

Local agent instruction files should point here and avoid duplicating the full protocol. This makes the protocol the single update point.
