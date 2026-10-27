---
name: my-escape-data
description: Privacy and consent for Escape from Evernote. Use when the user asks "what do you know about me", "what have you saved", "show my escape log", "forget my escape", "delete my progress", "stop saving", or "what happens to my notes". Also explains, at the start of an escape, what the plugin saves.
---

# Your data

## What the plugin saves

Only a short **escape log**, and only if the user agreed:
- their name, the buckets they chose, their destination, and (if shared) what they paid Evernote each month
- notebook names, note counts, and which steps are done
- the titles of notes and what was decided for them (titles of sensitive notes may be replaced with "sensitive note #N")

**Never saved:** note contents, passwords, account or card numbers, ID numbers, or anything inside a sensitive note.

**Where:** in the user's own Claude memory (`/areas/escape-from-evernote.md`) or a file in their own folder. Nothing goes to Mindful Tech Projects. The plugin has no servers and no analytics.

**The copied notes themselves** go only where the user chose: their downloads, their Google Drive, their Notion, and so on. The `.enex` backup stays wherever they saved it.

## Commands

- **"What do you know about me?" / "show my escape log":** show the log in plain language.
- **"Forget [something]":** remove that line from the log and confirm.
- **"Forget my escape" / "delete my progress":** offer the log as a download first, then delete the log file (or memory file) and confirm. This never touches their notes, their copies, or their backup.
- **"Stop saving":** stop updating the log for the rest of the chat; offer to delete it.

## The disclosure (first time)

Say it once, plainly, before the first save:
"I'll keep a short progress log so you can stop and pick up later: your notebook names and counts, how you want things sorted, and which steps are done. Never the contents of your notes, and never passwords. It stays in your own Claude account. Okay?"

Respect a no completely: work without saving.
