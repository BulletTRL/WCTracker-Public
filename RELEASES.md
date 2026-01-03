# Release Notes

## v1.2.1 (1/2/2026)
- Restore onboarding prereq auto-completion for selected Ref/BTR/Lightkeeper quests while keeping level-based auto-complete excluded for those traders.
- Keep Collector/Kappa gating intact during onboarding auto-completion.
- Normalize completed/failed status checks so quest tree and tracker stay in sync across ID/name formatting differences.
- Add a Hideout Tracker placeholder view and menu entry for upcoming hideout upgrade tracking.
- Recommendations factor in quest item requirements and FIR counts to improve priority scoring.
- Recommendation cards show an item badge with total and FIR counts.
- Recommendation scoring uses normalized, balanced factors with weights in a single config block.
- Downscale item images to reduce packaged size.
- Document Next Tasks recommendations and item badges.
- Build packaging updates to stabilize 1.2.1 distribution.

## v1.2.0 (1/1/2026)
- Switch Windows build to NSIS-only installer and remove portable/zip targets.
- Add ASAR packaging and stable artifact naming for cleaner distributions.
- Add publisher/legal metadata and a copyright string for consistent installer details.

## v1.1.9 (1/1/2026)
- Improve onboarding quest search matching and dropdown positioning to prevent layout shifts.
- Stop onboarding from auto-completing all visible quests; only explicit prereqs are auto-completed.
- Remove total counters from item tracker section headers.
- Fix Safe Corridor unlock gating by clearing optional requires_any data.
- Preserve original prereq-hiding behavior after testing an alternate onboarding flow.
- Lightkeeper quests stay locked after the unlock chain unless they directly depend on Getting Acquainted.
- Delete the guitar pick item record from the tracker.
- Add Pathfinder to achievements with the correct metadata and local icon.
- Add missing EFT achievements from the wiki and refresh the source timestamp.
- Merge PVE duplicates into the base achievements.
- Download achievement icons for local display.
- Remove the green header bar in the profile panel.
- Remove the in-section Item Tracker heading and duplicate empty-state heading.
- Onboarding quest autofill starts after 3 characters instead of 5.
- Block auto-completing future quests that depend on selected prerequisites.
- Ensure Collector only shows as available after all Kappa-required quests are completed.
- Exclude BTR quests from onboarding auto-complete and ensure rep-regain tasks only auto-complete when their failed requirements are met.
- Stop hiding prereq quests during onboarding search to reduce false missing reports.
- Remove duplicate Cold Blooded quest entry.
- Exclude failed quests from Kappa progress and completion counts.
- Item tracker status tags use quest ID visibility so active/future states display correctly.
- Align item tracker filters with quest tracker UI and move search into the filters panel.
- Default item tracker to Active/Future on with Completed/FIR off.
- Show needed items in a two-column grid when completed items are hidden.
- Expand item list viewport height and align tracker width to the quest layout.

## v1.1.8 (12/28/2025)
- Add requires_any handling so OR groups work and selecting one path auto-fails the others.
- Normalize prereq/unlock data across quest JSONs and remove timing suffixes.
- Add requires_any groups to quests that needed OR gating.
- Add item requirements for Painkiller (4x Morphine injector FIR) and Colleagues - Part 3 (keycards and injectors).
- Clean item tracker duplicates and remove generic placeholders.
- Remove clock dial paintings from the tracker and add the Taiga wiki link.
- Switch image sync to tarkov.dev with stronger name normalization and 512px gun art.
- Rebuild item images and refresh catalog image paths.
- Gate rep-regain items so they appear only after failed requirements are met.
- Expand non-item filtering to keep objective placeholders out of the catalog.

## v1.1.8 (12/27/2025)
- Fill Collector.json with Kappa-required prereqs and rebuild quest-directory.json.
- Resync quest item requirements and refresh items.json.
- Update parsing/normalization logic in item scripts and image handling.
- Add the new quest file setting_priorities.json (untracked at the time).
- Drop The Stylish One from quest data and rebuild quest-directory.json.
- Normalize prereq resolution by stripping timing suffixes so low-level accounts do not see locked quests.
- Ignore Python cache files and remove tracked pyc artifacts.

## v1.1.7 (12/26/2025)
- Add found_in_raid_items to every quest with wiki verification and link fixes.
- Rework item tracker flow to support quest-derived FIR flags and split Active/Future vs Completed items.
- Build an item catalog generator that aggregates requirements, FIR flags, wiki links, and reward sources.
- Download item images and track missing pages/images.
- Add normalization maps to resolve item naming issues and avoid quest-only placeholders.
- Add item_requirements to quests and normalize FIR vs non-FIR hand-ins to avoid double-counting.
- Upgrade item tracker UI with images, quest links, and sorting.
- Add scripts for syncing quest item requirements and cleaning the catalog.
- Improve parsing for counts, FIR phrasing, and abbreviations (VPX/COFDM/RFID).
- Clean the catalog to remove phantom count-prefixed entries and duplicates.
- Purge bad item images and clear their references in items.json.
- Fix specific item counts and name normalization details.

## v1.1.6 (12/24/2025)
- Finish the compiler and build v1.1.4 for private beta.
- Add logo and ICO assets for the Windows executable.
- Add item-specific flags in each quest.
- Fill quests with item requirement flags based on quest and rewards.

## v1.1.5 (12/24/2025)
- Sync quest fields against the wiki (maps, objectives, rewards, prereqs/unlocks, Kappa) and refresh last_updated.
- Remove optional objectives from checking.json and update its timestamp.
- Refine the profile modal styling for a cleaner premium look.
- Rebuild the Upgraded from EOD section into a card-style toggle with title and badge.
- Fix profile grid markup so stats sit below form fields.
- Remove auto-update wiring and publish tooling references.
- Reintroduce electron-builder scripts and minimal Windows build config while excluding local/user data.
- Update package-lock.json for dependency changes.

## v1.1.4 (12/23/2025)
- Remake README with new logic.
- Save item tracker view state before first render.
- Remove the Any dropdown and show active filters under Maps/Traders/Quest Type.
- Keep filter dropdowns open on multi-select.
- Restore the large colored flow trader label block with centered content and depth styling.
- Adjust flow trader portrait sizing and wrap portrait + name in a centered container.
- Create the EFT achievements dataset and schema template.
- Implement Achievements view loading, toggles, and persistence.
- Add Achievements UI layout and card styling.
- Match the Achievements View on Wiki button styling to the completion toggle.
- Hide the Category line unless it is an Event and fix list icon sizing.
- Sort achievements to render completed entries after in-progress ones.
- Sort quests so completed items render after incomplete within each trader.
- Ensure achievements progress loads at startup and saves on app exit.

## v1.1.3 (12/22/2025)
- Replace item tracker buttons with a filter menu and dropdown.
- Fix future task toggle when moving between tree view and quest tracker.
- Fix failed task options logic in the tree.
- Remove terminal map from Delivery From The Past.
- Add a search bar above the mode selection for quest names.
- Hide scrollbars in map/section filters and adjust Clear Filters placement.

## v1.1.2 (12/21/2025)
- Add reload action in the profile popover to check for updates after pulling from git.
- Start item tracking for quest items.
- Add search in the item tracking menu.
- Add filter loop from quest data to split completed vs required items.
- Fix onboarding quest columns overlay with dropdowns.
- Resolve prereq/unlock matching by quest name or id.
- Remove a broken Immunity link and restore proper unlocks.
- Add the missing Immunity quest file and link it.
- Fix Fence quest handling by removing non-applicable quests.
- Remove Ref tasks that are Arena locked.
- Prevent Lightkeeper quests from being marked complete before unlock.
- Exclude Lightkeeper quests during onboarding auto-complete unless unlock is satisfied.
- Switch onboarding to a stable 3-column layout with fixed widths and ordered trader grouping.

## v1.1.1 (12/20/2025)
- Add a recommendations algorithm based on prereqs and priorities.
- Add Lightkeeper prereq tasks and tagging in internal documents.
- Create rep-regain quest logic and optional quest logic.
- Keep rep-regain and requires_failed quests hidden until requirements are met.
- Add onboarding edition selection for hiding/adding tasks.
- Add onboarding auto-complete based on what users do not input (and their level).
- Improve recommendation logic so Lightkeeper does not override Kappa priority.
- Ensure Lightkeeper quests and prereqs are tagged in recommendations.
- Fix Pets Wont Need It P2 prereq handling.
- Add onboarding options for EOD and Unheard (upgraded from EOD).
- Correct onboarding logic for task marking.
- Fix onboarding quest textbox alignment for multi-trader columns.
- Fix profile confirm reset button.

## v1.1.0 (12/18/2025)
- Grey out completed quests in the tree.
- Completing a future task auto-completes prerequisites.
- Add red overlay on future tasks to indicate locked status.
- Add left-click highlight and right-click popup on the tree.
- Add popup quest details on right-click.
- Fix prereq list marking during profile creation.
- Fix duplicated trader files and Collector prereq list entries.
- Fix profile creation menu display.
- Remove press-enter requirement during faction selection.

## v1.2 (12/17/2025)
- Improve quest tree hover view.
- Improve auto-zoom when selecting a quest in the tree.
- Add onboarding auto-complete integration on first load.
- Improve compiler for lighter app runtime.
- In progress at the time: updater system, recommendations, hideout tracking, quest item tracking, item tracking view, dashboard, achievement tracking, completed quest greying, PvE/PvP swap.

## v1.1 (12/16/2025)
- Add quest tree view and selection button.
- Add profile view.
- Add local storage based profile data.
- In progress at the time: compiler for public beta, updater, recommendations, mid-wipe start integration, hideout tracking, item tracking, dashboard, achievement tracking.
