# Design notes — Escape from Evernote 1.0.0
*Mindful Tech Projects · 2026-10-26*

## Where it came from

The founder moved his own Evernote out with Claude: 476 notes in 32 notebooks, sorted into work and personal, sensitive notes kept in restricted folders, every notebook exported to `.enex` and backed up twice, and the subscription canceled ($22 a month saved). Escape from Evernote turns that escape into a guided plugin anyone can run.

## Who it's for

- **Everyday people** with years of recipes, journals, and family records who are tired of paying.
- **Business owners** with client notes mixed in with personal ones.
- **Anyone in between:** students, freelancers, caregivers, people who just want their notes somewhere they already use.

Plain language, one question at a time, and a suggested answer every time. Many users aren't technical, and some are nervous about losing years of notes.

## Principles

1. **Never delete the user's notes.** The plugin never calls an Evernote delete tool. Deleting is the user's own step, after the backup check.
2. **Backup before leaving.** The `.enex` export is the only copy with every attachment.
3. **Sensitive stays out of the wrong places.** Passwords, account and ID numbers, and private legal, medical, or family notes never go into a Claude Project, Claude's memory, a log, or a shared folder. Ask each time; default to a locked copy; offer a printable sheet; offer to delete the plugin's own copies after the user has moved them somewhere safe.
4. **Count everything, prove it at the end.** Survey totals are the yardstick for every later step.
5. **Stop anytime.** A short progress log (with consent) means the user can pick up tomorrow.
6. **Be honest about limits.** If a tier can't copy attachments, say so and point to the backup.
7. **Never paywall safety.** Sensitive-note protection, the backup check, and the cancel guide are in every version.
8. **Upsell at most once.** Mention paid versions only when the user asks for something their version doesn't include.

## The nine steps

Connect → Survey → Sort → Sensitive → Copy → Back up → Check → Cancel & celebrate → Clean up. Backup and check can happen first if the user wants to cancel today.

## Versions

| Version | Price | Idea |
|---|---|---|
| Escape Hatch | Free | Everything you need to escape safely, using the Evernote connector, with Claude-ready files as the destination |
| Side Door | $9 | The `.enex` backup as a source (all attachments), and Google Drive |
| Getaway Car | $18 | More destinations (Notion, Word/OneDrive, Markdown/Obsidian) and custom buckets |
| The Great Escape | $27 | Autopilot (Claude uses the computer while you talk from your phone), Apple Notes, Google Keep, Irons hand-off (beta) |

Each version is a full plugin with the same name, so installing a higher version simply replaces the lower one. A small `tier.md` file inside the plugin tells it which version is installed, so it offers only what's included.

## Lessons from the real escape (built into the skills)

- The Evernote connector returns notes in pages; never assume a list is complete until the last page.
- Attachments often can't be downloaded through the connector; the `.enex` backup has them all.
- Google Drive search results come in small pages too; a "missing" file is usually on the next page.
- A notebook with one note exports under the note's title, not "(1 note)".
- Empty notebooks can't be exported and don't need to be.
- For computer use: Screen Recording and Accessibility permissions need a full restart of Claude, which drops the chat's link to the computer; reopen the chat to relink. The computer must stay awake. Esc stops Claude.

## Not affiliated

Independent project. Not affiliated with, endorsed by, or sponsored by Evernote or its owner, or by Anthropic.
