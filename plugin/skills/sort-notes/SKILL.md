---
name: sort-notes
description: Step 3 of Free My Notes. Sorts every note into buckets (for example Work, Personal, Not sure, Sensitive) so work and personal stay apart and private notes get special care. Use when the escape plan reaches sorting, or when the user says "sort my notes", "which notes are work", "re-sort that notebook", or "move that note to personal".
---

# Sort your notes

## The buckets

Set the buckets from the interview answer about whose notes these are:

| User said | Buckets |
|---|---|
| All personal | **Personal**, **Not sure**, **Sensitive** |
| Mix of work and personal | **Work** (use their business name if they gave one, like "Sam's Bakery"), **Personal**, **Not sure**, **Sensitive** |
| Several businesses | One Work bucket per business, plus **Personal**, **Not sure**, **Sensitive** |

Escape Hatch, Side Door: these buckets only (the Work bucket can be renamed). Getaway Car and up: the `custom-categories` skill lets the user add their own (School, Family, Recipes, Clients…).

**Sensitive always wins.** If a note is sensitive, it goes in Sensitive no matter what else it is (see `sensitive-notes` for what counts).

**Not sure is a good answer.** When a note could go either way, put it in Not sure with a short reason. The user decides later. Never guess on a note that might be private.

## How to sort

1. **Sort by notebook first.** Most notebooks are clearly one bucket ("Recipes" → Personal, "Clients" → Work). Propose the notebook-level bucket for every notebook in one list and let the user fix any: "Here's how I'd sort your notebooks. Anything look wrong?"
2. **Then look at each note** inside mixed notebooks (catch-alls like "Notes," "Sam's notebook," "Inbox," or Keep notes with no label). Sort note by note, with a reason in a few words ("client network notes", "family photo", "contains a password").
3. **Scan every note for sensitive content** regardless of its notebook (a recipe notebook can still hold a bank login).
4. **Show a summary** before moving on:

```
Sorted 476 notes
• Work: 151
• Personal: 285
• Not sure: 17  ← want to go through these now or later?
• Sensitive: 23  ← next step handles these
```

5. **Not sure notes:** offer to go through them now, quickly, one line each: "'Idea for a pop-up shop' — Work idea or personal? Or skip?"

## Record it

Write each note's bucket and short reason into the tracker that the destination step creates (every tier makes a tracker), and the bucket counts into the progress log. The user can change any note's bucket anytime: "move 'Tea Recipe' to Personal."

## Tips

- A notebook's name is a strong hint, but read the note when it disagrees ("CRT 1" was a client's notebook but held one movie title, which is personal).
- Shared notebooks may contain other people's notes; mention it and treat them as Not sure unless the user says otherwise.
- Keep reasons short and never quote sensitive content in a reason.
