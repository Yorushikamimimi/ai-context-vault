# AI Context Protocol

Last Updated: {{YYYY-MM-DD}}

## Vault Owner

- Owner: `{{NAME}}`
- Identity Summary: `{{SHORT_IDENTITY_SUMMARY}}`
- Current Priority: `{{CURRENT_PRIORITY}}`

## Read Order

1. `AI_CONTEXT.md`
2. `SYSTEM_STATUS.md`
3. `00-Profile/identity.md`
4. `00-Profile/goals.md`
5. Read other directories only when triggered by the current task

## Directory Protocol

### `00-Profile`

- Purpose: stable identity, preferences, goals, constraints
- Default Read: Yes
- Trigger Words: default read

### `10-Knowledge`

- Purpose: learning notes and reusable knowledge
- Default Read: No
- Trigger Words: knowledge, study, learning, review, backend, frontend, algorithm

### `20-Projects`

- Purpose: project index, portfolio projects, retrospectives
- Default Read: No
- Trigger Words: project, repo, portfolio, architecture, system design

### `30-Career`

- Purpose: resume, applications, interviews, job fairs, career growth
- Default Read: No
- Trigger Words: interview, job, resume, application, HR, phone call, job fair, offer
- Source of Truth:
  - Applications: `30-Career/10-Applications/application-progress.md`
  - Interview records: `30-Career/20-Interviews/records.md`
  - Interview questions: `30-Career/20-Interviews/questions.md`
  - Target companies: `30-Career/10-Applications/target-companies.md`

### `50-Workflow`

- Purpose: AI usage, sync rules, daily logs, prompts, decision rules
- Default Read: No
- Trigger Words: workflow, productivity, review, decision, tool, prompt, summarize current conversation
- Source of Truth:
  - AI usage: `50-Workflow/AI_USAGE.md`
  - Sync rules: `50-Workflow/SYNC_RULES.md`
  - Daily log: `50-Workflow/daily-log.md`
  - Reusable prompts: `50-Workflow/prompts/`

### `90-Inbox`

- Purpose: temporary capture
- Default Read: No
- Trigger Words: inbox, capture, save this

## Behavior Constraints

- Default language: `{{DEFAULT_LANGUAGE}}`
- Keep answers concise and actionable
- Prefer user-stated current instruction over old archive context
- Do not read private or ops directories unless explicitly requested
- When a change is meaningful, update the corresponding source-of-truth file

## Operating Rule

Agent entry files should only point to this protocol. Detailed workflow rules should live inside this vault.

