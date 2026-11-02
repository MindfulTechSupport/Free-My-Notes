---
name: sensitive-notes
description: Step 4 and step 9 of Free My Notes. Finds notes with passwords, logins, account or card numbers, ID numbers, and private legal, medical, or family matters; asks the user what to do with each one; keeps them in a locked spot; and, once the user has moved them somewhere safe, offers to delete those temporary copies for good. Use when the escape reaches sensitive notes or cleanup, or when the user says "what did you find that's private", "show my sensitive notes", "I've moved my passwords", "print my sensitive notes", or "delete the sensitive files".
---

# Sensitive notes

Notes apps often end up holding the keys to someone's life: Wi-Fi passwords, bank logins, safe codes, a scan of a driver's license. These need different handling from everything else. This skill is in every tier. Safety is never paywalled.

## What counts as sensitive

Flag a note as sensitive if it contains any of these (or the user says so):

- **Logins:** usernames with passwords, PINs, recovery codes, security questions, Wi-Fi or router passwords, door or lock codes, safe or vault combinations.
- **Money:** bank account or routing numbers, card numbers, crypto wallet keys or seed phrases, loan or investment account numbers.
- **Identity:** Social Security or national ID numbers, driver's license, passport, birth certificate, tax ID or EIN letters.
- **Private matters:** medical, therapy, legal or court matters, custody, background checks, anything about abuse or safety.
- **Other people's secrets:** another person's logins or account numbers.

When in doubt, flag it and let the user decide.

**Never quote sensitive content back in chat.** Refer to notes by title and what kind of thing they hold ("Bank info - SWF: account numbers and a login"). Never put sensitive content into Claude's memory, the progress log, a Claude Project, or a shared folder.

## Ask the user (step 4)

1. Say how many you found and offer a choice of pace:
   "I found 23 notes that look sensitive: 12 with passwords or logins, 6 with account numbers, 3 ID documents, and 2 private family or legal notes. Want to go one at a time, by group, or use the same choice for all of them?"
2. For each note (or group), offer these choices. Suggest **Locked copy** as the default:

| Choice | What happens |
|---|---|
| **Locked copy** (suggested) | Copy it into a separate locked spot, never into the main destination. You move it to a password manager (or print it), then it gets deleted. |
| **Skip** | Don't copy it at all. It stays in the notes app and in your backup. Good for things you've already saved elsewhere. |
| **Copy normally** | Treat it like any other note. Only for things that aren't actually private (a public Wi-Fi password, an old expired code). |

3. Record each decision in the tracker (title and choice only).

## The locked spot

Where it lives depends on the destination:

- **Claude-ready files (Escape Hatch):** one separate file, `SENSITIVE - move to password manager - <date>.md`, made for download only. Tell the user plainly: "Don't add this file to a Claude Project. Download it, move what's in it to your password manager, then delete it."
- **Google Drive (Side Door and up):** a folder named `Sensitive – RESTRICTED (delete after moving)` with inherited sharing turned off, so only the owner can open it. Check its permissions after creating it.
- **Other destinations:** a single local file like the Escape Hatch one. Never into Notion, Keep, Apple Notes, or a shared workspace unless the user insists after being told the risk.

Organize the locked copy by type (Logins, Accounts, IDs, Private) so it's quick to move into a password manager.

## Printable sheet (optional)

Offer once: "Want a printable version? Some people keep a paper copy in a safe." If yes, make a clean, printer-friendly document (PDF if available) with one section per type, large text, and a header that says "PRIVATE — store securely." Remind them to delete the digital file after printing.

## Cleanup (step 9)

When the user says they've moved everything (to a password manager, printed it, or both):

1. Confirm in plain words: "You've moved your sensitive notes somewhere safe and want me to delete the temporary copies I made. This can't be undone. Delete them?"
2. Only on a clear yes, delete **only the files and folders this plugin created for sensitive notes**, and list exactly what was deleted.
3. If the destination has a trash (Google Drive, a computer), remind them to empty it, or offer to, since deleted files stay in trash for a while.
4. Remind them the originals are still in their notes app and in the backup. Those are theirs to keep or delete. The plugin never deletes anything from the notes app.
5. Mark cleanup done in the progress log.

If the user wants the sensitive copies deleted right away, before moving them anywhere, warn once that it'll be their only easy-to-read copy outside the notes app and the backup, then do it if they confirm.

## Password managers (if asked)

Suggest they use whatever they already have (Apple Passwords/iCloud Keychain, Google Password Manager, 1Password, Bitwarden, and others). Don't recommend one as best. Most can import a simple list, but typing a few by hand is often quicker for small amounts.
