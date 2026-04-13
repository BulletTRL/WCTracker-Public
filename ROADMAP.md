# Roadmap

This is a lightweight roadmap based on current plans and beta feedback. Priorities can shift.

## Release Gate (v1.3.6)
- Fresh `npm start` smoke test: login, profile totals, dashboard, quest list/details, quest tree, item tracker, achievements, hideout, overlay, and onboarding/OCR status
- Confirm quest tree trader portraits and custom layout positions after remote app-data migration
- Confirm remote-only app-data behavior shows a clear error when required datasets cannot load
- Build signed Windows installer and fresh-install smoke test
- Confirm GitHub release assets include installer, `latest.yml`, and blockmap files

## Recently Completed
- Remote app-data pipeline for Supabase Storage and release metadata tables
- Remote-only migrated app content after login: quests, quest directory, layout overrides, image index, item index, achievements, and hideout
- Legacy app-content source moved under `Archives/`; live `data/` now keeps packaged branding assets only
- Remote dataset caching and lazy quest-detail loading to reduce repeat load time
- Hidden diagnostics `/network` output for remote/auth call timings
- Protected saved-login passwords from reveal/copy on reopen
- Quest tree remote migration fix for layout overrides and trader portraits
- v1.3.6 package metadata and public/internal release documentation refresh

## Active (Soon)
- Guided onboarding OCR matching stabilization for multi-line quest titles
- Password reset flow (email)
- Website account portal for username/email management
- Two-factor authentication groundwork
- Remote manifest validator and publish health check before builds
- First-load sync status/progress messaging for remote datasets
- Remote app-data cleanup/reporting for stale unreferenced storage files
- All Items view (search item, see requirements, rewards, barters, hideout use, and description)
- Active Overlay for displaying item requirements
- Debounced save pipeline with forced flush on close and critical actions
- PvP prestige flow (hide prestige quests until the next threshold)

## Backlog
- Installer UI/branding polish (NSIS styling, visuals, and copy)
- Auto-rotating data backups (5-slot history with version/date metadata) plus restore/export selection UI
- Safeguards for irreversible actions (confirmation/undo + restore path for resets and quest path changes)
- Quest tree grid + camera correctness pass (snap/offset/clamp cleanup to keep alignment polished)
- Quest tree render performance pass (address large render warnings seen in the console)

## Long Term
- Map-based loot key guide (click key to see possible loot)
- Barter items tab
- Additional onboarding improvements and mid-wipe start support
- Performance and packaging optimizations

If you want to suggest a priority, open an issue or post feedback with details.
