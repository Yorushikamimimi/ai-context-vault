# Daily Interaction Report

Use this when you want a short end-of-day record of what your work with AI tools actually produced, without turning it into a scorecard.

## Trigger

The owner asks for it ("today's report"). No scheduled jobs; days nobody asked for are not backfilled.

## How the coordinator writes it

- Read today's commits in the relevant repositories and today's events in the weekly log. Nothing else is required.
- Write one section in the month file `50-Workflow/logs/{{YYYY-MM}}/daily-report.md` (create it from the format below at the start of a month), and show the same text in the conversation.
- At most eight lines; each line is a conclusion plus a pointer to the source document.
- Conversations that wrote nothing back cannot be seen in the files. List them as "off the record" instead of inventing them.
- The report is a history source. It is not part of the recovery path and does not own any current fact.

## Format

```markdown
## {{MM-DD}}

- **Done** (at most 3): {{RESULT}} ([source]({{LINK}}))
- **You decided**: {{DECISIONS_THE_OWNER_MADE}}
- **Energy check**: one sentence comparing where the effort went with the priorities in `00-Profile/goals.md`.
- **Tomorrow** (at most 3, each with its source): {{NEXT}}
- **Off the record**: what the files do not show.
```

The energy check is one sentence against stated priorities. Do not compare item counts, give scores, or ask the owner to make up for missed days.
