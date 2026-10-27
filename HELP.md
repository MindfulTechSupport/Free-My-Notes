# Help

*Free My Notes · Mindful Tech Projects*

Quick answers to the things people run into most. You can also just ask the plugin: "help," or "how do I back up my [app]?"

## Getting started

### Which notes apps does it work with?

Evernote, Google Keep, Microsoft OneNote, Apple Notes, Notion, Zoho Notebook, Joplin, Simplenote, Bear, Standard Notes, Obsidian, UpNote, MyScript Notes (Nebo), and Zoom notes, plus most other apps that can export. Start a chat, say "free my notes," and tell it which app.

### Claude can't see my notes

- **Evernote, Notion, or Zoom:** these use a connector. In Claude, open **Settings → Connectors**, add the app, sign in, and allow access. Then start a new chat and say "free my notes."
- **Every other app:** the plugin walks you through the app's export, and you share the file with Claude (upload it, or connect its folder in the Claude desktop app).

### Nothing happens after installing

Start a brand-new chat. Existing chats may not pick up a new plugin. Then say "free my notes."

### Can I do this from my phone?

You can talk to it from your phone once it's installed, and copying can keep going while you drive. Installing the plugin and most apps' exports need a computer. The plugin keeps an "at your computer" list for those steps.

## Backups (exports) by app

The plugin has a full guide for each app; here's the short version:

| App | Where the export is |
|---|---|
| Evernote | Desktop app → Notebooks → ⋯ → Export notebook… → ENEX, one notebook at a time |
| Google Keep | takeout.google.com → Deselect all → tick Keep → Create export (emailed link, or save to Drive) |
| Notion | Settings → Export all workspace content → Markdown & CSV |
| Zoho Notebook | Settings → export all your Notebook data → HTML (emailed link) |
| Joplin | File → Export all → JEX |
| Simplenote | Export Notes (a zip) |
| Bear | Select all notes → File → Export Notes → TextBundle or Markdown |
| Standard Notes | Preferences → Backups → download a decrypted backup |
| Obsidian | Copy (or zip) your vault folder |
| UpNote | Export all notes as Markdown |
| MyScript Notes | Select notes → Export, one folder at a time (Word or PDF) |
| Zoom notes | One meeting at a time (notes as PDF, transcripts as text), or Zoom's connector |
| OneNote | OneNote for Windows: File → Export → Notebook (.onepkg), plus sections as PDF or Word |
| Apple Notes | No built-in bulk export: a Mac export app, PDFs one at a time, or The Great Escape's Autopilot |

Menus change; if yours looks different, tell the plugin what you see. Keep the export exactly as downloaded, plus a second copy somewhere else, before canceling anything.

## During the escape

### Some notes look missing

Before worrying: most "missing" notes are on a page of results that wasn't fetched yet, inside a stack or nested folder, empty, in the Trash, archived, locked, or a sensitive note you chose to skip. Say "check the counts" and the plugin re-counts and compares against the tracker.

### My PDFs and photos didn't come over

In the free version (Escape Hatch), attachments are listed in the tracker but may not be copied, because connectors often can't download them and big exports are slow to unpack in a chat. They are all in your app's backup, so nothing is lost. Side Door and up read the backup directly and pull every attachment out.

### Handwriting came out as pictures

That's normal for handwritten pages (MyScript notebooks, OneNote drawings, Apple Notes sketches). Typed or converted text comes through as text.

### Locked or encrypted notes

Unlock them in the app (and, for Standard Notes, download a decrypted backup), then export again. The plugin never asks for your passwords.

### I pressed Esc and Claude stopped (The Great Escape)

Esc is the stop button for Claude using your computer. Say "keep going" and it picks up where it left off.

### Claude stopped while my laptop was closed

Long jobs that use your computer (Autopilot, Google Keep) need the laptop open, plugged in, and awake. Reopen the chat in the Claude desktop app and say "keep going."

## Sensitive notes

- **What counts:** passwords, logins, account or card numbers, ID numbers, and private legal, medical, or family notes.
- **What happens:** the plugin asks you about each one. The default is a locked copy that never goes into a Claude Project, Claude's memory, or a shared folder.
- **The best home for passwords** is a password manager. Once you've moved them, say "clean up my sensitive notes" and the plugin deletes the copies it made, only after you confirm.
- **Remember the app's Trash.** After you delete notes in your app yourself, empty its Trash too.

## Canceling

Do the backup first. Many notes apps are free and have nothing to cancel (Google Keep, Simplenote, Joplin, Obsidian, Apple Notes, OneNote). For paid ones, cancel where you pay:
- **The app's website:** its account or billing settings.
- **Apple (iPhone or Mac App Store):** Settings → your name → Subscriptions → the app → Cancel.
- **Google Play:** Play Store → profile → Payments & subscriptions → Subscriptions → the app → Cancel.

## The backup service

- **What it does:** a fresh backup of your notes app every month, made in your own Claude and saved to your own Google Drive.
- **Needs:** a paid Claude plan (for scheduled tasks), and Free My Notes' backup plugin installed beside Free My Notes.
- **Automatic** for Evernote, Notion, and Zoom. For other apps, it reminds you each month and checks the export you drop in its Inbox folder.
- **Stop it:** say "stop my backups." Your backups stay where they are.

## Paid versions

- **Installing:** remove the older Free My Notes in **Customize → Plugins**, then upload the new `.plugin` file. Your progress log is kept separately, so the escape picks up where it left off.
- **Where to buy:** the [website](https://freemynotes.com/#pricing).
- **Lost your file?** Open the purchase email or your Patreon, Gumroad, or Lemon Squeezy library and download it again. For crypto purchases, [send feedback](../../issues/new?template=feedback.yml) with your payment ID (never your wallet keys or seed phrase).

## Your information

- **See what's saved:** "what do you know about me?"
- **Erase it:** "forget my escape." You'll be offered a copy first. This never touches your notes, your copies, or your backup.
- Nothing is sent to Mindful Tech Projects. See [PRIVACY.md](PRIVACY.md).

## Still stuck?

Say "send feedback" and describe what happened, or [open a feedback form](../../issues/new?template=feedback.yml). Posts there are public, so leave out anything private.
