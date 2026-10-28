---
name: notes-apps
description: Guides for each notes app Free My Notes supports (Evernote, Google Keep, Notion, Zoho Notebook, Joplin, Simplenote, Bear, Standard Notes, Obsidian, UpNote, MyScript Notes / Nebo, Zoom notes, OneNote, Apple Notes, and others) - how Claude gets the notes, how to make a full backup with the app's own export, what the backup contains, and how to cancel. Use at step 1 of an escape, for the backup and cancel steps, or when the user asks "how do I back up my Google Keep", "export my OneNote", "get my notes out of Joplin", "how do I download my Zoom notes", or "can you help me leave [app]".
---

# Notes app guides

Every notes app hides its export in a different place. Before step 1 of an escape, open the guide for the user's app and follow it. Each guide covers the same four things:

1. **How Claude gets the notes** (a connector, or the app's export file).
2. **The full backup**: the app's own export, step by step.
3. **What's in the backup**, and what Claude can read from it.
4. **Canceling**: where people pay, or "nothing to cancel" for free apps.

| App | How Claude gets the notes | The backup | Guide |
|---|---|---|---|
| Evernote | Evernote connector, or the backup | .enex files from the desktop app | `references/evernote.md` |
| Google Keep | The backup | Google Takeout download | `references/google-keep.md` |
| Notion | Notion connector, or the backup | Markdown & CSV export | `references/notion.md` |
| Zoho Notebook | The backup | HTML export, emailed link | `references/zoho-notebook.md` |
| Joplin | The backup | JEX file (keeps everything) | `references/joplin.md` |
| Simplenote | The backup | Zip with notes.json | `references/simplenote.md` |
| Bear | The backup | Markdown or TextBundle export | `references/bear.md` |
| Standard Notes | The backup | Decrypted backup file | `references/standard-notes.md` |
| Obsidian | The vault folder itself | A copy of the vault | `references/obsidian.md` |
| UpNote | The backup | Markdown or HTML export | `references/upnote.md` |
| MyScript Notes (Nebo) | The backup | Word, text, or PDF exports, one folder at a time | `references/myscript-notes.md` |
| Zoom notes | Zoom's connector, or downloads | One meeting at a time | `references/zoom.md` |
| OneNote | PDF or Word exports | OneNote Package (.onepkg) | `references/onenote.md` |
| Apple Notes | PDFs, a Mac export app, or Autopilot | No built-in bulk export | `references/apple-notes.md` |
| Anything else | The backup | Whatever the app offers | `references/other-apps.md` |

## Rules for every app

- **Menus change.** The steps in each guide were right when written. If what the user sees doesn't match, help them from what's on their screen (ask them to describe it, or look at a screenshot they share), and suggest the app's own help pages.
- **Ask for the most complete format.** When an app offers several, pick the one that keeps the most: attachments, dates, tags, and folders. Each guide says which.
- **The export is the backup.** Keep the original file exactly as downloaded, in one folder (for example `Notes Backup – Google Keep – October 2026`), plus a second copy somewhere else before anything is canceled or deleted.
- **Reading the backup in Escape Hatch:** the user shares the file (upload it here, or connect its folder in the Claude desktop app). Claude opens it with the tools available (unzip, then read the Markdown, text, HTML, or JSON). This works well for small and medium exports. Very large exports, and pulling every attachment out, are what Side Door's `read-backup` skill is for.
- **Locked or encrypted notes** (Evernote's encrypted text, Apple Notes locked notes, an encrypted Standard Notes backup) can't be read until the user unlocks them in the app. Count them and tell the user; never ask for their passwords.
- **Trash:** most apps leave trashed notes out of the export, or mark them. Ask once whether the user wants trashed notes too. Default: leave them.
- **Never call an app's delete tools**, through a connector or on screen.
