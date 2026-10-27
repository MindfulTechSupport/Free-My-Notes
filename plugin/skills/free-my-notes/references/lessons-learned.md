# Lessons learned from real escapes

Most of these came from the first full escape (476 notes, 32 notebooks, October 2026). Check here, and the app's guide in `../../notes-apps/references/`, before improvising.

## Any notes app

- **Exports are the backup.** Keep the file exactly as downloaded, plus a second copy, before anything is canceled or deleted.
- **Pick the most complete format.** Joplin's JEX keeps tags and dates that its Markdown export drops; Standard Notes must be a decrypted backup; Zoho Notebook's HTML is readable where its ZNote format isn't.
- **Some exports arrive by email** (Google Takeout, Zoho Notebook, big Notion workspaces). Record "waiting for export email" in the progress log and pick up when it arrives.
- **"Notebooks" differ by app.** Keep has labels, Simplenote and Bear have tags, OneNote has sections, Obsidian and Apple Notes have folders. A note with several labels or tags goes under the first one and keeps the rest as tags.
- **Notion file names end in a long code** (`Recipes 1a2b3c…`). It isn't part of the title.
- **Handwriting comes out as pictures** (MyScript notebooks, OneNote drawings). Copy them as pages and say so.
- **Count from the export, not from memory.** One .json per Keep note, one entry per Simplenote note in notes.json, one file per note in folder exports.

## Reading Evernote through the connector

- **List notebooks first** (search notebooks), then list each notebook's notes with a notebook query such as `notebook:"Side Projects"`.
- **Page through results.** Ask for the maximum page size (100) and keep going with the start index until the result says it's the last page. Notebooks with more than 100 notes need two or more pages.
- **Snippets are short.** Search results show a snippet, not the whole note. For any note longer than its snippet, or with an empty snippet (usually attachment-only notes), fetch the full note.
- **Notes come back as ENML** (Evernote's HTML). Convert to plain text or Markdown: keep headings, lists, checkboxes, tables, and links; drop styling.
- **Attachments are listed but may not download.** The connector gives a link for each attachment, but the place Claude runs often can't reach Evernote's file storage. Don't promise attachments from the connector. Record each attachment's name, type, and size in the tracker, and point to the `.enex` backup, which contains every attachment (Side Door and up can read it).
- **Web clips can be huge.** A clipped web page can be thousands of words of page clutter. Copy the title, source link, and a short description, and say the full clip is in the `.enex` backup.
- **Stacks are not notebooks.** A stack is a group of notebooks. Survey the notebooks inside it.
- **Empty notebooks exist.** Note them in the survey; there's nothing to copy or export.
- **Trash is separate.** The default search leaves out trashed notes. Ask the user whether they want their Trash too, before searching it.
- **Retry once.** "Service unavailable" or "resource exhausted" errors usually pass on a single retry. If it fails twice, pause and tell the user.

## Checking your own work

- **Don't trust one page of results.** When checking that files arrived (in Google Drive, a folder, anywhere), keep paging until there are no more pages before saying anything is missing. In the first escape, three files looked missing only because the check stopped after the first page.
- **Match by size when you can.** A file whose size matches the original exactly arrived completely.
- **Count notes, not just files.** Add up the note counts per notebook and compare with the survey total.

## Evernote's .enex backup (desktop app)

- Export is only in the **desktop app** (Mac or Windows), not the website. Free Evernote accounts can still export, so canceling the subscription doesn't block the backup, but do it first anyway.
- Export one notebook at a time: right-click (or ⋯) a notebook → **Export notebook…** → **ENEX** → keep the attributes checked (title, dates, tags, author, source URL) → **Export** → choose where to save.
- A notebook with **one note** is saved under the note's title, not the notebook's name.
- File names **drop characters** like `/` and `#` ("Trisha/Tessa…" became "TrishaTessa…", "TRAVEL Acct #'s" became "TRAVEL Acct 's").
- **Empty notebooks** can't be exported; skip them.
- Big notebooks make big files (one 115-note notebook was 111 MB). Some upload tools have size limits (for example 10 MB per upload through a browser extension); dragging the file into Google Drive in a browser works for any size.
- Save everything into one folder named something like "Evernote Export – October 2026", and keep a second copy somewhere else (another drive, a cloud folder) before deleting anything.

## Google Drive (paid tiers)

- Creating a Google Doc from HTML keeps headings, lists, links, and tables.
- A folder with "inherited permissions" turned off is visible only to the owner. Use that for sensitive notes and backups, then confirm with a permissions check.
- Drive searches return results in pages; keep paging.
- The Google Drive folder synced on a computer may belong to a different Google account than the one connected to Claude. Check which account before copying files into it.

## The computer (The Great Escape)

- Computer use must be turned on in the Claude desktop app, and macOS must give Claude **Screen Recording** and **Accessibility** permission. A new Screen Recording permission only works after Claude is fully quit (⌘Q) and reopened, and reopening drops the chat's link to the computer: open the chat again in the desktop app to relink.
- **If the computer goes to sleep**, Claude loses the connection. Plug it in and turn off sleep while plugged in, and keep the lid open.
- **Pressing Esc stops Claude's control** of the computer. Tell the user not to press Esc unless they want Claude to stop.
- In Evernote's notebook list, menus near the bottom of the window get cut off. Type the notebook name in **Find Notebooks** so the notebook is the top row, then open its ⋯ menu.
- The Save window may not show in Claude's screenshots; pressing Return accepts the default name and folder.
- The default notebook's menu is shorter than the others; look before clicking.
