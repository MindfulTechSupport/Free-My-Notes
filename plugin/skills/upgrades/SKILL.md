---
name: upgrades
description: Explains the Free My Notes versions and the backup service, and how to get or install them. Use when the user asks "what do the paid versions do", "how do I get Google Drive / Notion / Apple Notes / Google Keep as a destination", "can Claude do the export for me", "upgrade", "how much is it", "how do I install the paid version", "can you back up my notes automatically", or asks for a feature their tier doesn't include.
---

# Versions, the backup service, and upgrades

Mention paid versions only when the user asks, or when they ask for something their tier doesn't include, and at most once per session. Never pressure. Safety features and every app's backup guide are in every version.

Check `../free-my-notes/references/tier.md` to see what's installed.

## The four versions (each includes everything before it; one-time prices)

| Version | Price | Adds |
|---|---|---|
| **Escape Hatch** | Free | All 14 notes apps' guides, survey, sorting, sensitive-note protection, Claude-ready files, backup guide and check, cancel guide, savings counter, voice-friendly mode |
| **Side Door** | $9 | Reads any app's backup in one pass (every PDF, photo, and attachment, big exports included); Google Drive (one Google Doc per note plus a tracker sheet, locked sensitive folder) |
| **Getaway Car** | $18 | Notion, Word files / OneDrive, Markdown / Obsidian vault, your own sorting buckets |
| **The Great Escape** | $27 · early access | Autopilot: Claude makes the exports and does the moving by using your computer while you talk to it from your phone. Apple Notes and Google Keep as destinations. Hand-off to "All of my Irons in the Fire!" (beta) |

Google Keep has no import, so Claude types notes in one at a time. It's the slowest destination: plan to leave the laptop open, plugged in, and awake.

## The backup service ($1 a month)

For people who keep using their notes app and want a copy they control, made for them on a schedule:
- Runs as a scheduled task in **their own Claude** (needs a paid Claude plan) and saves a dated backup to **their own** Google Drive or a folder on their computer. Mindful Tech Projects never sees it.
- Automatic for apps Claude can reach with a connector (Evernote, Notion, Zoom); for other apps, a reminder on schedule plus a check of the export they drop in.
- Installed as its own small plugin, `free-my-notes-backup`, next to any version.

## Where to get them

Website, with every way to pay: https://freemynotes.com
- Patreon (one-time purchase, or a membership for the backup service)
- Gumroad
- Lemon Squeezy
- Pay with crypto (Bitcoin, Ethereum, Solana): no card or bank details needed

Each purchase comes with a `.plugin` file.

## Installing a version

On a computer (the Claude phone app can't install plugins from a file):
1. In the Claude desktop app or claude.ai, go to Customize → Plugins.
2. Remove the older Free My Notes if it's listed.
3. Upload the new `.plugin` file.
4. Start a new chat and say "free my notes." The progress log is kept separately, so the escape picks up where it left off.

The backup service plugin installs the same way, but leave Free My Notes installed beside it.
