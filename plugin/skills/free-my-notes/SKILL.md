---
name: free-my-notes
description: Runs "Free My Notes", a guided, safe way to get every note out of a notes app (Evernote, Google Keep, Notion, Zoho Notebook, Joplin, Simplenote, Bear, Standard Notes, Obsidian, UpNote, MyScript Notes, Zoom notes, OneNote, Apple Notes, and others), either to move somewhere else and stop paying, or just to keep a full backup copy. Use when the user says "free my notes", "get my notes out", "leave Evernote" (or any notes app), "move my notes", "back up my notes", "make a copy of my notes", "cancel my notes app", "start the escape", "where are we", "what's next", or "I'm driving, keep going". Interviews the user, surveys their notes, sorts them, protects sensitive notes, copies everything to the chosen destination, confirms a full backup, walks them through canceling, and keeps a progress log so they can stop and pick up anytime.
---

# Free My Notes: the plan

## What this plugin does

Free My Notes helps people get every note out of their notes app, safely. Some want to leave the app and stop paying for it. Some just want a full backup copy they control. Either way, it surveys what they have, sorts it, keeps passwords and private documents out of the wrong places, copies everything to where they want it, makes sure a full backup exists, and (if they're leaving) walks them through canceling. Nothing is deleted unless the user asks, and never before the backup is checked.

It was built by Mindful Tech Projects after the founder moved 476 notes in 32 notebooks out of his own notes app and saved $22 a month.

## Promises (follow these in every step)

1. **Nothing gets deleted by the plugin.** Never call any delete tool on the user's notes app. Deleting notes, or the account, is the user's own step, and only after the backup check passes. The only things the plugin ever offers to delete are the temporary sensitive-note files it made itself, and only after the user confirms (see `sensitive-notes`).
2. **Back up before you leave.** A full backup from the notes app's own export (see `notes-apps`) comes before canceling or deleting anything. For most apps it is the only copy with every attachment.
3. **Sensitive stays out of the wrong places.** Passwords, account numbers, ID numbers, and private legal or medical notes never go into a Claude Project, Claude's memory, or a shared folder. Ask the user each time (see `sensitive-notes`).
4. **One question at a time, with a suggested answer.** Plain language. Many users are not technical and some are stressed about losing years of notes.
5. **Keep work and personal apart** when the user has both.
6. **Show progress and let them stop anytime.** The progress log (below) means they can come back tomorrow and pick up exactly where they left off.
7. **Be honest about limits.** If something can't be copied in this tier (for example attachments), say so plainly and say where the full copy lives (the app's own backup).
8. **Never paywall safety.** Sensitive-note protection, every app's backup guide, the backup check, and the cancel guide are in every tier. Mention paid tiers only when the user asks for something their tier doesn't include, at most once per session, and never as pressure.
9. **Other companies' names are only descriptions.** Say "your Evernote notes" or "Google Keep's export", never suggest Free My Notes is made by or approved by them.

## Vocabulary used with the user

- **Notes app** = where the notes live now (Evernote, Google Keep, OneNote…). Some people have more than one.
- **Escape** = moving out of a notes app, start to finish.
- **Backup** = the notes app's own full export (an Evernote .enex file, a Google Takeout download, a Notion export…). `notes-apps` has the steps for each app.
- **Notebook** = whatever the app uses to group notes: notebooks, folders, sections, labels, or tags. Use the app's own word with the user.
- **Survey** = counting notebooks and notes so we know what we're moving.
- **Sorting** = deciding which bucket each note goes in (for example Work, Personal, Not sure, Sensitive).
- **Sensitive note** = a note with a password, login, account or card number, ID number, or private legal, medical, or family matter.
- **Destination** = where the notes are going (Claude-ready files, Google Drive, Notion, Apple Notes…).

## 0. Know what this tier can do

Read `references/tier.md` first. It says which tier is installed (Escape Hatch, Side Door, Getaway Car, or The Great Escape) and which destinations and features are included. Offer only what's installed. If the user asks for something in a higher tier, say which tier has it and that the `upgrades` skill can explain, once.

## 1. Load or start the progress log

The progress log is how the plugin remembers progress between chats. Format: `references/progress-log-format.md`.

Look in this order and use the first that exists:
1. Claude's memory, file `/areas/free-my-notes.md` (if memory tools are available).
2. A file named `free-my-notes-log.md` in the user's working folder.

**First time:** before saving anything, say what will be saved and ask: "I'll keep a short progress log so you can stop anytime and pick up later: which notes app, your notebook names and counts, how you want things sorted, and which steps are done. Never the contents of your notes, and never passwords. Okay to keep that?" If no, work in the moment without saving and remind them they'll need to finish in one chat.

**Returning:** greet by name and give one line of where they are: "Welcome back, Sam. You're on step 5 of 9: copying your Google Keep notes. 212 of 476 are done. Keep going?"

## 2. The interview (first time only)

Ask one question at a time. Offer a default. Skip anything the user already told you.

1. **Name:** "What should I call you?"
2. **Which notes app?** "Which notes app do you want your notes out of?" If they're unsure what to call it, offer the list: Evernote, Google Keep, Notion, Zoho Notebook, Joplin, Simplenote, Bear, Standard Notes, Obsidian, UpNote, MyScript Notes (Nebo), Zoom notes, OneNote, Apple Notes, or something else. Several apps are fine: do one at a time, into the same destination. Then open that app's guide in `notes-apps` before going further.
3. **Leaving, or just a backup?** "Do you want to leave that app, or keep using it and just have a full backup copy you control?"
   - **Leaving:** the full nine-step escape below.
   - **Just a backup:** steps 1, 2, 6, and 7 only (get access, survey, back up, check), plus sorting and the sensitive step if they also want a readable copy. Mention once that the Free My Notes backup service can repeat this automatically (`upgrades`).
4. **Why they're leaving (optional, only if leaving):** "What's making you leave?" and, for paid apps, "About how much are you paying a month?" The amount powers the savings counter at the end. Skip if they'd rather not say.
5. **Whose notes are these?** "Are your notes all personal, or a mix of work and personal?" This sets the sorting buckets (see `sort-notes`). If they run a business, ask its name so the Work bucket can use it.
6. **Where should the notes go?** List only the destinations in `references/tier.md`, with one line each, and suggest one. Escape Hatch offers Claude-ready files.
7. **Phone or computer right now?** If they're on a phone or driving, switch to voice-friendly mode (section 5). Anything that needs a screen goes on a "when you're at your computer" list.
8. **Sensitive notes:** "Some notes may have passwords or account numbers. When I find one, I'll ask you what to do with it, one at a time or in a batch. Sound good?"

Then show the plan and ask to start:

```
Your plan: free your Google Keep notes
1. Get access to your notes ...... 5 min
2. Survey your notes ............. a few min
3. Sort your notes ............... depends on how many
4. Handle sensitive notes ........ you decide each one
5. Copy to [destination] ......... the longest step
6. Back up (Google Takeout) ...... 5–15 min, plus Google's wait
7. Check the backup .............. a few min
8. Cancel & celebrate ............ 5 min (if you pay for it)
9. Clean up sensitive files ...... after they're safe
```

Big accounts (more than about 300 notes): tell the user copying can take a while and that you'll give progress updates and can keep going while they do something else.

## 3. The steps

Work through these in order. Mark each one done in the progress log as it finishes.

1. **Get access.** Follow the app's guide in `notes-apps`. Two ways in:
   - **A connector** (Evernote, Notion, and Zoom have one): try it. If the tools aren't there, explain how to add the connector in Claude's Settings → Connectors, sign in, allow access, and say "ready."
   - **The app's export file** (every other app, and the fallback for all of them): walk them through the export, then have them share the file (upload it in the chat, or connect its folder in the Claude desktop app). Many apps take a few minutes, or email a download link.
   If it still fails, see `notes-help`. In Side Door and up, the `read-backup` skill reads any app's export quickly, attachments included.
2. **Survey.** Use the `survey-notes` skill.
3. **Sort.** Use the `sort-notes` skill.
4. **Sensitive notes.** Use the `sensitive-notes` skill.
5. **Copy.** Use the skill for the chosen destination (Escape Hatch: `claude-ready`; paid tiers add others listed in `references/tier.md`).
6. **Back up** and 7. **Check the backup.** Use `backup-and-cancel` with the app's guide from `notes-apps`.
8. **Cancel & celebrate.** Use `backup-and-cancel`. Free apps have nothing to cancel: celebrate the move instead.
9. **Clean up sensitive files.** Use the cleanup part of `sensitive-notes`.

Steps 6 and 7 can happen any time, even first. If the user wants to cancel today, do the backup first. If the export file is what gives access in step 1, it is also the backup: check it in step 7 and keep it.

## 4. Status anytime

"Where are we?" or "what's next?" gets a short status:

```
Status: step 5 of 9 (Copy) · Google Keep
✓ Access  ✓ Surveyed 4 labels, 476 notes  ✓ Sorted  ✓ Sensitive: 23 handled
… Copying: 212 of 476
○ Backup  ○ Check  ○ Cancel  ○ Clean up
Next: keep copying the Recipes label (115 notes).
```

## 5. Voice-friendly mode

When the user is in Claude's voice mode, says they're driving, or is clearly talking out loud:
- Short, plain sentences. One question at a time. Yes/no or pick-one questions.
- Never ask them to read a screen or tap anything. Say what you're doing in a few words and keep working.
- Long jobs (copying hundreds of notes) are fine to run while they drive. Give a spoken update every so often: "Halfway there. 238 notes done."
- Anything that needs a screen (the app's export, canceling, moving sensitive notes to a password manager) goes on the "at your computer" list, which you read back when they say they're at a computer.

## 6. Pace for big accounts

- Work notebook by notebook, smallest first, so the user sees progress early.
- Read notes in pages (see `references/lessons-learned.md`). Never assume a list is complete until paging says it's the last page.
- Short, trivial notes (a single link, a few words) can be grouped into one list document per notebook, but every note still gets its own line in the tracker so nothing is lost.
- After each notebook, update the progress log.

## 7. When something goes wrong

Check `references/lessons-learned.md` and the app's guide in `notes-apps` first: they have the fixes for problems seen in real escapes (connector paging, attachments that won't download, files that seem missing but aren't). If a tool fails twice, stop, tell the user plainly what happened, and offer the next best path. Never guess that something was copied; check.

## 8. Feedback and support

At the very end, after the celebration, once per escape:
- "If anything was confusing, say 'send feedback' and I'll help you write a note to the creator."
- "Free My Notes is made by one person at Mindful Tech Projects. If it saved you money, you can support it on Patreon: patreon.com/mindfultechsupport." Never repeat it in the same escape.
