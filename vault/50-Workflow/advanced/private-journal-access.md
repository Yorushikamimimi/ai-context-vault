# Read-only Access to a Private Journal

Use this when the owner wants an agent to read exports from a private journal app without the journal entering Git or being reread in full every time. This file describes the method only; it contains no journal content.

## Storage

- Keep the original exports in a private, Git-ignored folder such as `{{PRIVATE_DIR}}/journal/originals/{{YYYY-MM-DD}}/`, one folder per export date. Originals are read-only: never edit, rename, or reformat them.
- Never copy journal text into tracked files. Tracked documents may at most hold a one-line, non-quoting summary.

## Who reads, and when

- Name the one agent or responsibility allowed to read the journal (for example the coordinating session). Other tools and responsibilities do not read it, even if they could.
- Read only when the owner starts it. No timers, folder watchers, or background reading.

## Updating

- The owner exports from the app and says so ("sync the journal"). The agent makes sure cloud placeholder files are fully downloaded, checks that the export's entry count is complete, then copies it into a new dated folder.
- Temporary copies in cloud or download folders are deleted by the owner, not the agent.

## Using what was read

- Monthly summaries live next to the originals, for example `{{PRIVATE_DIR}}/journal/summaries/`, with a README recording progress and how summaries are written. Read the summaries first; go back to the originals by date only when a detail is needed. A first full read goes in chronological batches.
- Observations about personality or what matters to the owner go into a private observation note. Moving any of it into the profile needs the owner's confirmation.
- A daily report mentions the journal in one summarizing sentence at most, never quoting it.
- Emotions and stress are observed, not diagnosed. If there are clear signs of something serious, say directly that talking to someone or seeking professional help would be good.
