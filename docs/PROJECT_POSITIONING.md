# Project Positioning

## One sentence

AI Context Vault is a local-first Markdown template for giving AI assistants minimum sufficient personal-workflow context while keeping current facts, history, and publication risk deliberately separated.

## Core value

The template makes six decisions visible instead of leaving them in an agent's memory:

- what an agent reads first and when it stops;
- which document owns a current fact;
- when project status should stay with the project;
- when a small task-memory note or dated weekly history is justified;
- how several AI tools share one vault and one rule file without drifting copies;
- how a private working vault differs from a sanitized public template.

## Two layers

- **Core**: the entry protocol, shared collaboration rules, minimal routing, one owner per fact, source-first handoff, and the privacy boundary. This is all a new user needs.
- **Advanced (optional)**: `vault/50-Workflow/advanced/` covers multi-tool sharing, weekly summaries, and execution records for heavier use. It can be deleted without breaking the core.

## What it is not

- Not another note-taking application: it can sit inside Obsidian or any Markdown folder.
- Not an autonomous agent runtime or a claim of operational verification.
- Not a safe way to publish a filled personal vault.
- Not a replacement for a password manager, encrypted backup, or access-control system.

## Best use cases

- Long-running local AI sessions that need a repeatable recovery path
- Project documentation with one current status owner
- Several AI tools working on the same vault, where source documents are stronger than any one tool's chat history
- Personal workflow templates that must remain private by default

## Maintenance status — 2026-10-27

The GitHub About description now mentions that multiple tools such as Claude Code and Codex share the same context. This is a repository metadata change only; no template files changed. The maintainer keeps a private list of rules that may be synced into this template later; each batch sync gets its own public-release check.

The README now opens with "Try it in 5 minutes": newcomers run the existing fictional `examples/first-recovery/` sample in Codex or Claude Code (a thin `CLAUDE.md` was added next to `AGENTS.md`) and check what the assistant read and whether it kept current decisions, history and unknowns apart. One fresh-session walkthrough followed the expected minimal path on both the current-state question and the history follow-up. This is a single model-run check, not a guarantee for every tool.

## Maintenance status — 2026-10-26

The template now separates shared collaboration rules into `vault/50-Workflow/COLLABORATION.md`, turns `AGENTS.md` and `CLAUDE.md` into identical thin pointers, adds context-reuse rules to `AI_CONTEXT.md`, and introduces the optional `advanced/` layer (multi-tool sharing, weekly summaries, execution records). The README highlights multi-tool sharing, and a Chinese README (`README.zh-CN.md`) mirrors the English one.

This is a manually curated template update, not a mirror of a filled private vault. It adds no real profile, career or health records, operational logs, attachments, credentials, local paths, tool configurations, model names, or private Git history. The 2026-10-24 additions (portable cross-tool acceptance prompts, shared file/section writer ownership, explicit Inbox access, and collaboration guidance) are retained.

Validation covers the changed text files, relative links, placeholder boundaries, a text scan for local paths and personal identifiers, and Git diff. Actual target-tool recovery, instruction loading, tool integration, and user acceptance remain unverified. No dependencies, application runtime, or release package are involved. Push and publication require separate authority.
