# FAQ

## Is WC Tracker offline?
Progress is stored locally, but login and published app content require WC Tracker services. There is no cloud progress sync yet.

## Do I need an account?
Yes. You can sign in with your username or email and password. Account management is handled on the website for now.

## Where is my data stored?
Local user data is stored on your device, including progress and quest overrides. Published quest/item/hideout/achievement content is loaded from WC Tracker's remote app-data service after login.

## Why does the app need the remote data service?
WC Tracker now ships app content through a published remote manifest so quest data, item data, images, achievements, and hideout requirements can be updated without rebuilding the Electron app.

## What happens if remote app data cannot load?
The app should show a clear remote-data error instead of loading stale migrated data.

## Does it support Kappa tracking?
Yes. Kappa-required quests are tracked and used by the recommendations and gating rules.

## Does it support PvE and PvP profiles?
Yes. PvE and PvP have separate progress data so you can track both.

## Why didn't I get a mode selection prompt?
If only one profile has progress, WC Tracker auto-selects it to get you into the app faster.

## Is there a diagnostics console for support?
Yes. Click the page title 5 times, then press Ctrl/Cmd+Shift+D to open the hidden diagnostics panel.

## The overlay keeps turning off. How do I reset OCR?
The overlay toggle now persists across game restarts. If OCR gets stuck, toggle Overlay Off and back On to reset OCR state.

## How do updates work?
Updates are delivered via GitHub Releases and downloaded/installed in-app for signed builds. The installer, latest.yml, and blockmap must be attached to the latest release for updates to work.

## Is this affiliated with Battlestate Games?
No. WC Tracker is a community project and is not affiliated with Battlestate Games.

## How do I report issues?
Post feedback in Discord or open an issue with clear steps and screenshots where possible.
