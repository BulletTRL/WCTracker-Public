# Overlay Compliance Notes (Tarkov)

This document captures our intent, constraints, and decisions to keep any display-only overlay legit and compliant. It is a summary of discussions and planned boundaries, not legal advice.

## Scope
- Target: Escape from Tarkov with BattlEye enabled.
- Overlay type: display-only, out-of-process, click-through.
- Game mode: borderless windowed is mandatory for overlay behavior.

## Non-Negotiables
- No injection, no hooks, no in-process rendering.
- No reading game memory or scanning the process.
- No kernel drivers or privileged access.
- No automation that plays the game for the user.
- No anti-cheat bypasses or evasion attempts.

## Allowed Surface Area (If Permitted by Policy)
- Separate always-on-top window that does not capture input.
- OS-level window management only (position/size tracking).
- Screen capture + OCR only if explicitly allowed by game and BattlEye policy.
- Public data sources (wiki, official APIs, user-provided notes).

## Disallowed Surface Area
- DLL injection or swap-chain hooks (DirectX/Vulkan/OpenGL).
- Overlay rendering inside the game process.
- Memory reads, file patching, or tampering with the game.
- Hidden data extraction, packet inspection, or network interception.

## Compliance Checklist
- Verify Escape from Tarkov ToS and BattlEye policy for overlays.
- Seek explicit approval or guidance from BattlEye or Battlestate Games.
- Document the exact overlay behavior and data sources used.
- Provide a public disclaimer that the app is a community tool, not affiliated.
- If approval is denied or unclear, do not ship the overlay.

## Go/No-Go Acceptance Checklist
- [ ] Written policy guidance permits the overlay approach.
- [ ] Overlay is strictly out-of-process (no injection, no hooks, no memory reads).
- [ ] Overlay is read-only and never sends input or automation.
- [ ] Click-through behavior is verified (no input interception).
- [ ] Overlay is limited to borderless windowed mode.
- [ ] Data sources are documented and approved (no hidden or private data).
- [ ] Public disclosure and disclaimers are up to date.
- [ ] Compliance evidence is captured and stored.

## Evidence to Keep (Proof of Intent)
- Written notes showing the no-injection, no-memory-read stance.
- Architecture summary demonstrating out-of-process rendering only.
- List of data sources and confirmation they are public.
- Any written approvals or responses from BattlEye or Battlestate Games.
- Test notes showing the overlay does not capture input or modify the game.

## Decision Log (Summary of Conversations)
- We confirmed BattlEye is in use and must be respected.
- We agreed the overlay must be display-only and out-of-process.
- We agreed borderless windowed mode is required for overlay stability.
- We explicitly rejected any injection, hooks, or memory access.
- We stated this must be legit with no bypass or evasion attempts.

## Implementation Plan (Legit-Only)
### Phase 1: Policy Gate
- Collect official guidance for Tarkov + BattlEye on overlays, screen capture, and OCR.
- If guidance is unclear, request written confirmation and wait for a response before shipping.
- Document allowed vs disallowed behaviors in a public-facing summary.

### Phase 2: Architecture (Out-of-Process)
- Overlay runs as a separate window/process with zero interaction with the game process.
- Overlay window is transparent, always on top, and click-through.
- Data flow is one-way: the app renders info it already knows or that the user provides.

### Phase 3: Window Tracking
- Detect the Tarkov window and sync position/size.
- Re-align on display changes, resolution swaps, and focus changes.
- Hide overlay if the game is not active or not in borderless windowed mode.

### Phase 4: Data Sources
- Primary: app data (quests, items, progress, user inputs).
- Optional (only if allowed): screen capture + OCR for on-screen text.
- No memory reads, no injection, no hooks, no network interception.

### Phase 5: UX + Safety
- Make overlay read-only, no input capture.
- Provide a clear toggle and visibility state.
- Expose a "compliance mode" banner when the overlay is active.

### Phase 6: Validation
- Confirm overlay does not hook, inject, or read process memory.
- Record test notes proving click-through behavior and out-of-process rendering.
- Verify no performance impact or rendering artifacts in borderless mode.

### Phase 7: Release Gate
- Do not ship without policy confirmation.
- Provide a clear disclaimer and data-source summary in the public docs.

## Research Needed (To Be Collected)
- Tarkov ToS statements relevant to overlays/screen capture/OCR.
- BattlEye policy or guidance on external overlays.
- Any public developer posts or approvals for similar tools (citations + dates).

## RatScanner Review (Pending Sources)
## RatScanner Review (Source-Based Summary)
This summary is based only on their public documentation and is not an endorsement or a compliance guarantee.

### What RatScanner says it does
- External tool that does not access game memory.
- Captures a screenshot, applies image processing, identifies the item, then displays results in its window and as an overlay tooltip.
- Uses a third-party API (tarkov.dev) for item data.
- Notes borderless or windowed mode may be required for overlay behavior.

### Anti-cheat related statement (their claim)
- They state no proven bans from RatScanner usage to date, while noting the project is not affiliated with Battlestate Games.

### Sources
- RatScanner README: https://raw.githubusercontent.com/RatScanner/RatScanner/master/README.md
- RatScanner FAQ: https://raw.githubusercontent.com/RatScanner/RatScanner/master/FAQ.md
