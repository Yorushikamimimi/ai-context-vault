# Sharing One Vault Across AI Tools

Use this when two or more AI tools (for example a coding agent, a desktop assistant, and a web chat) work on the same vault. The vault is the shared base; each tool is a replaceable entry point. Switching tools is not a migration, and no tool becomes the permanent authority.

## Three layers

- **Shared rules**: `../COLLABORATION.md`, kept as one copy.
- **Vault protocol**: `../../AI_CONTEXT.md` for reading routes and privacy, `../SYNC_RULES.md` for where writes go.
- **Platform adapter**: each tool's entry file plus its own model, tool, and Skill settings. Keep platform-specific notes there. Do not copy one tool's model names, tool names, or settings into the shared rules.

## Adding a new tool

1. Check what the tool loads on startup: entry files in the folder and its parents, plugins, and built-in memory. Isolate conflicting old rules in a recoverable way; do not delete shared sources that other tools still use.
2. Give it a thin entry file that points to `AI_CONTEXT.md` and `COLLABORATION.md`.
3. Recover read-only first, then run one small authorized write and read-back, then one real small task. The gates are described in `../conversation-handoff.md` ("Cross-tool acceptance procedure").
4. Record which responsibilities this tool may now maintain, in your responsibility index or the project's own documents. Other responsibilities stay with their current tool until you restore them one at a time.

## Day to day

- Any authorized tool may write, but only one writer per file or section at a time. Re-read the target right before writing; never overwrite from an old copy.
- When you return to a tool after others have edited, refresh only the sources relevant to the task (see "Reusing context" in `AI_CONTEXT.md`). Do not repeat onboarding.
- A tool's built-in memory is not a source of truth for vault facts. Prefer turning it off or ignoring it.
- Shared Skills or prompts: keep one maintained copy and point each tool to it. Similar names do not mean the same behaviour on every tool.
- Updating a rule file, delivering a notice, and a tool actually following the rule are three different things. Judge adoption by the tool's later answers and actions.

## Pitfalls

- On case-insensitive file systems, a documentation file named like another tool's entry file (for example `claude.md`) may be loaded as instructions. Give documentation files distinct names.
- An entry file in a parent folder (such as a workspace or home folder) applies to every project below it. Check parent folders when onboarding a tool.
