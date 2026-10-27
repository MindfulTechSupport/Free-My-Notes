---
name: claude-ready
description: Step 5 of Free My Notes for the Claude-ready destination (included in every tier). Turns the user's notes into tidy Markdown files, one per notebook and bucket, plus a tracker, ready to add to a Claude Project's knowledge. Use when the escape reaches copying and the destination is Claude, or when the user says "make my notes Claude-ready", "put my notes in a Claude Project", or "give me my notes as files".
---

# Claude-ready files

The goal: every non-sensitive note, readable by Claude, organized so the user can drop a whole topic into a Claude Project and start working with it.

## What to make

In one output folder named `Free My Notes – <App> – <Month YYYY>` (for example `Free My Notes – Google Keep – October 2026`):

1. **One Markdown file per notebook, inside a folder per bucket:**
   ```
   Free My Notes – Google Keep – October 2026/
     Work/
       Side Projects.md
       Clients.md
     Personal/
       Recipes.md
     Not sure/
       Not sure – to review.md
     START HERE.md
     Notes tracker.csv
   ```
   Notes from a mixed notebook go into the matching bucket's folder, in a file named after the notebook.
2. **Inside each file**, one section per note, oldest to newest or as the user prefers:
   ```markdown
   # Side Projects
   *From Google Keep · 95 notes · copied 2026-10-26*

   ---
   ## Booth checklist for the weekend market
   *Created 2025-10-25 · Updated 2026-10-25 · Tags: market, ideas*

   Tent, two tables, card reader, change box, price signs…

   *Attachment: booth-layout.jpg (image, 1.2 MB). Full copy in your Google Takeout backup.*
   ```
   - Convert the app's formatting to Markdown (Evernote's ENML, HTML exports, Keep checklists, Word files): headings, bullet and numbered lists, checkboxes (`- [ ]` / `- [x]`), tables, links. Drop colors and fonts. Files that are already Markdown (Obsidian, Bear, Joplin, Notion) keep their formatting.
   - Keep the note's created and updated dates and tags in the italic line under the title.
   - Attachments: one italic line per attachment with name, type, and size, pointing to the backup.
   - Web clips: title, source link, and a 1–3 sentence description; say the full clip is in the backup.
   - Empty notes: keep the title with "(empty note)" so the count still matches.
3. **Split big files.** If a file would go over about 150 KB of text, split it: `Sam's notebook (part 1 of 3).md`. Smaller files work better in a Project.
4. **`Notes tracker.csv`** with one row per note, including sensitive ones (title and decision only):
   `Note title, Notes app, Notebook, Stack, Bucket, Why, Created, Updated, Tags, Attachments, Attachment details, File, Sensitive choice, Your notes`
5. **`START HERE.md`**: what's in the folder, counts per bucket, how to add a topic to a Claude Project (below), and a reminder that the app's own backup is the complete copy.
6. **Sensitive notes** marked "Locked copy" go only into the separate sensitive file described in `sensitive-notes`, never into these folders.

## Making the files

Use whatever file tools are available here:
- **Claude desktop app with a folder connected:** write the folder there, and tell the user where it is.
- **claude.ai or the Claude app:** create the files and hand them back as downloads. For many files, put them in one `.zip` named `Free My Notes – Google Keep – October 2026.zip`.
- If there's no way to create files here, say so, and offer to paste one notebook at a time into the chat as a fallback.

Work notebook by notebook. After each notebook, update the progress log ("Side Projects: 95/95 copied") and, every few notebooks, give a one-line progress update.

## Getting them into a Claude Project

Tell the user, in plain steps:
1. In Claude, create a Project for the topic (for example "Side Projects"), or open one you already have.
2. Add the matching file(s) to the Project's knowledge.
3. Start a chat inside that Project and ask about your notes ("Which of my side project ideas could I start this month?").

Suggest one Project per big topic rather than one giant Project for everything, and keep work and personal Projects apart (better still, separate Claude accounts for work and personal).

## Check before calling it done

- Count the notes in the files plus the skipped and locked sensitive notes. The total must equal the survey count. If it doesn't, find the difference before marking the step done.
- Open one file per bucket and skim it for formatting problems.
- Mark the copy step done in the progress log with the counts.
