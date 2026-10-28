# Design notes — Free My Notes 1.0.0
*Mindful Tech Projects · 2026-10-27*

## Where it came from

The founder moved his own paid notes app (Evernote) out with Claude: 476 notes in 32 notebooks, sorted into work and personal, sensitive notes kept in restricted folders, every notebook exported and backed up twice, and the subscription canceled ($22 a month saved). Free My Notes turns that escape into a guided plugin, and widens it to the notes apps people actually use.

## Why "Free My Notes" and not an app's name

A product name that contains another company's app name suggests a connection that doesn't exist, and some app makers' trademark rules forbid it. Free My Notes names no app. App names appear only to say which apps it works with, with credit to their owners.

## Who it's for

- **Everyday people** with years of recipes, journals, and family records.
- **Business owners** with client notes mixed in with personal ones.
- **People who just want a backup** they control, without leaving their app.

Plain language, one question at a time, and a suggested answer every time.

## Principles

1. **Never delete the user's notes.** The plugin never calls a notes app's delete tools. Deleting is the user's own step, after the backup check.
2. **Backup before leaving.** The app's full export is usually the only copy with every attachment.
3. **Sensitive stays out of the wrong places.** Passwords, account and ID numbers, and private legal, medical, or family notes never go into a Claude Project, Claude's memory, a log, or a shared folder. Ask each time; default to a locked copy; offer a printable sheet; offer to delete the plugin's own copies after the user has moved them somewhere safe.
4. **Count everything, prove it at the end.**
5. **Stop anytime.** A short progress log (with consent) lets the user pick up tomorrow.
6. **Be honest about limits.** Some apps make leaving hard (Apple Notes has no bulk export; Zoom exports one meeting at a time). Say so, and offer the best path.
7. **Never paywall safety.** Every app's backup guide, sensitive-note protection, the backup check, and the cancel guide are in every version.
8. **Upsell at most once.**

## Supported apps and how Claude reaches them

| App | Access | The backup |
|---|---|---|
| Evernote | Connector, or the backup | .enex per notebook |
| Google Keep | Backup | Google Takeout |
| Notion | Connector, or the backup | Markdown & CSV export |
| Zoho Notebook | Backup | HTML export |
| Joplin | Backup | JEX |
| Simplenote | Backup | Zip with notes.json |
| Bear | Backup | TextBundle or Markdown |
| Standard Notes | Backup | Decrypted backup |
| Obsidian | The vault folder | A copy of the vault |
| UpNote | Backup | Markdown export |
| MyScript Notes | Backup | Word, text, or PDF per folder |
| Zoom notes | Connector, or downloads | One meeting at a time |
| OneNote | PDF or Word exports | .onepkg |
| Apple Notes | A Mac export app, PDFs, or Autopilot | No built-in bulk export |

## The nine steps

Get access → Survey → Sort → Sensitive → Copy → Back up → Check → Cancel & celebrate → Clean up. "Just a backup" stops after the check.

## Versions

| Version | Price | Idea |
|---|---|---|
| Escape Hatch | Free | Everything needed to leave any app safely, with Claude-ready files as the destination |
| Side Door | $9 | Reads any app's backup in one pass, attachments included; Google Drive |
| Getaway Car | $18 | More destinations (Notion, Word/OneDrive, Markdown/Obsidian) and custom buckets |
| The Great Escape | $27 | Autopilot, Apple Notes and Google Keep as destinations, Irons hand-off (beta) |
| Backup service | $1 a month | A monthly backup in the user's own Claude, saved to their own storage |

Each version is a full plugin with the same name, so installing a higher version replaces the lower one. The backup service is its own small plugin that sits beside any version.

## Lessons from the real escape (built into the skills)

- Connectors return notes in pages; never assume a list is complete until the last page.
- Attachments often can't be downloaded through a connector; the app's backup has them all.
- Drive search results come in small pages too; a "missing" file is usually on the next page.
- Exports differ: pick the most complete format (Joplin JEX over Markdown, Standard Notes decrypted, Zoho HTML over ZNote).
- For computer use: Screen Recording and Accessibility permissions need a full restart of Claude, which drops the chat's link to the computer; reopen the chat to relink. The computer must stay awake. Esc stops Claude.

## Not affiliated

Independent project. Not affiliated with, endorsed by, or sponsored by the makers of any notes app it works with, or by Anthropic.
