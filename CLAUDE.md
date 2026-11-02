# Free My Notes · instructions for Claude

This public repo holds the free plugin (Escape Hatch), the website (`docs/`, freemynotes.com), and the docs. Paid versions, the backup service, and the project's governance documents live in the owner's private repo, Free-My-Notes-Pro.

**Before any change, follow the standing rules** (master copy: `governance/STANDING-RULES.md` in the private repo). The ones that matter most here:
- The plugin never deletes users' notes and never calls a notes app's delete tools; backups come before canceling.
- Sensitive notes never go into Claude Projects, memory, logs, trackers, combined files, or shared folders. Safety features and every app's backup guide stay free.
- No other company's name in our product name, domain, or repo name; app names only as "works with," with trademark credit.
- Never use the owner's real notes, notebooks, or clients in examples; use the made-up person "Sam."
- Never put a paid `.plugin` file in this repo.
- Releases go on a `release/vX.Y.Z` branch and merge to `main` only after the owner approves the pull request.
