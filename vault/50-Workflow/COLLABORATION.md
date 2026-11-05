# Collaboration Rules

Shared working rules for every AI tool that uses this vault. Agent entry files (`../AGENTS.md`, `../CLAUDE.md`, or another tool's entry) only point here and to `../AI_CONTEXT.md`; keep the rule text in this one file. Reading routes and privacy boundaries stay in `AI_CONTEXT.md`.

## Communication

- Default reply language: `{{PREFERRED_LANGUAGE}}`. Keep technical terms as written.
- Lead with the conclusion and the next step. Separate verified facts, inferences, and unknowns.
- When sources conflict, say so and prefer the newer, better-evidenced, or more explicit statement instead of guessing.

## Scope and authorization

- Do only what was asked. Report unrelated problems instead of fixing them.
- Execute clear, bounded tasks directly. Ask only when missing information would materially change the outcome, scope, authority, or risk; do not require a fixed interview before every task.
- Commit, push, deploy, publish, delete, rename, archive, and contacting others are separate authorizations. Approval for one action does not cover the next.
- Do not read, print, or copy credentials, tokens, cookies, or `.env` files without explicit scope.

## Evidence

- Prefer code and real data, then version history, then run results, then documents, then an agent's report.
- Check another agent's "done" against the actual artifacts. A passing check is not proof of a working service, a deployment, or user acceptance.
- Acceptance first: for anything beyond a small change, write observable acceptance criteria before starting ("open this page, click here, you should see that"). At the end, report against each one; an agent's self-assessment does not replace them.
- Converging reviews: sort review findings into must fix (affects acceptance), could fix (note it for later), and won't fix (style preference). Fix only the first kind in this round. Run at most two review rounds on the same change; if disagreement remains, the user decides.
- Visible filtering: when screening material, candidates, or options for the user, also list what was excluded with a one-line reason. For major decisions (offers, contracts, staying or leaving, large spending), present the strongest counter-argument alongside the recommendation, and where it fits, ask for the user's own leaning first.

## Verification

- Tests that open visible windows or take focus (desktop GUIs, automation that launches a visible browser) are not run repeatedly while work is in progress. Prefer background or headless runs. Tests that need a real window, and screenshots, run once at the end, after asking the user about timing, or are handed to the user to run.
- A browser tool that works in its own isolated workspace without taking over the user's screen does not count as a pop-up test.
- This applies to every executor, including delegated ones: write it into delegation prompts. The exception is when the user has said pop-ups are fine.

## Projects and repositories

- Each project keeps its own README and one current-progress document; update that document after meaningful work.
- Project READMEs explain purpose, actual results, a concrete usage example, and the real start or download entry before long development details. Keep internal work queues in the current-progress document.
- Before changing visible frontend behavior, provide a viewable, adjustable preview using fictional data. Implement after explicit approval, unless the user has approved this direction or explicitly skipped preview. Silence is not approval; a build is not visual acceptance.
- Interfaces look current by default, with transitions, progress feedback, and responses to interaction, unless the user asks for something simple or static. Details: `AI_USAGE.md` "Clear tasks and adjustable previews".
- Before creating a remote repository, ask for its name unless the user has explicitly provided or confirmed it. A local folder name is not confirmation.
- Git: commit as `{{GIT_NAME}} <{{GIT_EMAIL}}>`, stage only the current task's changes, and use `{{COMMIT_MESSAGE_STYLE}}`. Do not rewrite shared history.

## Keeping records short

- An event or progress entry has at most five points, each at most two lines. Put every limitation in one "Not proven" line.
- Index rows and table cells hold a conclusion plus a link. Details go to the project or evidence file.
- When a new rule replaces or overlaps an old one, merge or delete the old one in the same change.
- Every so often, shorten the longest few places. Shortening moves details and merges repeats; it never deletes a decision change or where its evidence lives.
- Entry documents (`AI_CONTEXT.md`, `SYSTEM_STATUS.md`, indexes, READMEs, current-progress files) are rewritten in place to the current conclusion, never appended to as a running log. A paragraph holds only the conclusion, its limits, and a pointer; debugging steps, verification details, and version numbers go to the project or evidence file. Before writing, check whether the same section already has a sentence to merge with.
- Keep this rules file lean. A section needed only for certain tasks (design, READMEs, publishing, browser use) keeps a one-line rule plus a pointer to the detailed guide, and the pointer names the guide's maintained source path, so stale copies elsewhere do not matter. The details live only in that guide.

## Tools and external material


- Select browser, model, and tool integrations from the user's preferences and the current tool's actual capabilities. Do not hard-code one machine's configuration or assume a Skill is installed.
- Use sub-agents only when the task needs them. When the tool accepts model and effort parameters, pass them explicitly in the call, and say which model, effort, and how many were used. Distinguish "passed" from "verified"; if the platform does not report it, say so instead of guessing.
- When studying external material, separate original material, agent research, interpretation, user decisions, and actual practice. Preserve source links and verification limits; saving a note does not mean the user adopted it.
- For cross-tool continuity, use `conversation-handoff.md`. Templates and correct answers do not prove a tool is usable, access stayed in scope, or a handoff has been accepted.
