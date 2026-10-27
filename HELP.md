# Help

*Escape from Evernote · Mindful Tech Projects*

Quick answers to the things people run into most. You can also just ask the plugin: "help."

## Getting started

### Claude can't see my Evernote

The Evernote connector isn't added or isn't signed in. In Claude, open **Settings → Connectors**, add **Evernote**, sign in, and allow access. Then start a new chat and say "escape Evernote." If it was working and suddenly fails, try once more; Evernote's service sometimes hiccups.

### Nothing happens after installing

Start a brand-new chat. Existing chats may not pick up a new plugin. Then say "escape Evernote."

### Can I do this from my phone?

You can talk to it from your phone once it's installed, and copying can keep going while you drive. Installing the plugin and making the backup need a computer. The plugin keeps an "at your computer" list for those steps.

## During the escape

### Some notes look missing

Before worrying: most "missing" notes are on a page of results that wasn't fetched yet, inside a stack, empty, in Evernote's Trash, or a sensitive note you chose to skip. Say "check the counts" and the plugin re-counts with full paging and compares against the tracker.

### My PDFs and photos didn't come over

In the free version (Escape Hatch), attachments are listed in the tracker but not copied, because Claude often can't download them through the Evernote connector. They are all inside your `.enex` backup, so nothing is lost. Side Door and up read the backup directly and pull every attachment out.

### How do I make the backup (.enex export)?

It has to be the **Evernote desktop app**, not the website.
1. Open Evernote on your computer and go to **Notebooks**.
2. Next to a notebook, click **⋯ (More actions) → Export notebook…**
3. Choose **ENEX (.enex)**, keep tags and other details checked, and click **Export**.
4. Save it to one folder, like "Evernote Export – October 2026." Repeat for each notebook. Empty notebooks can be skipped.
5. Make a second copy of the folder somewhere else: an external drive, or Google Drive.

Then say "check my backup" and the plugin compares the files against the survey.

### I pressed Esc and Claude stopped (The Great Escape)

Esc is the stop button for Claude using your computer. Say "keep going" and it picks up where it left off.

### Claude stopped while my laptop was closed

Long jobs that use your computer (Autopilot, Google Keep) need the laptop open, plugged in, and awake. Reopen the chat in the Claude desktop app and say "keep going."

## Sensitive notes

- **What counts:** passwords, logins, account or card numbers, ID numbers, and private legal, medical, or family notes.
- **What happens:** the plugin asks you about each one. The default is a locked copy that never goes into a Claude Project, Claude's memory, or a shared folder.
- **The best home for passwords** is a password manager. Once you've moved them, say "clean up my sensitive notes" and the plugin deletes the copies it made, only after you confirm.
- **Remember Evernote's Trash.** After you delete notes in Evernote yourself, empty Evernote's Trash too.

## Canceling Evernote

Do the backup first. Then cancel where you pay:
- **Paid on Evernote's website:** sign in on evernote.com, open your account settings, and look for Billing or Subscription.
- **Paid through Apple (iPhone or Mac App Store):** Settings → your name → Subscriptions → Evernote → Cancel.
- **Paid through Google Play:** Play Store → profile → Payments & subscriptions → Subscriptions → Evernote → Cancel.

Menus change from time to time; say "how do I cancel" and the plugin walks you through what you see.

## Paid versions

- **Installing:** remove the older Escape from Evernote in **Customize → Plugins**, then upload the new `.plugin` file. Your progress log is kept separately, so the escape picks up where it left off.
- **Where to buy:** the [website](https://mindfultechsupport.github.io/Escape-from-Evernote/#pricing).
- **Lost your file?** Open the purchase email or your Patreon, Gumroad, or Lemon Squeezy library and download it again. For crypto purchases, [send feedback](../../issues/new?template=feedback.yml) with your order number (never your wallet keys or seed phrase).

## Your information

- **See what's saved:** "what do you know about me?"
- **Erase it:** "forget my escape." You'll be offered a copy first. This never touches your notes, your copies, or your backup.
- Nothing is sent to Mindful Tech Projects. See [PRIVACY.md](PRIVACY.md).

## Still stuck?

Say "send feedback" and describe what happened, or [open a feedback form](../../issues/new?template=feedback.yml). Posts there are public, so leave out anything private.
