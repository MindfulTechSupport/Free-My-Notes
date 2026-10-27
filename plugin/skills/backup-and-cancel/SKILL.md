---
name: backup-and-cancel
description: Steps 6, 7, and 8 of Escape from Evernote. Guides the full .enex backup from the Evernote desktop app, checks the backup against the survey, then walks the user through canceling their Evernote subscription and shows what they're saving. Use when the escape reaches the backup, the check, or canceling, or when the user says "back up my Evernote", "how do I export", "did my backup work", "check my backup", "cancel Evernote", "how do I cancel", or "how much am I saving".
---

# Back up, check, cancel

## Step 6: the backup (.enex export)

The `.enex` export is the only copy that holds every note **and** every attachment. It comes before canceling or deleting anything.

**It needs a computer** with the Evernote desktop app (Mac or Windows). The Evernote website can't export. If the user is on a phone or driving, put it on the at-your-computer list.

Walk them through it, one step at a time (The Great Escape tier can do this for them with `autopilot-export`):

1. Make a folder for the backup, for example on the Desktop: **Evernote Export – October 2026**.
2. Open the **Evernote desktop app** and go to **Notebooks**.
3. If notebooks are grouped in **stacks**, open each stack to see its notebooks.
4. For each notebook that has notes: open its **⋯** menu (or right-click it) → **Export notebook…** → choose **ENEX** → leave the boxes checked (note title, dates, tags, author, source URL…) → **Export** → save into the backup folder.
5. Skip empty notebooks (they can't be exported and don't need to be).
6. When all are done, **make a second copy** of the folder somewhere else: an external drive, or a cloud folder like Google Drive (dragging the files into Drive in a web browser works for any size).

Tips to share only if they come up (more in `../escape-plan/references/lessons-learned.md`):
- A notebook with only one note gets saved under the note's title.
- Some characters (like `/` and `#`) are dropped from file names.
- Big notebooks take longer and make big files; that's normal.

## Step 7: check the backup

Compare the backup with the survey (from the escape log):

1. Ask the user to share the backup folder, or list the files there if a folder or Drive tool is available. Otherwise ask them to read the file names and the "(N notes)" in each name.
2. Check that every notebook with notes has a file, and add up the note counts. They should match the survey total exactly.
3. Notebooks with one note won't show "(1 note)" in the file name; match them by the note's title.
4. For the second copy (for example in Google Drive), check the files there too. Keep paging through results until the last page before saying anything is missing, and compare sizes when possible: matching sizes mean the upload finished.
5. Report it plainly:
   "Backup check: 32 files, 476 notes. Matches your survey exactly. Second copy in Google Drive: all 32 files, sizes match. You're safe to cancel."
   Or, if something's off: name exactly what's missing and how to fix it.

Mark steps 6 and 7 done in the escape log only when the check passes.

## Step 8: cancel and celebrate

**Only after the backup check passes.** If the user wants to cancel before backing up, say once that backing up first is safer: after canceling, the account drops to Evernote's free plan, whose limits can change. Then respect their choice.

1. **Find where they pay.** Ask: "Do you pay Evernote directly, or through the Apple App Store or Google Play?" (If they're not sure: check for an Evernote charge on the card statement, or look in their phone's subscriptions.)
   - **Evernote directly:** cancel in their Evernote account settings on the Evernote website, under billing or subscription.
   - **Apple:** on iPhone, Settings → their name → Subscriptions → Evernote → Cancel.
   - **Google Play:** Play Store → profile picture → Payments & subscriptions → Subscriptions → Evernote → Cancel.
   Screens change over time. If what they see doesn't match, help them find it from what's on their screen, and suggest Evernote's own help pages.
2. **Canceling is not deleting.** Canceling stops the charges. Their notes stay in Evernote (on the free plan) until they delete them or the account. Deleting the notes or the account is their decision, and only after the backup check passed. The plugin never does it.
3. **Celebrate with the savings counter** if they shared what they pay: "You just saved $22 a month: $264 a year. Nice escape, Sam." Then show the final status (all steps checked) and record the cancel date in the escape log.
4. **Last step reminder:** if sensitive copies still exist, remind them of cleanup (`sensitive-notes`, step 9).
