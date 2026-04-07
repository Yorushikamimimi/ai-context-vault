# AI Context Vault

AI-readable personal context vault template for Obsidian, Codex, Claude Code, and long-running AI workflows.

> Recommended GitHub description: AI-readable personal context vault template for Obsidian, Codex, Claude Code, and long-running AI workflows.

## What This Is

AI Context Vault is a Markdown-based template that helps AI tools recover your long-term context quickly and safely.

It is designed for people who use AI assistants across many sessions and want a clean, local-first way to describe:

- who they are
- what they are working on
- what files are source of truth
- how AI agents should update the archive
- what must stay private

It provides:

- A single AI entry protocol: `vault/AI_CONTEXT.md`
- A handoff snapshot for future sessions: `vault/SYSTEM_STATUS.md`
- A profile layer for stable preferences and constraints
- A project layer for portfolio and engineering work
- A career layer for applications, interviews, and job fairs
- A workflow layer for daily logs, sync rules, and reusable prompts

## Current Status

- Stage: public template MVP
- Data policy: sanitized placeholders only
- Code: no runtime code, Markdown template repository
- Main focus: AI context recovery, cross-tool handoff, and privacy-safe publication

## Who It Helps

This template is useful if you:

- use Codex, Claude Code, ChatGPT, or other AI agents across multiple sessions
- want AI tools to understand your stable preferences without repeating context every time
- are managing job applications, interviews, projects, and learning notes
- want a local-first personal operating system based on Markdown

## What It Can Help With

- Resume and interview preparation
- Project retrospectives and portfolio positioning
- Daily work summaries
- Cross-tool AI handoff
- Personal knowledge organization
- Reducing repeated context setup in new AI conversations

## Structure

```text
vault/
  AI_CONTEXT.md                 # agent entry protocol
  SYSTEM_STATUS.md              # current state and handoff snapshot
  CLAUDE.md                     # Claude Code entry rule
  00-Profile/                   # identity, goals, skills, working style
  10-Knowledge/                 # reusable learning notes
  20-Projects/                  # project index and retrospectives
  30-Career/                    # resume, applications, interviews, job fairs
  50-Workflow/                  # AI usage, sync rules, daily logs, prompts
  90-Inbox/                     # temporary capture
docs/
  PRIVACY_CHECKLIST.md          # before publishing a filled vault
  PUBLICATION_GUIDE.md          # GitHub release guidance
  PROJECT_POSITIONING.md        # product positioning and similar tools
```

## What It Is Not

- It is not a private data backup system.
- It is not a replacement for Obsidian, Logseq, Notion, or Anytype.
- It is not safe to publish after filling it with real personal data unless you sanitize it first.

## Quick Start

1. Copy the `vault/` directory into your Obsidian workspace.
2. Fill in `vault/00-Profile/identity.md`, `goals.md`, `skills.md`, and `working-style.md`.
3. Tell your AI tool:

```text
Please read and follow ./vault/AI_CONTEXT.md before working with this archive.
```

4. For daily handoff, say:

```text
Summarize the current conversation.
```

Then ask the AI to append the summary to `vault/50-Workflow/daily-log.md`.

## Common Workflows

### Start A New AI Session

```text
Please read and follow ./vault/AI_CONTEXT.md before working with this archive.
```

### Summarize A Conversation

```text
Summarize the current conversation.
```

Expected output location:

```text
vault/50-Workflow/daily-log.md
```

### Update Career Progress

Use:

```text
vault/30-Career/10-Applications/application-progress.md
vault/30-Career/20-Interviews/records.md
```

### Reuse Web AI Output

Use:

```text
vault/50-Workflow/prompts/web-conversation-summary-template.md
```

## Recommended Agent Entry Rule

For Codex or Claude Code, put this in your local agent instructions and adjust the path:

```text
At the beginning of every new session, first read and follow {{VAULT_PATH}}/AI_CONTEXT.md.
Follow the read order, directory triggers, behavior constraints, and context recovery rules defined there.
```

## Privacy Warning

Do not publish your filled vault directly.

Before pushing to GitHub, read:

- `docs/PRIVACY_CHECKLIST.md`
- `docs/PUBLICATION_GUIDE.md`

## Roadmap

- Add more reusable templates for projects, interviews, and daily reviews
- Add optional script-based privacy scan
- Add example filled vault with fake data
- Add screenshots or diagrams for the vault workflow

## License

MIT
