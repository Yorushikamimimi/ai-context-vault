# AI Usage Guide

## Short Command

### Summarize the current conversation

When the user says:

```text
Summarize the current conversation
```

The AI should:

1. Read `AI_CONTEXT.md` and `50-Workflow/SYNC_RULES.md`
2. Append useful content to `50-Workflow/daily-log.md`
3. Record only:
   - what was discussed
   - what changed
   - what decisions were made
   - next actions
4. Check whether other files need sync updates
5. Keep it concise

## Common Scenarios

| Scenario | Read | Write |
|---|---|---|
| Career / interview | `30-Career/README.md` | application progress, records, prep notes |
| Project work | `20-Projects/index.md` | project index or project notes |
| Daily review | `50-Workflow/daily.md` | `daily-log.md` |
| Prompt reuse | `50-Workflow/prompts/README.md` | prompts directory |

