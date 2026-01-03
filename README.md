# WC Tracker

WC Tracker is an offline Escape from Tarkov quest tracker built with Electron. It focuses on local progress, quest dependency clarity, and item planning for Kappa progression. No accounts, no servers.

## Highlights
- Quest tracker with filters for Kappa-only, completion states, maps, traders, and search.
- Quest flow (tree) view with trader lanes, prerequisites, zoom/pan, and layout overrides.
- Item tracker that aggregates quest-required items with FIR tags.
- Achievements tracker with local completion state.
- Next Tasks recommendations with weighted scoring (Kappa/Lightkeeper pathing, level fit, friction, and item needs).
- Profile and onboarding flows with edition, faction, level, and quest selection logic.
- Local JSON storage with user overrides and progress in git-ignored folders.

## Getting Started (dev)
- Install Node.js (LTS recommended).
- Install dependencies:
  - npm install
- Run the app:
  - npm start
- Run tests:
  - npm test
- Rebuild quest directory:
  - npm run build:quest-directory
- Build a Windows installer:
  - npm run dist:win

## Build (release checklist)
1) Update version in package.json
2) npm install
3) npm run build:quest-directory
4) npm test
5) npm run dist:win

Notes:
- The installer is produced by electron-builder (NSIS) and already compressed.
- Output goes to dist/ as WCTracker-{version}-win-x64.exe.

## Data and Storage
- Quest and item data is stored under data/ and is curated from public sources and manual verification.
- Local user data is stored under user/ (ignored by git).
- User quest overrides live under user/quests/.

## Documentation
- Release notes: public_repo/RELEASES.md
- Dev log: public_repo/DEVLOG.md
- Roadmap: public_repo/ROADMAP.md
- FAQ: public_repo/FAQ.md
- Contributing: public_repo/CONTRIBUTING.md
- Disclaimer: public_repo/DISCLAIMER.md

## Contact
For support or feedback, reach out on Discord.

- Discord: XotiicWC

## Credits
- Escape from Tarkov Wiki (quest data references and documentation)
- tarkov.dev (item imagery and metadata references)
- Battlestate Games (Escape from Tarkov game and trademarks)
- Tyler (Bullet) Hoyos - WorldClassStudios Founder

## Status
Public beta. Features are evolving quickly and data updates track the live game.

## Company
WorldClassStudios
