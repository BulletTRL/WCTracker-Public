# Dev Log (Discord)

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
- Hideout modules highlight when maxed and show a “Hideout Max Upgraded” banner when fully completed
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
