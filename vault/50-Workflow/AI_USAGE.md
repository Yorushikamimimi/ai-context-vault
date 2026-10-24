# AI Usage Guide

## Start or continue work

Ask the agent to read `AI_CONTEXT.md`, select a minimal recovery route, and name the current source it will use. Do not ask it to scan the whole vault for background.

## Summarize a conversation safely

Use this request when an authorized, evidence-bound handoff is needed:

```text
List only the confirmed, unpersisted delta from this conversation: decisions, artifacts, verification, unknowns, and next entry point. For each item, suggest its source-of-truth destination. Do not invent file changes or copy the full conversation.
```

Then review the proposal against `SYNC_RULES.md` before writing. An ordinary summary is not automatically a weekly log or task-memory update.

## Common routing

| Scenario | Read | Write when authorized |
|---|---|---|
| Project work | the named project's current document | that same project document |
| Domain fact | the relevant domain source of truth | that source, plus only required links |
| Cross-session work with no other owner | `task-memory/README.md` | one focused task-memory file |
| Important milestone | the current owner and `logs/weekly-log-template.md` | the current owner, then one concise weekly entry |
| Conversation migration | `conversation-handoff.md` | existing source first; only the unpersisted delta afterward |
| Prompt reuse | `prompts/README.md` | a focused reusable prompt file |

## Evidence boundary

State what was verified, inferred, and unknown. A successful file write or static check does not prove an external workflow, deployed service, user acceptance, or privacy-safe publication.

## Clear tasks and adjustable previews

Do a clear, bounded task directly. Clarify only a material ambiguity. For frontend design, show a viewable preview with fictional representative content before production changes, unless the user has approved that direction or explicitly waived preview. Validate the implemented UI against the approved view and required states; compilation alone is insufficient.

## External reading

Keep the original material separate from agent research and user conclusions. Check important, uncertain, or changing claims against appropriate primary sources. Record whether an idea was saved, discussed, adopted, tried, or verified; these are different states. Do not turn a personal reminder into an agent policy or a personality diagnosis without the user's decision.
