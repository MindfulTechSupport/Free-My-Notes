---
name: survey-notebooks
description: Step 2 of Escape from Evernote. Counts every Evernote notebook and note through the Evernote connector and builds the survey the rest of the escape works from. Use when the escape plan reaches the survey step, or when the user asks "how many notes do I have", "what's in my Evernote", "list my notebooks", or "survey my Evernote".
---

# Survey your notebooks

The survey is the master list. Every later step (sorting, copying, the backup check) is checked against it, so be complete and exact.

## How

1. **List all notebooks** with the Evernote connector. Record each notebook's name, its stack (if any), and whether it's shared.
2. **Count notes in each notebook** by searching `notebook:"<name>"` with the largest page size, paging until the last page (see `../escape-plan/references/lessons-learned.md`). Record:
   - note count
   - newest and oldest note dates
   - how many notes have attachments (empty snippets usually mean attachment-only notes; the full note shows the attachment list)
   - how many look like web clips (long page text, a source link)
3. **Spot empty notebooks** (0 notes). They need nothing; list them as "empty, skip."
4. **Ask about Trash** once: "Evernote's Trash has notes you deleted. Want those too, or leave them?" Default: leave them.
5. **Total it up** and check: the sum of notebook counts must equal the total from an all-notes search. If it doesn't, find the gap before moving on (often a notebook missed inside a stack, or a page that wasn't fetched).

## Show the user

Short, scannable, biggest first. Then a one-line read on how long copying might take.

```
Your Evernote: 32 notebooks with notes, 476 notes (plus 6 empty notebooks)
• Sam's notebook ... 115
• Side Projects ......... 95
• Recipes ............... 56
• Clients ............... 30
• …and 28 more (show all?)
About 140 notes have attachments (PDFs, photos). Copying will take a while; I'll keep you posted.
```

In voice-friendly mode, say the totals and the top three only.

## Save

Write the notebooks table and totals into the escape log (`../escape-plan/references/escape-log-format.md`), mark the survey step done, and move on to sorting.

## Big accounts

For more than about 1,000 notes, tell the user before you start that the survey alone may take several minutes, and give a progress line every few notebooks.
