# Test Plan — Unciv desktop

**Author:** Seif El Islam Bouklab  
**Date:** 2026-09-24  
**Status:** Execution complete on 2026-09-25. 24 run, 20 passed, 4 blocked, 0 failed, 0 defects.

## 1. Purpose and scope

Confirm that a player can install the public desktop build, start a small single-player game, play the first city/tech/unit loop, and save/load without losing the match.

In: main menu, New Game, first 20–40 turns on a tiny map vs AI, city production, tech picker, unit move, one combat if a barbarian or AI unit is adjacent, save/load/continue, options, window resize, Civilopedia open/close.

Out: multiplayer server, ranked play, every civ, every map script, mods, Android store build, Gradle unit tests, performance soak, security, full localisation.

## 2. System under test

Unciv — open-source Civ-style 4X (Kotlin / libGDX). Desktop jar from itch or GitHub. JVM 17+ (tester has 21).

## 3. Test approach

System-level manual testing.

| Type | Where |
|---|---|
| Smoke | TC-001–005 |
| Functional | cities, tech, units, persist |
| Boundary | smallest map / fewest opponents the UI allows |
| Negative | start with incomplete New Game choices if the UI allows it; load missing name |
| Usability | resize, blocked controls, Civilopedia |
| Confirmation / regression | bugs in `/bugs` taken from 4.21–4.22 release notes |

Exploratory charters were written (`docs/exploratory-charters.md`). This run executed the 24 cases and did not log a separate charter session.

No automation in this pack. One Playwright script on a public website is a different folder, later.

## 4. Risk analysis

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| New Game hangs on map gen | Medium | Critical | Smoke on tiny map first; 4.22.0 already “start fresh if latest start is erroring” |
| Save/load mismatch | Medium | Critical | Named save + reload + check turn number |
| Civilopedia / tech picker ANR | Medium | Major | Open/close only; do not scroll for minutes |
| City screen double-control crash | Low | Major | Regression BUG-003 |
| Options written to UI but not applied | Medium | Major | Change autosave, restart, read back |
| Mods leak into a “clean” game | Medium | Major | Mods off for the whole pack |
| Java 21 vs documented 17 | Low | Major | Launch smoke first |

## 5. Entry and exit

Entry: jar launches, version string readable, no mods, Java 21 recorded.

Exit for the *analysis* pack: plan, 24 cases, traceability, five regression reports, three charters.

Exit for the execution pass: all 24 cases run on the tester PC. Met on 2026-09-25. Smoke TC-001–005 and persist TC-018–020 passed. Four cases are blocked, recorded as tasks, not defects. No defect was seen, so none was filed.

## 6. Environment and tools

See `env/ENVIRONMENT.md`. Evidence: window screenshots and a copy of the `.json` save. `lasterror.txt` if the process dies.

## 7. Deliverables

Test plan, requirements, cases, traceability, execution log, summary, exploratory charters, defect reports.

## 8. Traceability

`tests/traceability.csv` — every REQ has at least one TC.
