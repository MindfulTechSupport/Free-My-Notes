# Evernote

Tested end to end in the first real escape (476 notes, 32 notebooks, October 2026).

## How Claude gets the notes
- **The Evernote connector.** In Claude: Settings → Connectors → add Evernote, sign in, allow access. Claude lists notebooks, pages through each notebook's notes, and reads each note. Attachments are listed but often can't be downloaded this way.
- **Or the backup (.enex files).** Side Door's `read-backup` reads them directly, attachments included.

## The full backup (.enex)
Needs a computer with the **Evernote desktop app** (Mac or Windows). The website can't export.
1. Make a folder, for example on the Desktop: `Evernote Export – October 2026`.
2. Open the Evernote desktop app → **Notebooks**. Open each **stack** to see the notebooks inside it.
3. For each notebook with notes: its **⋯** menu (or right-click) → **Export notebook…** → **ENEX** → leave the boxes checked (title, dates, tags, author, source URL) → **Export** → save into the folder.
4. Skip empty notebooks (they can't be exported and don't need to be).
5. Make a second copy of the folder somewhere else (an external drive, or drag it into Google Drive in a web browser).
The Great Escape's `autopilot-export` can do this for the user.

## What's in it
One .enex file per notebook, named `Notebook (N notes).enex`, holding every note, tag, date, and attachment. A notebook with one note is named after the note. Characters like `/` and `#` are dropped from file names. Big notebooks make big files (one 115-note notebook was 111 MB).

## Notebooks are called
Notebooks, grouped into stacks. Tags too.

## Canceling
Ask where they pay:
- **Evernote's website:** sign in on evernote.com, open account settings, and look for Billing or Subscription.
- **Apple:** iPhone Settings → their name → Subscriptions → Evernote → Cancel.
- **Google Play:** Play Store → profile picture → Payments & subscriptions → Subscriptions → Evernote → Cancel.
Canceling drops the account to Evernote's free plan; the notes stay until the user deletes them.

## Watch out for
- Encrypted text inside notes can't be read until it's decrypted in Evernote.
- Web clips can be thousands of words of page clutter; copy the title, link, and a short summary.
- The default notebook's ⋯ menu is shorter than the others.
