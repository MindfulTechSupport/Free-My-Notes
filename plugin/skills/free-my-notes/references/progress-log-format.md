# Progress log format

The progress log keeps progress between chats. Save it only after the user agrees (see `free-my-notes` section 1).

**Where:** Claude's memory at `/areas/free-my-notes.md` if memory tools are available; otherwise `free-my-notes-log.md` in the user's working folder.

**Never put in the log:** note contents, passwords, account or card numbers, ID numbers, or anything from a sensitive note other than its title and what the user decided. Titles of sensitive notes may themselves be private; if a title contains a number or a name the user may not want stored, write "sensitive note #N" instead.

## Template

```markdown
---
name: free-my-notes
description: Progress log for Free My Notes (Mindful Tech Projects plugin)
---
# Free My Notes: progress log

consent: yes (2026-10-26)
name: Sam
tier: Escape Hatch 1.0.0
goal: leave                        # leave, or backup-only
started: 2026-10-26
buckets: Work (Sam's Bakery), Personal, Not sure, Sensitive
destination: claude-ready
voice-mode: off

## Notes apps
| App | Access | Paying per month | Notes | Status |
|---|---|---|---|---|
| Google Keep | Takeout export (arrived 2026-10-26) | 0 | 476 | copying |
| Evernote | connector | 14.99 USD | 212 | not started |

## Steps (Google Keep)
1. access: done 2026-10-26
2. survey: done (4 labels, 476 notes, 31 without a label)
3. sort: in progress (310 of 476)
4. sensitive: not started
5. copy: not started
6. backup: done (the Takeout zip is the backup)
7. check: not started
8. cancel: nothing to cancel (free app)
9. cleanup: not started

## Notebooks (Google Keep)
| Notebook | Notes | Bucket(s) | Copied | Backup file |
|---|---|---|---|---|
| Side Projects | 95 | Work | 95/95 | takeout-20261026.zip |
| Recipes | 115 | Personal | 0/115 | takeout-20261026.zip |

## At-your-computer list
- Export the Evernote notebooks from the desktop app

## Notes for next time
- Sam wants the Side Projects label copied first.
```

Update the log after every notebook, every step change, and before ending a session.
