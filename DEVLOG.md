# Dev Log (Discord)

## 2/8/2026 - WC Tracker v1.3.2
Changes:
- Raid bring-in items respect map selection and objective progress (remaining counts).
- Raid bring-in counts for kill-with gear objectives now show 1 (bring-in).
- Quest key requirements updated for room-locked objectives and bring-in keys.
- Overlay close control supports click-out and Esc; hint is shown inside the overlay panel.
- Overlay toggle is session-only (full app restart resets it).
- Suppressed the "New quests unlocked" popup in overlay mode.
- Pinned Images control aligned with the dashboard header row.
- Recommended map scoring now weighs remaining progress and per-map objectives.
- Item progress remaining counts now refresh correctly after partial updates.
- Guided auto sync in onboarding is temporarily disabled (manual setup only).
## 1/30/2026 - WC Tracker v1.3.0
Changes:
- Faster dashboard renders by caching recommendations, visible-quest sets, and quest item needs.
- Quest item detail popups now keep tile counts synced after +/- adjustments.
- Mode selection auto-picks the only existing profile (PvP/PvE).
- Profile creation prompt is now a lightweight panel instead of a full-screen block.
- Quest tracker view now renders immediately when switching from the menu.
- Diagnostics console enabled for support (hidden unlock: title x5 + Ctrl/Cmd+Shift+D).

## 12/16/2025 - WC Tracker v1.1 Update Log
Added:
- Quest Tree View
- Quest Tree Selection Button
- Profile View
- Local Storage Based Profile Data

In progress at the time:
- Compiler for public beta access
- Updater system with interval checks
- Recommended quests algorithm
- Mid-wipe start integration
- Hideout tracking
- Item tracking
- Dynamic dashboard
- Achievement tracking

## 12/17/2025 - WC Tracker v1.2 Update Log
Added:
- Better hover view in the quest tree
- Better auto-zoom when selecting a quest in the tree
- Auto-complete integration on first load
- Compiler updates for lighter runtime

In progress at the time:
- Updater system with interval checks
- Recommended quests algorithm
- Hideout progress tracking with item additions
- Quest item reward and requirement tracking
- Item tracking view
- Dynamic dashboard
- Achievement tracking
- Completed quests greyed in the tree
- PvE and PvP view swap

## 12/17/2025 - Bug List
- Pre-req list did not mark all prerequisites correctly
- Missing and duplicated tasks in logic
- Active quests in pre-req loader showed vertically instead of grid

## 12/18/2025 - WC Tracker v1.1.0
Added:
- Completed quests in the tree are greyed out
- Completing a future task auto-completes prerequisites
- Red overlay on future tasks to show locked state
- Left click highlight and right click popup on the tree
- Popup quest info on right click
\nUpdates:\n- Pre-req list marking in profile creation
- Duplicated trader files and Collector prereq list
- Profile creation menu display
- Removed press-enter requirement during faction selection

## 12/20/2025 - WC Tracker v1.1.1
Added:
- Recommended Tasks algorithm based on prereqs and priorities
- Lightkeeper prereq tasks and tagging
- Rep-regain quest logic and optional quest logic
- Edition selection in onboarding
- Auto-complete in onboarding based on what users do not input (and their level)
\nUpdates:\n- Lightkeeper priority no longer overrides Kappa in recommendations
- Lightkeeper tag shown for quests and prereqs in recommendations
- Pets Wont Need It P2 prereqs
- Onboarding options for EOD and Unheard (upgraded from EOD)
- Onboarding logic for task marking
- Onboarding textbox alignment in multi-trader columns
- Profile confirm reset button

## 12/21/2025 - WC Tracker v1.1.2
Added:
- Reload action in the profile popover to check updates after git pull
- Start of item tracking for quest items
- Search in the item tracking menu
- Filter loop from quest data to split completed vs required items
\nUpdates:\n- Onboarding quest columns overlay with dropdowns
- Prereq/unlock matching by quest name or id
- Immunity link restored and quest file added
- Fence quest logic cleaned up
- Ref tasks removed when Arena locked
- Lightkeeper quests blocked from completion until unlocked
- Onboarding auto-complete excludes Lightkeeper quests unless unlocked
- Onboarding moved to stable 3-column layout with ordered trader grouping

## 12/22/2025 - WC Tracker v1.1.3
Added:
- Filter menu for item tracking
- Filter dropdown replacing the old menu buttons
\nUpdates:\n- Future task toggle between tree view and tracker
- Failed task options logic in the tree
- Removed terminal map from Delivery From The Past
- Added quest search bar above mode selection
- Hidden scrollbars for maps/sections and adjusted Clear Filters placement

## 12/23/2025 - Sneak Peek
- Quest layout previews (images not included in repo)

## 12/23/2025 - WC Tracker v1.1.4
Changes:
- Synced kappa-only toggles across dashboard, quest tracker, and item tracker for consistent mode switching
- Item tracker now defaults Future on at launch
- Hideout modules highlight when maxed and show a �Hideout Max Upgraded� banner when fully completed
- README remade with updated logic
- Item tracker view state saved before first render
- Removed Any dropdown and show active filters under Maps/Traders/Quest Type
- Keep filter dropdowns open on multi-select
- Restored flow trader label block styling
- Adjusted flow trader portrait sizing and centered portrait + name
- Created EFT achievements dataset and schema template
- Achievements view loading, toggles, and persistence
- Achievements UI layout and card styling
- Matched Achievements View on Wiki button styling to completion toggle
- Hid Category line unless Event and fixed list icon sizing
- Sorted achievements with completed entries after in-progress
- Sorted quests with completed after incomplete within each trader
- Achievements progress loads at startup and saves on app exit

## 12/23/2025 - Sneak Peek
- Achievements tracking preview (image not included in repo)

## 12/24/2025 - WC Tracker v1.1.5
Changes:
- Synced quest fields against the wiki and refreshed timestamps
- Removed optional objectives from checking.json
- Refined profile modal styling
- Rebuilt Upgraded from EOD toggle into a card layout
- Fixed profile grid markup
- Removed auto-update wiring and publish tooling references
- Reintroduced electron-builder scripts and minimal Windows build config
- Updated package-lock.json for dependency changes

## 12/24/2025 - Profile Edit Modal Preview
- Layout preview (image not included in repo)

## 12/24/2025 - WC Tracker v1.1.6
Changes:
- Finished the compiler and built v1.1.4 for private beta
- Added logo and ICO for the executable
- Created item-specific flags in quests
- Filled quests with item requirement flags

## 12/26/2025 - WC Tracker v1.1.7
Changes:
- Added found_in_raid_items to every quest with wiki verification
- Reworked item tracker for quest-derived FIR flags
- Built an item catalog generator
- Downloaded item images from the wiki and tracked missing pages/images
- Added normalization maps and cleanup rules for item names
- Added item_requirements to all quests and normalized FIR vs non-FIR hand-ins
- Upgraded item tracker UI with images, quest links, and sorting
- Added scripts for syncing quest item requirements and catalog
- Improved parsing for counts and abbreviations
- Cleaned the item catalog and removed duplicates
- Purged bad item images and cleared their references
- Fixed specific item counts and name normalization details

## 12/27/2025 - WC Tracker v1.1.8
Changes:
- Filled Collector.json with Kappa prereqs and rebuilt quest-directory.json
- Resynced quest item requirements and refreshed items.json
- Updated parsing/normalization in item scripts and image handling
- Added setting_priorities.json (untracked at the time)
- Dropped The Stylish One from quest data
- Normalized prereq resolution by stripping timing suffixes
- Ignored Python cache files and removed tracked pyc artifacts

## 12/28/2025 - WC Tracker v1.1.8
Changes:
- Added requires_any OR handling with auto-fail of alternate options
- Normalized prereq/unlock strings across quest JSONs
- Added item requirements for Painkiller and Colleagues - Part 3
- Cleaned item tracker duplicates and removed generic placeholders
- Removed clock dial paintings and added Taiga wiki link
- Switched image sync to tarkov.dev with better name normalization
- Rebuilt item images and refreshed catalog image paths
- Gated rep-regain items until failed requirements are met
- Expanded non-item filtering to keep objective placeholders out

## 1/1/2026 - WC Tracker v1.1.9
Changes:
- Improved onboarding quest search matching and dropdown positioning
- Stopped onboarding from auto-completing all visible quests
- Removed total counters from item tracker headers
- Fixed Safe Corridor unlock gating
- Preserved prereq hiding behavior after testing alternate onboarding logic
- Kept Lightkeeper quests locked unless they directly depend on Getting Acquainted
- Deleted guitar pick item record
- Added Pathfinder achievement and icon
- Added missing EFT achievements and merged PVE duplicates
- Downloaded new achievement icons
- Removed green header bar in profile panel
- Removed in-section Item Tracker heading and duplicate empty state heading
- Onboarding autofill starts after 3 characters
- Blocked auto-completing future quests that depend on selected prereqs
- Collector availability now requires all Kappa quests
- Excluded BTR from onboarding auto-complete and ensured rep-regain tasks follow failed requirements
- Stopped hiding prereq quests during onboarding search
- Removed duplicate Cold Blooded quest entry
- Excluded failed quests from Kappa progress and completion counts
- Item tracker status tags use quest ID visibility for active/future states
- Aligned item tracker filters with quest tracker UI
- Moved item search into filters panel and stacked above sort
- Defaulted item tracker to Active/Future on with Completed/FIR off
- Showed needed items in two-column grid when completed items are hidden
- Expanded item list viewport height and aligned tracker width

## 1/1/2026 - WC Tracker v1.2.0
Changes:
- Switched Windows build to NSIS-only installer
- Added ASAR packaging and stable artifact naming
- Added publisher/legal metadata and copyright string

## 1/2/2026 - WC Tracker v1.2.1
Changes:
- Restored onboarding prereq auto-completion for selected Ref/BTR/Lightkeeper quests while keeping level-based auto-complete excluded for those traders
- Kept Collector/Kappa gating intact during onboarding auto-completion
- Normalized completed/failed status checks to keep tree and tracker in sync
- Added Hideout Tracker placeholder view and menu entry
- Recommendations now factor in quest item requirements and FIR counts
- Recommendation cards show item badges with counts
- Recommendation scoring uses normalized, balanced factors
- Weights live in a single config block
- Downscaled item images to reduce packaged size
- Documented Next Tasks recommendations and item badges
- Updated build for v1.2.1 distribution

## 1/4/2026 - WC Tracker v1.2.2
Changes:
- Fixed quest JSON/map issues, standardized map labels (Labs/Factory), removed Arena-only limits, and normalized filters to keep renamed maps visible
- Corrected "What's on the Flash Drive?" prereq text so Shady Business, Golden Swag, and The Extortionist link properly
- Updated quest map requirements for cultist/raider/rogue objectives and reverted non-cultist map additions
- Hardened quest/progress/achievement loading against UTF-8 BOM
- Added public repo documentation set and refreshed the roadmap
- Fixed the Through Another's Eyes achievement icon reference
- Centered the onboarding quest input
- Added achievement search with refined sizing/spacing in the achievements header
- Item tracker: added reward-source lookup + counts, hid empty reward counts, and aligned counts to active/future rewards
- Item tracker: reworked two-column layout/spacing, removed extra outlines, and fixed expansion behavior
- Item tracker: moved search to the top row with aligned filters and matched rounding
- Hideout: added module groupings, selection detail panel, and icon display
- Added hideout module icon set including the ventilation fan-only icon
- Added hideout requirements data with per-level requirements and unlocks from the wiki
- Hideout requirements now show current vs next upgrade with cleaner styling and "Not Built" labels
- Hideout requirements now hide trader LL entries and use edition-based starting levels for stash/cultist circle
- Hideout modules now show built/ready styling and hide locked modules until their prerequisites are met
- Hideout unlock lists now filter to show actual unlocks while skipping requirement-only noise

## 1/5/2026 - WC Tracker v1.2.3
Changes:
- Re-synced hideout requirements/functions/timings from the wiki for full accuracy
- Filled missing hideout levels (Security, Vents, Weapon Rack)
- Cleaned hideout unlock lists to focus on real unlocks instead of requirement noise
- Added hideout upgrade button flow with saved module levels and ready/locked refresh
- Spaced out hideout reward lists for easier scanning
- Item tracker now includes all future hideout level requirements (next level as active, later levels as future)
- Item tracker now ignores currency requirements (Roubles, Dollars, Euros)
- Synced item images and refreshed item metadata from the item image fetch pass
- Added missing hideout requirement items to the catalog and refreshed their images
- Added PvP/PvE mode switching with separate progress, hideout, and achievements per mode
- Onboarding now supports per-mode setup while keeping username and edition shared
- Mode switch prompts are optional so users can keep a single profile until they opt in
- Added a session startup mode prompt to choose PvP or PvE on app open
- Replaced the default create-profile confirm with a custom modal that matches the app styling
- Remembered the last chosen mode for reloads while still prompting on fresh app starts
- Achievements now share completion across PvE/PvP by default with optional per-mode support when explicitly tagged
- Added Workbench level 3 requirements and upgrade effects
- Hideout upgrades now show "Max level reached" at the cap
- Hideout item tracker now resolves module levels from stored hideout keys and skips locked modules
- Removed Defective Wall from hideout data and related prerequisites
- Fix: removed UTF-8 BOM markers from quest data to stop build JSON parse errors

## 1/6/2026 - WC Tracker v1.2.4
Changes:
- Electron updater wiring for GitHub Releases with update modal, header/hero badges, progress, and cleaner error states
- Update checks now animate the title, time out to a clean "latest release" state, and clear timers on errors
- Manual update refresh now reloads first and then triggers the update check panel; modal sizing tightened
- Windows build metadata updated for publisher fields, updater files bundled for ASAR, version bumped to 1.2.4, and package name set to world-class-tracker
- Quest list now renders the tree even when filters hide all quests, with clearer empty-state guidance
- Onboarding only asks for edition on first profile creation, BTR auto-complete stays opt-in, and under-15 auto-complete only marks prerequisites
- Hid the quest tree edit button and disabled its toggle
- Hideout downgrade controls added with edition guardrails, moved to the current level card, and confirmation removed
- Hideout requirements/rewards now use collapsible sections with columns, inline FIR/counts, de-duplicated rewards, and clearer headers
- Hideout upgrades now enforce prerequisite modules, cascade downgrades to dependents, and show missing-upgrade tooltips with module links
- Hideout layout refinements: module grid above the detail panel, next upgrade cards styled like current, and the extra placeholder removed
- Profile panel refined with viewport clamping, read-only Mode/Faction rows, centered header, and aligned refresh styling
- Profile reset now uses a typed confirmation overlay with cancel/escape/backdrop close support
- Mode switching now uses a full-screen "Switching Profiles..." fade and returns to Quest Tracker after switching
- Moved the PvP/PvE toggle next to the menu button in the header
- Item tracker search field and progress bar background now match the achievements styling
- Progress bar fill now renders correctly over the updated background styling
- Removed the "Updated on" label from the interface
- Recommendation item scoring now matches item tracker entries by quest name or ID
- Bumped version to 1.2.5
- Set installer artifact name to WCTracker-Setup
- Updater release notes now strip HTML and the update notes scrollbar is hidden
- Updater now links to the GitHub release instead of downloading/installing, and the hero update pill was removed
- Public repo docs refreshed and roadmap reorganized to Active/Backlog/Long Term
- Prep build for 1.2.4 release

## 1/9/2026 - WC Tracker v1.2.5
Changes:
- Added the Dashboard view as the new landing hub with map-based recommended tasks
- Added quest item and hideout item panels with search filtering and hidden-scroll lists
- Added a raid items panel that pulls key items from the recommended tasks
- Reworked the dashboard into a 2x2 panel layout so all four panels stay visible
- Refreshed the map selector styling to a larger, cleaner pill
- Added a dashboard mode selector (Completion/Kappa/Lightkeeper/Prestige) to filter quest panels
- Tightened dashboard list density and spacing to fit more content at a glance

## 1/10/2026 - 1/13/2026 - WC Tracker v1.2.5
Changes:
- Reduced dashboard side padding to give panels more width
- Balanced dashboard panel heights with cleaner bottom spacing
- Dashboard lists now scroll within panels while keeping the page fixed
- Raid items now ignore placeholder key item entries
- Dashboard panels now collapse vertically per column when empty, preserving headers and empty states
- Filled key_items_required across quests for bring-into-raid requirements (keys, markers, jammers, cameras, gear, weapons)
- Cleaned key_items_required to avoid hand-over/found items so only true raid bring-ins remain
- Dashboard recommendations now show all tasks for the selected map with an Any Map option
- Dashboard cards now auto-size when lists are shorter than the panel
- Dashboard columns now shrink the smaller list by item count while the larger panel fills the remaining space
- Raid items now render in a 2-column grid for cleaner scanning
- Dashboard empty states now swap the card title instead of showing body text
- Dashboard item tiles now open a centered detail popup with quest/module breakdowns
- Recommended tasks now open a quest detail popup with a View in Tracker action
- Quest detail popup now shows full quest info (maps, prerequisites, unlocks, objectives, items, rewards)
- Quest detail popup styling tightened with no internal scroll and updated buttons
- Recommended tasks include a quick checkmark to mark a quest complete
- Added Kappa markers on dashboard recommended tasks and raid items tied to Kappa quests
- Quest items now highlight and sort to the top when the linked quest is active
- Hideout items now include all future upgrade requirements, with next-level items highlighted
- Softened highlight styling and bumped dashboard item icon sizing
- Quest detail popup now shows plain-text meta (map/type/level/trader) and hides prereq/unlock and item requirement lists
- Quest detail popup close action now uses a larger top-right X
- Standardized Farming - Part 2 objectives to combined "Find in raid and hand over" wording
- Dashboard view buttons now use a muted style so the completion checkmark stands out
- Filled key items required for weapon/gear-specific kill quests, including Setup and Decontamination Service
- Dashboard map/mode selectors now use a styled dropdown panel with Any as the default
- Recommendations now list selected map quests before Any Location entries
- Raid item panel sizing respects 2-column rows and trims extra bottom gap
- Removed the Prestige mode option from the dashboard selector
- Raid items to bring now pull their own icon set from Tarkov.dev, with a dedicated image map for dashboard use
- Removed non-item raid entries from Scrap Metal and Rigged Game key item lists
- Dashboard recommended task meta now includes map info
- Dashboard quest item counts now reflect the active mode filter
- Removed Lightkeeper from the dashboard mode selector
- Search-empty states now appear at the top of quest/hideout item panels
- Fishing Gear now tracks SV-98 and Leatherman Multitool as raid bring-ins and quest items
- Raid item sanitization now keeps non-key items for bring-into-raid tracking
- Standardized generic gear requirements to "Any" wording across relevant quests
- Silent Caliber now calls out a suppressed 12ga specifically
- Added a pistol icon override for the "Any Pistol" raid item entry
- Dashboard item detail popups now use trader portraits with chip-based metadata and View actions
- Reward item lists now use plain text styling with tighter spacing
- Kappa-only toggles now sync across dashboard, quest tracker, and item tracker
- Item tracker filters now use Kappa Only instead of Active (Active is always on)
- Dashboard map selection now resets to Any on app start
- Quest rewards spacing tightened and panel alignment refined
- Item tracker now defaults Future on at launch
- Hideout modules now highlight when maxed and show a Hideout Max Upgraded banner

## 1/14/2026-1/15/2026 - WC Tracker v1.2.6
Changes:
- Added quest images across traders (BTR Driver, Fence, Jaeger, Lightkeeper, Mechanic, Peacekeeper, Prapor, Ragman, Ref, Skier, Therapist)
- Updated Tigr Safari to require three MS2000 markers
- Quest list no longer shows thumbnails; images now appear only in quest detail views
- Dashboard quest + hideout item searches now stay in sync
- Removed duplicate Revision - Part 1/2 quest files and image sets in favor of the canonical Revision quests
- Quest detail panels now show quest images as a right-side gallery in the tracker and dashboard
- Quest detail images now use a stacked card preview with a click-to-view carousel
- Chumming now tracks Golden neck chains for item tracker (x9) and raid items (x3 per map)
- Item tracker now includes hideout requirements from locked modules (e.g., Military power filters)
- Hideout item detail popups now show the module icon (Workbench, Generator, etc.)
- Quest image viewer styling refined with a larger image panel and cleaner modal layout
- Quest image viewer now uses a view-only zoom + pan experience constrained to the frame
- Dashboard detail popups now expand to fit content (no visible scroll)
- Normalized objective text to avoid duplicate "Find" + "Hand over" lines
- Marker, camera, and signal jammer counts now match the number of objective placements
- Quest detail view now hides key items (kept for backend logic)
- Quest image viewer no longer shows scrollbars
- Downscaled oversized quest map JPGs (1920px max) to cut app size by ~22MB
- Removed the stray Reserve map entry and cleaned its related assets
- Added a Shoreline resort map image to Chemistry Closet
- Image cleanup to remove non-quest visuals and trim quest image sets
- Quest tracker cards no longer show the left green accent bar
- Quest/detail modal styling updated for a cleaner panel look
- Chemistry Closet objective now calls out East wing room 110
- Build info modified for v1.2.6 pre-release.

## 1/16/2026 - WC Tracker v1.2.7
Changes:
- Quest item partials now edit per-quest rows in item popups (counts + controls inline with each quest)
- Quest objectives show inline found counts with +/- controls instead of a separate hand-in section
- Item tracker quest rows show found/required counts with inline +/- controls (no duplicate count chip)
- Non-item objectives now support partial progress (kills, marks, extracts, etc.)
- Item progress now reconciles item name variants so counts stay synced across views
- Item tracker totals now refresh immediately after partial adjustments
- Objective progress now syncs between dashboard quest popups and the quest tracker
- Completed objective styling now strikes only the objective text (counts stay clean)
- Recommended task scoring now boosts quests with partial objective progress
- Profile panel save moved to the header; cancel removed in favor of clicking out
- Build info modified for v1.2.7 pre-release.

## 1/17/2026 - 1/18/2026 - WC Tracker v1.2.8
Changes:
- Signing and build now use Azure Trusted Signing (service principal + managed certificate profiles), with tool/setup docs, local env templating, runtime injection, a space-free executable name, and the v1.2.8 bump.
- Quest data now includes the missing Jaeger Reserve task so it appears in the tracker and onboarding, and Information Source no longer requires armor.
- Onboarding flow no longer repeats the first-launch mode prompt, and the task choice modal now shows trader portraits with hover descriptions.
- Dashboard item detail popups are clamped to the viewport with hidden scrollbars, and hideout item counts are adjustable per module.
- Quest tree now supports Kappa-only filtering with a green diamond indicator, plus a focus mode that can hide unrelated quests/edges while showing full prereq + future chains across traders.
- Quest tree focus mode suppresses Collector unless it is selected, and cross-trader link overlays exclude Collector.
- Quest tree single click highlights same-trader prereq chains; double click enters the cross-trader focus view.
- Quest tree pan/zoom behavior is based on real node extents and trader lanes, with tighter left padding, extended bottom range for BTR/Lightkeeper rows, and a width-locked baseline zoom.
- Quest tree now opens top-left from the main panel, resets to the 0% baseline, and keeps the 0% label stable.
- Roadmap refreshed with the next-up items (All Items view, in-raid overlay work, and PvP prestige flow) and removed the generic recommendation tuning entry.
- Quest choice paths can now be reset, clearing failed alternatives and dependent progress so users can backtrack.
- Update prompts now download and install updates in-app instead of linking to the release page.
- Roadmap now includes debounced save work (Active), auto-rotating backups with restore/export selection, quest tree render performance fixes, and safeguards for irreversible actions.
- Documentation now aligns with the in-app updater flow and required release assets for updates.
- Public and internal docs refreshed with the latest 1.2.8 highlights and update flow.
- Roadmap now includes a quest tree grid/camera correctness pass to keep alignment polished.
- Contributor guidelines removed to keep docs aligned with a solo-maintained project.
- Resources menu now includes a Discord invite link.
- Action buttons now register reliably on the first press.
- Added a full-screen loading cover on launch and made profile switch/mode selection overlays fully opaque.

## 1/19/2026 - 1/20/2026 - WC Tracker v1.2.9
Changes:
Discord bot prep:
- Quest directory metadata now skips rewrites when unchanged to avoid build churn.
- Added a Discord bot workspace and drafted the role-gated auth implementation plan.

Website:
- Added a one-page landing site with a centered WC Tracker wordmark, beta corner brace, scroll hint, and Discord CTA.
- Reworked the hero typography and palette to match the in-app styling while keeping the layout minimal.
- Added scheduled version sync so the beta label auto-updates from the latest public release.
- Kept additional website assets in repo for future iteration while excluding them from builds.

App + data:
- Added a VERSION file and updated Discord devlog notifications to include the current dev target version in the header.
- Bumped the dev target version to 1.3.0 for Discord devlog headers.
- Bumped the app version to 1.2.9 to align updater builds.
- Added a backlog item for installer UI/branding polish.
- Build packaging now excludes internal docs and local tooling from the app bundle.
- Release notes and public docs refreshed for the v1.2.9 build.
- Quest detail completion now closes the dashboard modal, and ready-to-complete quests pulse in the tracker and dashboard.
- Onboarding now includes a back action so profiles can be corrected mid-setup.
- Quest tree single-click highlighting now stays within the same trader so cross-trader links only appear in focus mode.
- Touch input now maps to primary button clicks for header and dashboard controls.
- Objective count parsing now ignores model numbers so marker tasks don't inflate required counts.
- Objective count parsing now ignores distance and location numbers so task targets stay accurate.
- Objective count parsing now handles win/out-of phrasing and ignores part/level markers in objectives.
- Item tracker now uses a single auto-allocate add/remove control per item and removes duplicate requirement listings in item details.
- Added an item short-name alias dataset (with collision tracking) to prep OCR matching against in-game UI labels.
- Added a click fallback delay to prevent stepper controls from double-advancing on press.
- Suppressed delayed touch clicks when the native tap event already fired to stop double increments.
- Updated the large beef stew item label to use the plural form.
- Chumming now tracks the full 9 Golden neck chains in the item tracker.
- Health Care Privacy - Part 5 now tracks the Gunpowder "Kite" hand-ins in the item tracker.
- Mode selection and profile creation prompts now always use a full black backdrop and appear every app launch.
- Onboarding back button styling refreshed and centered.
- Added a back exit on the first onboarding step so profile setup can return to mode selection.
- Onboarding action layout now centers the footer controls with matched button sizing.
- Pharmacist now lists the Dorm room 114 key as a required raid item.
- Dorm room 114 key now uses the same raid item image as Tarcone Director's office key.
- Dashboard now opens by default on refresh and when switching profiles.
- Onboarding buttons now share consistent sizing and styling across the flow steps.
- Onboarding buttons now share a unified color treatment across all steps.
- Back button sizing reduced to stay lighter in the onboarding footer.
- Onboarding buttons now use a single unified hover/active treatment for a cleaner step flow.
- Mode selection buttons now show the profile level (or N/A) under PvP/PvE.
- Mode selection buttons now use hover-only emphasis with updated styling.
- Raid items now stay in a simple two-column list and sort by quest order to keep related items adjacent.
- Option-based quests no longer re-surface their alternate choice once a failed branch is set.
- Raid items now use quest-based outline colors to keep same-quest items visually grouped.
- Raid item quest colors now include a subtle glow for better visibility.
- Quest item progress adjustments no longer flash the quest detail popup.
- Dashboard map selection now includes a recommended entry based on active task density for the current mode.
- General Wares objective copy now merges the find/hand-in wording into a single line.
- Car Repair objectives now use combined find/hand-in wording per item.
- Merged find + hand-in objectives for item quests where both lines already referenced the same item.
- Dashboard quest-item detail view now respects quest state so "View" jumps to future/completed quests correctly.
- Switching to Hideout or Item Tracker no longer bounces back to the dashboard when onboarding is already closed.
- Onboarding labels and hints now use consistent sizing and spacing for readability.
- Onboarding sync step now centers status, hints, and actions for clearer guided flow.
- Quest sync overlay now anchors top-right, grows into two columns after ten items, and preserves capture order without scrollbars.
- Quest sync OCR now crops to the left task pane to reduce stray captures.
- OCR worker initialization now prefers reinitialize and filters noisy Tesseract warnings during capture.
- Quest sync capture now uses OCR line confidence and requires stable repeats before adding quests.
- Quest sync capture now stabilizes per visible line slot and inserts new quests in-screen order.
- Onboarding progress no longer saves mid-flow; profile data writes only after completion.
- Onboarding quest sync now uses hover capture with a cursor-based OCR window and left-pane guardrails.
- Onboarding sync list is now removable in-app and uses a side-by-side control + list layout.
- Quest sync overlay now flashes a green box over detected quest lines.
- Removed the Enter-to-continue hint from the fresh wipe onboarding step.
- Onboarding now asks for edition right after name, with shared name/edition skipped for new mode profiles.
- Fresh wipe onboarding auto-fills level 1 when the level step opens.
- Onboarding quest sync no longer blocks on Tarkov running, so offline testing works.
- Onboarding quest sync keeps the overlay visible even when the toggle is off.
- Quest sync now auto-starts with a single Start/Stop toggle and runs at ~5 captures per second.
- Quest sync status stays on Scanning with brief Found confirmations for new captures.
- Quest capture region now sits fully to the right of the cursor and the preview box is hidden.
- Quest sync now matches numbered quests (including roman numerals) to the correct part.
- Quest sync OCR now accepts question marks and uses relaxed matching for short quest lines.
- Guided sync list now matches the manual trader-grouped layout.
- Switching to manual now carries over any quests already captured.
- Confirming quest sync now closes the overlay immediately.
- Added a fresh-profile dev launch option that uses a separate test profile and resets it on start.
- Completed quests in the tree no longer reveal cross-trader links unless focus mode is active.
- Inactive overlay now opens a semi-transparent dashboard-only view with the same sections as the main dashboard.
- Quest sync capture area was enlarged and the preview box is visible again for alignment.
- Quest sync capture area reduced by 20% to improve responsiveness and accuracy.
- Quest sync capture now runs ~3x per second and waits for the cursor to settle before capturing.
- Quest sync capture now runs ~10x per second with a more forgiving cursor-still threshold.
- Fresh wipe onboarding now skips the level prompt and auto-sets level 1.
- Quest sync onboarding no longer requires holding the cursor still before capture.
- Quest sync capture now refuses off-screen crop positions so it only reads inside the visible box.
- Quest sync overlay now hides the capture box highlight and places the confirmation checkmark above-right of the cursor.
- Quest sync overlay now balances captured quests evenly across two columns and updates the cursor guidance copy.
- Quest sync capture now waits for stable repeats before adding a quest to reduce false positives.
- Quest completion no longer forces the view back to the dashboard.
- Quest tree zoom now centers on the cursor position when scrolling.
- Inactive overlay now renders inside a rounded, semi-transparent panel with margins and supports ESC to close.
- Dashboard view buttons now open the quest detail popup again instead of switching views.
- Clicking a dashboard quest preview now jumps to the quest tracker, while View opens the popup.
- General Wares now uses No Location to avoid map-based duplication.
- Dashboard quest previews are no longer clickable; use View to open the popup and View in Tracker from there.
- View in Tree now closes the quest popup after opening the quest tree.
- Overlay dashboard now stays open when toggled and uses a fully transparent backdrop with the semi-transparent panel styling.
- Quest completion now reuses cached quest dependency maps to reduce UI lag.
- Quest tree rendering is skipped unless the tree view is active to speed up non-tree actions.
- Quest sync overlay guidance now matches the right-of-text capture direction.
- Quest sync matching now requires higher OCR confidence and stronger token overlap to reduce false positives.
- Quest sync capture width increased to better read longer quest names.
- Quest sync overlay hint now instructs a slow sweep past quest names and is bolded for visibility.
- Quest sync OCR now strips bracketed zone tags like [PvP Zone]/[PvE Zone] before matching quest names.
- Quest sync overlay now shows a temporary �Reading �� status line to reveal what OCR sees before confirmation.
- Quest sync capture height increased to pick up the extra zone tag line.
- Overlay mode now hides the loading spinner backdrop for faster open.
- Overlay now restores its last image viewer state per session without affecting the main app.
- Overlay dashboard now mirrors the app�s active PvP/PvE mode and updates when the app mode changes.
- Fixed early init errors in overlay mode caused by debug and mode helpers loading too late.
- Quest sync status now holds the last OCR line until a new scan, so the readout stays visible.
- Quest sync now accepts stable repeats by quest name even if the OCR line shifts position.
- Quest sync OCR now uses a multi-line page segmentation mode and a taller capture box for wrapped quest names.
- Quest sync now strips PvP/PvE zone-only lines and allows a lower match threshold for Ref quests.
- App loading overlay now waits briefly before showing and stays hidden when load is instant.
- Overlay dashboard edits now sync back to the main app instantly.
- Overlay dashboard now opens centered with fixed max dimensions and no startup loading splash.
- Overlay detection now treats Tarkov Arena as a supported process for testing.
- Overlay no longer prompts for PvP/PvE selection and instead relies on the app�s active mode.
- Mode-switch loading overlay is now suppressed in overlay mode so it opens instantly.
- Overlay now skips building non-dashboard views to prevent the quest list flash on hotkey open.
- Item and objective progress updates now debounce disk writes and UI renders to reduce +/� lag.
- Overlay mode now applies its layout class before the page paints to avoid the brief quest-list flash.
- Quest list rendering now runs only while the quest tracker view is active to reduce click lag.
- Added temporary performance timing logs in the diagnostics console to identify slow render paths.
- Item progress buttons now avoid duplicate dashboard/item tracker renders, and item tracker rendering only runs when that view is active.
- Disabled DevTools shortcuts and removed the hidden diagnostics console access in production builds.

- Discord devlog webhook now derives the next dev version from the latest public release tag automatically.
- Discord devlog now ignores non-semver tags (like beta labels) when computing the next version.
- Discord devlog now reads GitHub “latest release” to pick the correct version source before bumping.
- Discord devlog now authenticates GitHub API requests and falls back to semver tags if the API is unavailable.
- Discord devlog now reads the version directly from the public dev log in this repo.
- Fixed devlog version parsing to read vX.Y.Z from the public dev log for Discord posts.
- Overlay now targets the active Tarkov display only and can be re-opened after Esc close during a run.
- Overlay hotkey now re-checks Tarkov state on open so Esc close can reopen reliably.
- Overlay hotkey can reopen even after the base overlay window was closed.
- Quest tree zoom now anchors to the cursor without shifting pan limits.
- Quest tree focus mode now only exits when re-clicking the focused quest (no more clearing on pan/move).
- Quest tree single/double click now switches focus directly between quests; only empty space keeps the current focus.
- Mode creation now jumps straight into onboarding without re-asking PvP/PvE.
- New mode profiles now always enter onboarding immediately instead of returning to the mode selector.
- New mode profile creation now jumps into onboarding immediately without a second click.
- Onboarding OCR capture now reads to the left of the cursor, matching the guide instructions.
- Dashboard now supports pinning quest images and viewing them together in a pinned gallery.
- Pinned images control now matches dashboard styling and aligns to the right header actions.
- Pinned images control now aligns to the right column edge in the dashboard header.
- Pinned images notice now floats under the button so the button aligns cleanly to the right edge.
- Empty pinned state now shows a visible callout above the button on both app and overlay dashboards.
- Pinned empty-state callout now forces visibility to avoid getting lost in the layout.
- Pinned empty-state callout now appears to the left of the button with a side connector.
- Quest image viewer now centers the quest title in the header.
- Quest detail image pin button now anchors visibly to the top-right of the image.
- Quest image viewer now fills the star icon when pinned and highlights the button in green.
- Quest image viewer pin button now toggles pinning and updates the pinned gallery.
- Pinned gallery now includes an unpin button and keeps saved pins between sessions.
- Pinned star highlight now uses a tighter glow and brighter green fill.
- Ctrl+R refresh now keeps the current view state until the app is fully closed.
- Ctrl+R refresh now keeps the PvP/PvE session selection instead of re-prompting.
- Ctrl+R refresh now preserves open pinned/quest image/quest detail panels.
- Pinned images panel now uses a larger modal with tighter margins.
- Pinned gallery tiles now fill edge-to-edge with top-right unpin control and bottom-left labels.
- Pinned gallery overlays now anchor to each image frame so labels/buttons sit on the image.
- Pinned gallery overlays now lock to the actual rendered image bounds for consistent placement.
- Pinned gallery header now overlays the grid so images fill the full panel.
- Pinned star highlight now uses the main green and a tighter outline glow.
- Pinned star now fills without disappearing and uses a thinner outline glow.
- Fixed pinned star icon resetting when toggling.
- Pinned star now matches the highlight green for consistent color.
- Pinned star no longer changes the button background color when active.
- Pinned icon now updates per image as you navigate the viewer.
- Pinned gallery now uses a tight masonry layout with full images and small gaps.
- Pinned images now persist across Ctrl+R refreshes.
- Removed the yellow focus highlight from the pin button.
- Pinned gallery now reflows after images load so sizing stays tight and consistent.
- Pinned gallery now balances row heights to keep image sizes more even.
- Pinned gallery now uses a freeform packing layout to maximize image size without columns.
- Pinned gallery packing now prefers best-fit placement for cleaner tetris-like layouts.
- Pinned gallery now scales packed layouts to fully fill the available space.
- Pinned gallery now falls back to portrait-aware layouting to avoid large gaps.
- Overlay dashboard now removes the close X and shows an inline Esc/click-outside close hint.
- Overlay toggle now shows a hotkey tip in the header when enabled.
- Pinned gallery now opens faster when ratios are cached to reduce startup lag.
- Pinned images panel is now ~15% larger to maximize visible space.
- Onboarding quest sync preview now stays solid and locked to the left of the cursor.
- Overlay hotkey hint now appears as a timed dropdown with a progress bar.
- Pinned images close button now aligns to equal top/right margins with a circular frame.
- Quest sync preview now stays solid during capture and remains anchored to the left of the cursor.
- Quest sync OCR worker now auto-retries after worker crashes to prevent postMessage errors.
