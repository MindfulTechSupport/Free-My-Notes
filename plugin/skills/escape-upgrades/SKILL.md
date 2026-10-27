---
name: escape-upgrades
description: Explains the Escape from Evernote tiers and how to get or install one. Use when the user asks "what do the paid versions do", "how do I get Google Drive / Notion / Apple Notes / Google Keep", "can Claude do the export for me", "upgrade", "how much is it", "how do I install the paid version", or asks for a feature their tier doesn't include.
---

# Tiers and upgrades

Mention paid tiers only when the user asks, or when they ask for something their tier doesn't include, and at most once per session. Never pressure. Safety features are in every tier.

Check `../escape-plan/references/tier.md` to see what's installed.

## The four tiers (each includes everything before it)

| Tier | Price | Adds |
|---|---|---|
| **Escape Hatch** | Free | Survey, sorting, sensitive-note protection, Claude-ready files, backup guide and check, cancel guide, savings counter, voice-friendly mode |
| **Side Door** | $9 one time | Reads the `.enex` backup (gets every PDF, photo, and attachment), copies to Google Drive (one Google Doc per note plus a tracker sheet, locked sensitive folder) |
| **Getaway Car** | $18 one time | Notion, Word files / OneDrive, Markdown / Obsidian vault, your own sorting buckets |
| **The Great Escape** | $27 one time · early access | Autopilot: Claude does the export and the moving by using your computer while you talk to it from your phone. Apple Notes and Google Keep. Hand-off to "All of my Irons in the Fire!" (beta) |

Google Keep has no import, so Claude types notes in one at a time. It's the slowest destination: plan to leave the laptop open, plugged in, and awake.

## Where to get them

Website, with every way to pay: https://mindfultechsupport.github.io/Escape-from-Evernote/
- Patreon (one-time purchase)
- Gumroad
- Lemon Squeezy
- Pay with crypto (Bitcoin, Ethereum, Solana): no card or bank details needed

Each purchase comes with a `.plugin` file for that tier.

## Installing a tier

On a computer (the Claude phone app can't install plugins from a file):
1. In the Claude desktop app or claude.ai, go to Customize → Plugins.
2. Remove the older Escape from Evernote if it's listed.
3. Upload the new `.plugin` file.
4. Start a new chat and say "escape Evernote." The progress log is kept separately, so the escape picks up where it left off.
