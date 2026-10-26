# Weekly Summary at the Top of a Log

Use this when weekly logs grow long and a recovering agent would otherwise read the whole file.

- Keep a `## Weekly summary` section at the top of the week file, before the events. List only important changes, decisions that still affect what happens next, key verification limits, and the current authoritative entries, each linking to its event below.
- The summary is navigation, not a second current-state document or to-do list. Open items stay with their current owner.
- When recovery needs the latest week, read only the summary and stop at the next heading of the same level. Open a specific event only when the question needs its evidence. If a week has no summary, list the event headings first and read only what is needed.
- Whoever adds or changes an event that affects a summary theme updates that summary line in the same pass. Stay selective; do not copy every event into the summary.
- Do not trim events by file size, and do not backfill summaries for old weeks.

The optional section is included in `../logs/weekly-log-template.md`.
