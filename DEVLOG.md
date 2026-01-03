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

