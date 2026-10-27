# Escape from Evernote
*A Claude plugin by Mindful Tech Projects*

**Current version: 1.0.0** · [Website](https://mindfultechsupport.github.io/Escape-from-Evernote/) · [Change summary](CHANGELOG.md) · [All releases](releases/)

**[❓ Help](HELP.md)** · **[💬 Send feedback](../../issues/new?template=feedback.yml)** · **[❤️ Support on Patreon](https://www.patreon.com/mindfultechsupport)**

## What it does

Escape from Evernote gets every note out of Evernote, safely, so you can stop paying for it. It counts everything you have, sorts work from personal, keeps your passwords and private documents out of the wrong places, copies your notes to where you want them, makes sure you have a full backup, and walks you through canceling. Nothing is deleted unless you ask.

It was built after its maker moved his own Evernote out with Claude: 476 notes in 32 notebooks, all backed up, and $22 a month saved. Every lesson from that escape is built in.

## How it feels to use

- **It interviews you first.** Your name, why you're leaving, work or personal, where your notes should go. One question at a time, with a suggested answer.
- **It shows you the whole plan.** Nine steps, from "connect Evernote" to "clean up," and you can stop anytime and pick up tomorrow.
- **It counts everything.** Every notebook and every note, so at the end it can prove nothing was left behind.
- **It sorts for you.** Work, Personal, Not sure, and Sensitive, notebook by notebook, and asks you about the ones it can't tell.
- **It protects your passwords.** Notes with logins, account numbers, or ID scans are kept out of Claude Projects and Claude's memory. It asks you what to do with each one, keeps them in a locked spot, gives you a printable sheet, and offers to delete those copies once you've moved them to a password manager.
- **It makes Claude-ready files.** Your notes come out as tidy files, one per notebook, ready to drop into a Claude Project.
- **It checks your backup.** It walks you through the `.enex` export from the Evernote desktop app and confirms every notebook made it, before you cancel.
- **It shows you the savings.** "You just saved $22 a month: $264 a year. Nice escape."
- **It talks like a person when you're talking out loud.** In voice mode, or when you say "I'm driving," it keeps going and gives you short spoken updates.

## Versions

Each version includes everything before it. Safety features (sensitive-note protection, the backup check, the cancel guide) are in every version, including the free one.

| Version | Price | Adds |
|---|---|---|
| **Escape Hatch** | Free | Survey, sorting, sensitive-note protection, Claude-ready files, backup guide and check, cancel guide, savings counter, voice-friendly mode |
| **Side Door** | $9 one time | Reads your `.enex` backup (every PDF, photo, and attachment); Google Drive with one Google Doc per note, a tracker sheet, and a locked folder for sensitive notes |
| **Getaway Car** | $18 one time | Notion, Word files and OneDrive, Markdown and Obsidian, your own sorting buckets |
| **The Great Escape** | $27 one time · early access | Autopilot: Claude does the export and the moving on your computer while you talk to it from your phone. Apple Notes. Google Keep (Claude types each note in; the slowest option). Hand your ideas to [All of my Irons in the Fire!](https://github.com/MindfulTechSupport/All-of-the-Irons-in-the-Fire-App-) (beta) |

Paid versions are on the [website](https://mindfultechsupport.github.io/Escape-from-Evernote/#pricing): Patreon, Gumroad, Lemon Squeezy, or pay with crypto (Bitcoin, Ethereum, Solana; no card or bank details needed). Each comes as a `.plugin` file you install the same way as the free one.

## Install

**You'll need a computer for this.** Plugins are added in Claude on the web (claude.ai), the Claude desktop app, or Claude Code; the Claude phone app can't install a plugin from a file. Once installed, it's on your Claude account, and you can talk to it from your phone.

### Option 1: add the marketplace (free version)

- **Claude desktop app or claude.ai:** go to **Customize → Plugins**, add a marketplace, and enter `MindfulTechSupport/Escape-from-Evernote`. Then install **escape-from-evernote**.
- **Claude Code:**
  ```
  /plugin install escape-from-evernote --marketplace MindfulTechSupport/Escape-from-Evernote
  ```

### Option 2: install from a file (any version)

1. Download the `.plugin` file: [the latest free release](../../releases/latest) (currently `escape-from-evernote-free-v1.0.0.plugin`), or the file from your purchase.
2. In the Claude desktop app or claude.ai, go to **Customize → Plugins**.
3. Remove an older Escape from Evernote if it's listed, then upload the file.

### Then

1. Connect the **Evernote connector** in Claude (**Settings → Connectors**), sign in to Evernote, and allow access.
2. Start a new chat and say **"escape Evernote."**

## Try saying

- **"Escape Evernote."** Starts the interview and the plan, or picks up where you left off.
- **"Where are we?"** Shows the escape status: what's done and what's next.
- **"I'm driving, keep the escape going."** Switches to short spoken updates.
- **"What do you know about me?"** Shows the progress log; "forget my escape" erases it.
- **"How do I back up my Evernote?"** Walks you through the `.enex` export.
- **"How do I cancel?"** The cancel guide for Evernote, Apple, or Google Play billing.
- **"Help."** Fixes for the common problems.
- **"Send feedback."** Drafts a note to the creator with you.

## Skills (free version)

| Skill | What it's for |
|---|---|
| `escape-plan` | The interview, the nine-step plan, status, voice-friendly mode, and the progress log |
| `survey-notebooks` | Counts every notebook and note, with full paging so nothing is missed |
| `sort-notes` | Sorts notes into Work, Personal, Not sure, and Sensitive |
| `sensitive-notes` | Finds passwords and private notes, asks what to do with each, and cleans up the copies later |
| `claude-ready` | Makes Markdown files and a tracker, ready to add to a Claude Project |
| `backup-and-cancel` | The `.enex` export, the backup check, the cancel guide, and the savings counter |
| `escape-help` | Troubleshooting and feedback |
| `my-escape-data` | What's saved, and how to see or erase it |
| `escape-upgrades` | What the other versions add, and how to install one |

## Promises

1. **The plugin never deletes your notes.** Deleting anything in Evernote, or your Evernote account, is your own step, after your backup is checked.
2. **Back up before you leave.** The `.enex` export comes before canceling.
3. **Sensitive stays out of the wrong places.** Passwords, account numbers, and ID numbers never go into a Claude Project, Claude's memory, or a shared folder.
4. **Nothing goes to Mindful Tech Projects.** No servers, no analytics. See [PRIVACY.md](PRIVACY.md).
5. **Safety is never behind a paywall.**

## Repository layout

```
README.md        This page, always describing the current version
CHANGELOG.md     What changed in every version, newest first
LICENSE          Usage terms
HELP.md          Answers to common questions
PRIVACY.md       What the plugin does (and doesn't do) with your information
.claude-plugin/  Marketplace catalog, so Claude can install the plugin from this repo
docs/            The website (GitHub Pages)
plugin/          The free plugin's source files (current version)
releases/        Frozen copies of every version, version number in each file name
  v1.0.0/
```

## Versioning

Versions follow [Semantic Versioning](https://semver.org): `MAJOR.MINOR.PATCH`. Each release gets a git tag (`v1.0.0`), a GitHub Release with notes and the downloadable free plugin, an entry in CHANGELOG.md, and a folder in `releases/` with versioned copies of the plugin, README, and design notes.

Every version goes through review before it's published:

1. **Prepare** on a `release/vX.Y.Z` branch: update `plugin/` and its version number, add the version's section to CHANGELOG.md, and add a `releases/vX.Y.Z/` folder with the versioned files.
2. **Review** in a pull request. The owner reviews the changes; nothing is public yet.
3. **Publish** only after the owner approves: the pull request is merged into `main`, and the [Publish releases](.github/workflows/release.yml) workflow creates the tag and Release page automatically.

## Not affiliated with Evernote

Escape from Evernote is an independent project by Mindful Tech Projects. It is not affiliated with, endorsed by, or sponsored by Evernote or its owner. Evernote is a trademark of its owner. It is also not affiliated with Anthropic; Claude is a product of Anthropic.

## License

Copyright © 2026 Mindful Tech Projects. All rights reserved. See [LICENSE](LICENSE). The free version is free to use; the source is not open for reuse or redistribution.
