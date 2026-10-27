---
name: escape-help
description: Help and troubleshooting for Escape from Evernote. Use when the user says "help", "it's not working", "Claude can't see my Evernote", "the connector won't connect", "what does this notification mean", "my notes didn't all copy", "a file is missing", "send feedback", or seems confused about a step, a Claude notice, installing, or their data.
---

# Escape help

Answer the user's actual question first, in plain words, then offer the next step. Keep it short. If they're driving, give one spoken step at a time.

## Common problems

**Claude can't see my Evernote / no Evernote tools.**
The Evernote connector isn't added or isn't signed in. In Claude, open Settings → Connectors, add Evernote, sign in, and allow access. Then start a new chat and say "escape Evernote." If the connector is on but listing notebooks fails, try once more; Evernote's service sometimes hiccups. If it keeps failing, they can still escape with the `.enex` backup (Side Door and up read it directly).

**Some notes look missing.**
Before worrying: re-count with full paging (results come in pages), check stacks, and check whether the "missing" notes are empty notes, Trash, or notes the user chose to skip as sensitive. Compare against the tracker. Most "missing" notes turn out to be on a page that wasn't fetched yet.

**My attachments (PDFs, photos) didn't come over.**
In Escape Hatch, attachments are listed in the tracker but not copied, because Claude often can't download them through the connector. They're all inside the `.enex` backup. Side Door ($9) and up can read the backup and pull every attachment out.

**A file is missing from Google Drive (or another folder).**
Page through all results before deciding. Then compare file sizes; a matching size means the upload finished. Very big files can take a few minutes to finish uploading.

**The export (backup) won't work.**
It has to be the Evernote desktop app, not the website. Export one notebook at a time, and skip empty notebooks. See the backup steps in `backup-and-cancel`.

**I accidentally pressed Esc and Claude stopped (The Great Escape).**
That's the stop button for Claude using your computer. Say "keep going" and it picks up where it left off.

## Claude notices the user may see

These come from Claude itself, not this plugin.
- **"Allow Claude to use Evernote?" / connector permission:** approve it so the plugin can read your notes. You can remove the connector anytime after your escape.
- **"Claude saved a memory" or memory settings prompts:** the plugin only saves a short progress log (never note contents or passwords) and only if you agreed. See `my-escape-data`.
- **Computer-use permission prompts (The Great Escape):** approve them only if you asked Claude to drive your computer.

## Installing and updating

- Installing needs a computer: Claude desktop app or claude.ai → Customize → Plugins → upload the `.plugin` file (or add the marketplace `MindfulTechSupport/Escape-from-Evernote` for the free version).
- Upgrading to a paid tier: remove the older Escape from Evernote first, then upload the new file. The escape log is kept separately, so progress isn't lost.
- After installing, start a new chat and say "escape Evernote."

## Send feedback

When the user says "send feedback":
1. Ask what happened or what they'd like, in their own words.
2. Draft a short, friendly note with them. Remove anything private (no note contents, no names they wouldn't want public).
3. Give them the feedback link to post it themselves: https://github.com/MindfulTechSupport/Escape-from-Evernote/issues/new?template=feedback.yml
   Posts there are public. The plugin never sends anything on its own.
