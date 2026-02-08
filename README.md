# WC Tracker

WC Tracker is an offline Escape from Tarkov quest tracker built with Electron. It focuses on local progress, quest dependency clarity, and item planning for Kappa progression. No accounts, no servers.

## Highlights
- Quest tracker with filters, quest details, and quick actions.
- Quest detail views with image galleries and zoom/pan viewer.
- Quest tree view with trader lanes, prerequisites, Kappa markers, focus mode, and zoom/pan.
- Dashboard landing page with map-based recommendations and item panels.
- Dashboard map selector highlights a recommended map based on active tasks.
- Dashboard and item progress updates stay in sync across tiles and detail popups.
- Raid bring-in items now respect map selection and objective progress (remaining counts).
- Item tracker for quest-required items with FIR tags, reward sources, and hideout requirements.
- Partial completion tracking for items and objectives across quest tracker, dashboard, and item tracker.
- Achievements tracker with search and local completion state.
- Hideout tracker with per-level requirements, unlocks, and upgrades.
- Next Tasks recommendations that factor in item needs and progression paths.
- PvP/PvE modes with separate progress (shared username/edition).
- Mode selection auto-picks PvP/PvE when only one profile exists; profile creation uses a lightweight popup.
- Overlay toggle is session-only; restarting the app resets it.
- Overlay close control supports click-out and Esc to dismiss.
- Guided auto sync in onboarding is temporarily disabled (manual setup only).
- Update checker tied to GitHub Releases with in-app download/install for signed builds.

## Download and Install
- Download the latest Windows installer from Releases:
  https://github.com/BulletTRL/WCTracker-Public/releases
- Run the installer and launch WC Tracker.

## Updates
- The app checks for updates on launch.
- Use the Update badge in the header to open the updater panel and download/install in-app.
- Releases must include the installer, latest.yml, and blockmap assets for updates to succeed.

## Getting Started
1) Launch the app and pick PvP or PvE.
2) Complete onboarding (callsign, level, edition, starter quests).
3) Use filters, the quest tree, item tracker, and hideout tracker to plan progression.

## Support Diagnostics (Hidden)
For troubleshooting, click the page title 5 times and press Ctrl/Cmd+Shift+D to open the diagnostics console.

## Data and Privacy
All progress is stored locally in JSON files. No accounts or servers are required.

## Documentation
- Release notes: public_repo/RELEASES.md
- Roadmap: public_repo/ROADMAP.md
- FAQ: public_repo/FAQ.md
- Screenshots: public_repo/SCREENSHOTS.md
- Disclaimer: public_repo/DISCLAIMER.md
- Overlay compliance notes: public_repo/OVERLAY_COMPLIANCE_NOTES.md

## Contact
Discord: https://discord.gg/rEb8J4y6SF

## Credits
- Escape from Tarkov Wiki (quest data references and documentation)
- tarkov.dev (item imagery and metadata references)
- Battlestate Games (Escape from Tarkov game and trademarks)
- Tyler (Bullet) Hoyos - WorldClassStudios Founder

## Status
Public beta. Features are evolving quickly and data updates track the live game.

## Company
WorldClassStudios
