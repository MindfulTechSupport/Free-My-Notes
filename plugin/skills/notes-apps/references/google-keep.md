# Google Keep

## How Claude gets the notes
The backup. Keep has no connector, so the user downloads everything with **Google Takeout**, then shares the file.

## The full backup (Google Takeout)
1. Go to **takeout.google.com** and sign in to the Google account that has the notes.
2. Click **Deselect all**, then scroll down and tick **Keep** only.
3. **Next step.** Choose how to receive it: **Send download link via email**, or **Add to Drive** (handy: Claude can then reach it through the Google Drive connector). Leave the file type as .zip.
4. **Create export.** Google prepares it; small accounts take minutes, big ones longer. An email arrives when it's ready.
5. Download the .zip (or find it in Drive) and keep it in a backup folder, plus a second copy.

## What's in it
Inside the zip, a `Takeout/Keep` folder with, for each note, a .json file (title, text or checklist items with ticks, labels, created and edited times, pinned, archived, trashed) and an .html copy, plus any attached images, drawings, and recordings as files.

## Notebooks are called
Keep has no notebooks. It has **labels**. Treat each label as a notebook (a note with several labels goes under its first label and keeps the rest as tags), and unlabeled notes as "Keep (no label)".

## Canceling
Keep is free; there's nothing to cancel. (Google One is storage for the whole Google account, not just Keep. Only cancel it if the user doesn't need the space.)

## Watch out for
- Archived notes are included and marked; ask whether to treat them like the others.
- Trashed notes may be included and marked; leave them out unless the user asks.
- Reminders and collaborators don't carry over to other apps.
