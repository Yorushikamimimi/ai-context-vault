# Close-out and Batched Commits

Use this when long-running conversations edit the vault often and uncommitted changes from several conversations start piling up.

## When to close out

- Always when the owner says so ("let's wrap up", "close out for today").
- On the agent's own judgement only when a topic has reached a stopping point and produced a confirmed decision or artifact. Do not close out after ordinary questions, and do not repeat it for the same topic without new progress.

## What close-out does

- Bring the relevant source-of-truth documents and the resume point up to date, so a new agent can continue from files alone.
- Commit this conversation's own changes in batches by topic. Stage explicit paths or hunks only; if a file also holds another conversation's edits and you are unsure which lines are yours, leave them out and say so.
- Before pushing, fetch and check for new remote commits. On conflict, stop and report. Never force-push.

## Standing authorization (owner's choice)

Commit and push are normally separate authorizations (see `../COLLABORATION.md`). An owner may grant a standing authorization for close-out commits and pushes to the vault repository only. Write that grant down here with its date and scope; it does not cover other repositories, deployment, or publication.

## Reporting

- If the tool can message other sessions, send a short report to the coordinating session: files and sections changed, key conclusions, commit hashes, anything needing coordination.
- Otherwise, or across different tools, the commit history is the notice. The coordinator reviews new commits when it resumes. Seeing a report or a commit is not acceptance.
