# Joplin

## How Claude gets the notes
The backup.

## The full backup
1. In the Joplin desktop app: **File → Export all**.
2. Choose **JEX – Joplin Export File**. It keeps everything: notebooks, tags, dates, and attachments.
3. Save it in a backup folder, plus a second copy.

Markdown export also works and is easy to read, but it drops tags and dates, so prefer JEX. (Joplin forum, "Exporting all data should be way easier.")

## What's in it
A JEX file is an archive of Joplin's own text files: one per note, notebook, tag, and attachment, with the details (dates, which notebook) written at the bottom of each file. Side Door's `read-backup` turns it back into notebooks and notes. In Escape Hatch, ask for a Markdown export too if Claude has to read it directly.

## Notebooks are called
Notebooks (which can be nested), plus tags.

## Canceling
Joplin is free. If the user pays for Joplin Cloud, they cancel in their Joplin Cloud account.

## Watch out for
- End-to-end encrypted sync doesn't affect the export; exports come out readable.
- Conflict notes (copies Joplin made during sync problems) may appear; count them and ask.
