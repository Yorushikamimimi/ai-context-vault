# Delegation Task Card

A two-sided template for delegating research, static code analysis, or batch mechanical tasks that do not require the main controller's aesthetic judgment to another AI (a web model or another local agent).

The front card is sent to the executor; the back card stays with the project or main controller for acceptance.

## Front: send to executor

Provide this block to the delegated AI.

```text
You are assigned a delegated task. Do only what is specified below. If you encounter issues outside this scope, report them—do not fix them.

[Task]
{{ONE_SENTENCE_GOAL}}

[Context]
{{BACKGROUND_AND_WHY_THIS_MATTERS}}

[Materials]
- Workspace / local entry path: {{LOCAL_PATH_OR_NOT_APPLICABLE}}
- Attached or referenced text: {{ATTACHED_TEXT_OR_NOT_APPLICABLE}}

[Scope]
- Allowed to edit: {{ALLOWED_FILES_OR_NEW_FILE_PATHS}}
- Do not touch: do not inspect or modify credentials, tokens, cookies, or .env files; do not run git commit, git push, or deploy commands; do not edit files outside the allowed scope.

[Requirements]
{{NUMBERED_TECHNICAL_OR_FORMATTING_REQUIREMENTS}}

[Standard constraints]
- Do not start background daemons, scheduled jobs, or cron tasks.
- Do not access logged-in personal websites or authenticated remote services.
- Do not trigger focus-stealing pop-up windows or interactive GUI alerts while work is in progress.
- When unsure about a fact, dependency, or result, write "unknown" instead of guessing.

[Deliverables]
1. Target artifact: {{PRIMARY_OUTPUT_FILE_OR_CONTENT}}
2. Self-check report: a concise summary covering completed checks and any out-of-scope findings discovered during execution.

[Not considered done]
The task is not considered done if:
- Any file outside the allowed scope was modified;
- Tests or verification commands failed or were skipped without explanation;
- Credentials, private paths, or unverified claims are present in deliverables.
Report incomplete status or obstacles rather than claiming completion.
```

## Back: controller acceptance card

Keep this block with the main controller or project owner to verify deliverables.

```markdown
### Acceptance: {{TASK_OR_SUBPROJECT_NAME}}

- **Assigned executor:** {{EXECUTOR_TOOL_OR_MODEL}}
- **Delivery timestamp:** {{TIMESTAMP_OR_DATE}}

[Acceptance criteria]
- [ ] {{OBSERVABLE_CHECK_1}}
- [ ] {{OBSERVABLE_CHECK_2}}

[Spot check]
- Files or outputs to inspect directly: {{KEY_SOURCE_FILES_OR_GENERATED_OUTPUTS}}
- Scope compliance check: verify no forbidden files were touched, no secrets or private paths leaked.

[After pass]
- Record a single-line delegation status in the project's current progress document (for example: `- [x] Task A delegated to {{EXECUTOR}} passed acceptance on {{DATE}}`).
- No separate central board is needed by default; progress stays with the owning project.
```
