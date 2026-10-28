---
name: notes-help
description: Help and troubleshooting for Free My Notes. Use when the user says "help", "it's not working", "Claude can't see my notes", "the connector won't connect", "my export won't open", "what does this notification mean", "my notes didn't all copy", "a file is missing", "send feedback", or seems confused about a step, a Claude notice, installing, or their data.
---

# Free My Notes help

Answer the user's actual question first, in plain words, then offer the next step. Keep it short. If they're driving, give one spoken step at a time. For anything about one app's export, open its guide in `../notes-apps/references/`.

## Common problems

**Claude can't see my notes / no connector tools.**
For Evernote, Notion, or Zoom: the connector isn't added or isn't signed in. In Claude, open Settings → Connectors, add it, sign in, and allow access, then start a new chat and say "free my notes." If listing notes fails once, try again; services sometimes hiccup. If it keeps failing, use the app's export instead (every app has a guide).

**My export won't open, or Claude can't read it.**
Check the app guide for the right format (for example JEX for Joplin, decrypted for Standard Notes, HTML for Zoho Notebook, Markdown or Word rather than the app's own format). Big exports may be too large to upload in one go: connect the folder in the Claude desktop app, upload in parts, or use Side Door's `read-backup`.

**I haven't gotten the export email.**
Google Takeout, Zoho Notebook, and big Notion workspaces email a link when the export is ready. Big accounts can take hours. Check spam, and the email address on the account.

**Some notes look missing.**
Before worrying: re-count with full paging (results come in pages), check stacks and nested folders, and check whether the "missing" notes are empty, in the Trash, archived, locked, or ones the user chose to skip as sensitive. Compare against the tracker. Most "missing" notes turn out to be on a page that wasn't fetched yet.

**My attachments (PDFs, photos) didn't come over.**
In Escape Hatch, attachments are listed in the tracker but may not be copied, because connectors often can't download them and big exports are slow to unpack in a chat. They're all in the app's backup. Side Door ($9) and up pull every attachment out.

**Handwriting came out as pictures.**
That's normal for handwritten pages (MyScript Notes, OneNote drawings, Apple Notes sketches). Claude can look at them, but they copy as pages. Typed or converted text comes through as text.

**A file is missing from Google Drive (or another folder).**
Page through all results before deciding. Then compare file sizes; a matching size means the upload finished. Very big files can take a few minutes.

**I accidentally pressed Esc and Claude stopped (The Great Escape).**
That's the stop button for Claude using your computer. Say "keep going" and it picks up where it left off.

## Claude notices the user may see

These come from Claude itself, not this plugin.
- **Connector permission prompts:** approve them so the plugin can read your notes. You can remove a connector anytime after your escape.
- **"Claude saved a memory" or memory settings prompts:** the plugin only saves a short progress log (never note contents or passwords) and only if you agreed. See `my-notes-data`.
- **Computer-use permission prompts (The Great Escape):** approve them only if you asked Claude to use your computer.
- **Scheduled task prompts (backup service):** approve them only if you set up automatic backups.

## Installing and updating

- Installing needs a computer: Claude desktop app or claude.ai → Customize → Plugins → upload the `.plugin` file (or add the marketplace `MindfulTechSupport/Free-My-Notes` for the free version).
- Upgrading to a paid tier: remove the older Free My Notes first, then upload the new file. The progress log is kept separately, so progress isn't lost.
- After installing, start a new chat and say "free my notes."

## Send feedback

When the user says "send feedback":
1. Ask what happened or what they'd like, in their own words.
2. Draft a short, friendly note with them. Remove anything private (no note contents, no names they wouldn't want public).
3. Give them the feedback link to post it themselves: https://github.com/MindfulTechSupport/Free-My-Notes/issues/new?template=feedback.yml
   Posts there are public. The plugin never sends anything on its own.
