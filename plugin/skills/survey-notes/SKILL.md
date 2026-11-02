---
name: survey-notes
description: Step 2 of Free My Notes. Counts every notebook (or folder, label, tag, or section) and every note in the user's notes app, through a connector or the app's export, and builds the survey the rest of the escape works from. Use when the plan reaches the survey step, or when the user asks "how many notes do I have", "what's in my notes", "list my notebooks", or "survey my notes".
---

# Survey the notes

The survey is the master list. Every later step (sorting, copying, the backup check) is checked against it, so be complete and exact.

Use the app's own word for notebooks (Keep: labels; Simplenote and Bear: tags; OneNote: notebooks and sections; Obsidian and Apple Notes: folders). See the app's guide in `../notes-apps/`.

## Through a connector (Evernote, Notion, Zoom)

1. **List every notebook** (Evernote: notebooks and the stacks they sit in; Notion: top-level pages and databases shared with Claude; Zoom: meetings with notes or summaries, by month).
2. **Count the notes in each one**, paging until the last page (see `../free-my-notes/references/lessons-learned.md`). Record the note count, the newest and oldest dates, how many have attachments, and how many look like web clips.
3. **Total it up** and check against an all-notes count where the app offers one. If they differ, find the gap before moving on (usually a notebook inside a stack, or a page that wasn't fetched).

## Through the app's export

1. **Open the export** (unzip it if needed) and find the notes: one file per note (Markdown, text, HTML, Word, PDF), or one data file holding them all (Google Keep's .json files, Simplenote's notes.json, Standard Notes' backup, Joplin's JEX). The app guide says which.
2. **Group them into notebooks** the way the app does (folders, first label, first tag), and count each group.
3. **Note anything unreadable**: locked or encrypted notes, handwriting saved as pictures, files Claude can't open. Count them separately.
4. In Side Door and up, `read-backup` does all of this in one pass and writes a manifest.

## Both ways

- **Spot empty notebooks** (0 notes). They need nothing; list them as "empty, skip."
- **Ask about Trash and archived notes** once: "Your app keeps deleted (and archived) notes separately. Want those too, or leave them?" Default: leave trashed notes, include archived ones.
- **Several apps:** survey each app separately and keep separate totals.

## Show the user

Short, scannable, biggest first. Then a one-line read on how long copying might take.

```
Your Google Keep: 4 labels with notes, 476 notes (plus 31 without a label)
• Recipes .............. 115
• Side Projects ......... 95
• Work .................. 56
• Family ................ 30
• …and 180 more without a label (show all?)
About 140 notes have pictures or files. Copying will take a while; I'll keep you posted.
```

In voice-friendly mode, say the totals and the top three only.

## Save

Write the notebooks table and totals into the progress log (`../free-my-notes/references/progress-log-format.md`), mark the survey step done, and move on to sorting.

## Big accounts

For more than about 1,000 notes, tell the user before you start that the survey alone may take several minutes, and give a progress line every few notebooks.
