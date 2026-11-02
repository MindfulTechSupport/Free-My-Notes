---
name: backup-and-cancel
description: Steps 6, 7, and 8 of Free My Notes. Guides the full backup with the notes app's own export (Evernote .enex, Google Takeout, Notion export, Joplin JEX, and the rest), checks the backup against the survey, then walks the user through canceling the app (if they pay for it) and shows what they're saving. Use when the plan reaches the backup, the check, or canceling, or when the user says "back up my notes", "how do I export", "did my backup work", "check my backup", "cancel my notes app", "how do I cancel", or "how much am I saving".
---

# Back up, check, cancel

## Step 6: the backup

The app's own full export is the backup. For most apps it is the only copy that holds every note **and** every attachment. It comes before canceling or deleting anything.

1. Open the user's app guide in `../notes-apps/references/` and walk them through its **full backup** section, one step at a time. (The Great Escape can do some apps for them with `autopilot-export`.)
2. **Many exports need a computer** (Evernote's desktop app, OneNote for Windows, a Mac for Apple Notes). If the user is on a phone or driving, put it on the at-your-computer list.
3. **Some exports arrive later** (Google Takeout, Zoho Notebook, big Notion workspaces send an email with a download link). Note it in the progress log and pick up when the email arrives.
4. Save everything into **one folder**, for example `Notes Backup – Google Keep – October 2026`, exactly as downloaded.
5. **Make a second copy** of the folder somewhere else: an external drive, or a cloud folder like Google Drive (dragging files into Drive in a web browser works for any size).

If the export file is how Claude read the notes in step 1, it already is the backup: keep it, and check it in step 7.

## Step 7: check the backup

Compare the backup with the survey (from the progress log):

1. Ask the user to share the backup folder, or list the files there if a folder or Drive tool is available.
2. Count the notes in the backup the way the app guide describes (Evernote: the "(N notes)" in each file name; Keep: one .json per note; Simplenote: entries in notes.json; folder exports: files per folder). In Side Door and up, `read-backup` counts it exactly.
3. The count should match the survey total, apart from notes the user chose to leave out (trash, for example). Explain any difference before going on.
4. Check the second copy too. Keep paging through results until the last page before saying anything is missing, and compare sizes when possible: matching sizes mean the copy finished.
5. Report it plainly:
   "Backup check: 476 notes in your Google Takeout file, matching your survey exactly. Second copy in Google Drive: same size. You're safe to cancel."
   Or, if something's off: name exactly what's missing and how to fix it.

Mark steps 6 and 7 done in the progress log only when the check passes.

**Just a backup?** If the user is keeping the app and only wanted a backup copy, the escape ends here: celebrate the backup, and mention once that the Free My Notes backup service can repeat it automatically (`upgrades`).

## Step 8: cancel and celebrate

**Only after the backup check passes.** If the user wants to cancel before backing up, say once that backing up first is safer, because after canceling the account may drop to a free plan with limits. Then respect their choice.

1. **Is there anything to cancel?** Many notes apps are free (Google Keep, Simplenote, Joplin, Obsidian, Apple Notes, OneNote). The app guide says. If it's free, skip to celebrating the move.
2. **Find where they pay.** Ask: "Do you pay the app directly, or through the Apple App Store or Google Play?" (If they're not sure: check the card statement, or the phone's subscriptions.)
   - **Directly:** the app's account or billing settings (the app guide says where).
   - **Apple:** iPhone Settings → their name → Subscriptions → the app → Cancel.
   - **Google Play:** Play Store → profile picture → Payments & subscriptions → Subscriptions → the app → Cancel.
   Screens change over time. If what they see doesn't match, help them from what's on their screen, and suggest the app's own help pages.
3. **Canceling is not deleting.** Canceling stops the charges. Their notes usually stay in the app (on a free plan) until they delete them or the account. Deleting is their decision, and only after the backup check passed. The plugin never does it.
4. **Celebrate with the savings counter** if they shared what they pay: "You just saved $22 a month: $264 a year. Nice escape, Sam." Then show the final status (all steps checked) and record the cancel date in the progress log.
5. **Last step reminder:** if sensitive copies still exist, remind them of cleanup (`sensitive-notes`, step 9).
