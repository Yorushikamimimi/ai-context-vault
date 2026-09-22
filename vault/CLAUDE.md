# CLAUDE.md

Treat this directory as an AI Context Vault.

## Start a session

1. Read `AI_CONTEXT.md`.
2. Choose the smallest recovery route that supports the user's request.
3. Read only the exact current sources required by that route.

## Rules

- Before a meaningful write, read `50-Workflow/SYNC_RULES.md` and update the smallest current owner.
- Prefer documented sources of truth over old chat context; use `50-Workflow/conversation-handoff.md` when moving a task between conversations.
- Do not search or read private, operational, inbox, export, or credential material without explicit scope from the user.
- Do not treat a request to summarize a conversation as permission to append a transcript. Persist only confirmed, routed changes when authorized.
