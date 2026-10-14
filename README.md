# AI Context Vault

A local-first Markdown template for giving AI assistants the **smallest useful amount of context** without turning a personal archive into a public data dump.

It works in Obsidian or any ordinary Markdown folder, and is intended for Codex, Claude Code, ChatGPT, and similar tools that work across more than one session.

> This repository contains placeholders and clearly labelled fictional examples. A vault filled with real life, work, account, or project data is **not ready to publish** just because it started from this template.

## What it solves

Most long-running AI work has two opposite failure modes: every new session starts cold, or an agent reads far more personal material than the task needs. This template makes the boundaries explicit:

- one entry protocol that chooses a minimal recovery path;
- clear source-of-truth files instead of a single growing chat summary;
- separate homes for project status, lightweight cross-session task memory, and important weekly history;
- source-first handoff, so old conversations only supply an unrecorded delta;
- publication and search boundaries that keep private material out of routine reads.

It is a template and documentation framework, not a note-taking application, secret manager, backup service, or proof that an AI workflow has been tested in production.

## Current status

- Stage: reusable public template
- Contents: sanitized placeholders and a fictional recovery example; no real personal, account, or operational data
- Runtime: Markdown only; no automated workflow or privacy scan is claimed
- Intended use: copy, tailor locally, then keep your filled vault private by default

## Structure

```text
vault/
  AI_CONTEXT.md                         # minimal-context entry protocol
  SYSTEM_STATUS.md                      # small current-state index, not a full history
  AGENTS.md                             # optional Codex agent entry pointer
  CLAUDE.md                             # optional Claude Code entry rule
  00-Profile/                           # stable preferences and goals
  10-Knowledge/                         # reusable learning notes
  20-Projects/                          # project index; each project owns its own status
  30-Career/                            # optional career workflow templates
  50-Workflow/
    SYNC_RULES.md                       # write-routing and link-update rules
    conversation-handoff.md             # source-first handoff template
    task-memory/README.md               # only for tasks lacking another current source
    logs/weekly-log-template.md         # important dated history, never the current owner
    prompts/                            # reusable prompts
  90-Inbox/                             # temporary, unprocessed capture
docs/
  PRIVACY_CHECKLIST.md                  # sanitize before any publication
  PUBLICATION_GUIDE.md                  # safe public-release process
  PROJECT_POSITIONING.md                # scope and positioning
```

## First recovery example / 第一次恢复上下文

Start with the [fictional beginner example (中文)](examples/first-recovery/README.md). Its filled Markdown files show where current project state and past decisions belong, which files a new conversation should read, and what remains unverified. You do not need to fill a personal profile or read every domain folder.

This example contains no application code, real personal records, or runtime results. Reading it is not evidence that any project has run successfully.

## Quick start

1. Copy the repository into a private Markdown workspace. If you copy only `vault/`, keep the root `docs/` directory with it for the publication checklist and guide.
2. Replace only the placeholders you need in `vault/00-Profile/` and the relevant domain folders. Leave unknown fields blank or marked `{{UNKNOWN}}`; do not invent facts for completeness.
3. Start each AI session with the prompt below. The agent should read the protocol first and then only the specific sources needed for the task.

   ```text
   Read and follow {{VAULT_PATH}}/AI_CONTEXT.md. Use the smallest recovery path that supports this request. Do not search or read private material unless I explicitly name the file or folder.
   ```

4. Before asking an agent to write, review `vault/50-Workflow/SYNC_RULES.md`. It explains where a current fact belongs and when a weekly log is appropriate.
5. When context must move to a new conversation, use `vault/50-Workflow/conversation-handoff.md`; start from the documented source of truth, not a copied chat transcript.

## The four storage layers

| Need | Canonical home | What it must not become |
|---|---|---|
| Stable fact or formal current state | the relevant domain source of truth | a copy of every conversation |
| Current project progress | that project's `README`, `WORKLOG`, `CURRENT_PROGRESS`, or equivalent | a second generic task note |
| Cross-session context with no better owner | one file under `50-Workflow/task-memory/` | an archive of chat transcripts |
| Important dated milestone | `50-Workflow/logs/` | the only current-state record |

## Recommended entry rule

For Codex, Claude Code, or another local agent, point the agent at the protocol rather than reproducing rules in several instruction files. This template includes `vault/AGENTS.md` for Codex-style agents and `vault/CLAUDE.md` for Claude Code; both are deliberately small entry pointers.

```text
Before working in this vault, read and follow {{VAULT_PATH}}/AI_CONTEXT.md.
Use its context routing and privacy boundaries. Before a meaningful write, read {{VAULT_PATH}}/50-Workflow/SYNC_RULES.md and update only the documented source of truth.
```

## Privacy before publication

Keep your working vault private. If you want a public example, build a separate sanitized copy and review it line by line. Do not publish a filled vault directly—even if you removed obvious credentials.

Read [the privacy checklist](docs/PRIVACY_CHECKLIST.md) and [publication guide](docs/PUBLICATION_GUIDE.md) before any public push, release, or share link.

## Scope

The template includes optional career examples because they demonstrate source-of-truth routing. They are not required: remove or replace folders that do not fit your use case. The core is the protocol, the write-routing rules, and the privacy boundary.

## License

MIT
