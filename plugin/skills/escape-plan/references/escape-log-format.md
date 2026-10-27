# Escape log format

The escape log keeps progress between chats. Save it only after the user agrees (see `escape-plan` section 1).

**Where:** Claude's memory at `/areas/escape-from-evernote.md` if memory tools are available; otherwise `escape-from-evernote-log.md` in the user's working folder.

**Never put in the log:** note contents, passwords, account or card numbers, ID numbers, or anything from a sensitive note other than its title and what the user decided. Titles of sensitive notes may themselves be private; if a title contains a number or a name the user may not want stored, write "sensitive note #N" instead.

## Template

```markdown
---
name: escape-from-evernote
description: Progress log for Escape from Evernote (Mindful Tech Projects plugin)
---
# Escape from Evernote: progress log

consent: yes (2026-10-26)
name: Sam
tier: Escape Hatch 1.0.0
started: 2026-10-26
paying-per-month: 22.00 USD        # optional, for the savings counter
buckets: Work (Sam's Bakery), Personal, Not sure, Sensitive
destination: claude-ready
voice-mode: off

## Steps
1. connect: done 2026-10-26
2. survey: done (32 notebooks, 476 notes, 6 empty notebooks)
3. sort: in progress (310 of 476)
4. sensitive: not started
5. copy: not started
6. backup: not started
7. check: not started
8. cancel: not started
9. cleanup: not started

## Notebooks
| Notebook | Stack | Notes | Bucket(s) | Copied | Backup file |
|---|---|---|---|---|---|
| Side Projects | PROJECTS | 95 | Work | 95/95 | Side Projects (95 notes).enex |
| Recipes | — | 56 | Personal | 0/56 | — |

## At-your-computer list
- Export the .enex backup from the Evernote desktop app

## Notes for next time
- Sam wants the Side Projects notebook copied first.
```

Update the log after every notebook, every step change, and before ending a session.
