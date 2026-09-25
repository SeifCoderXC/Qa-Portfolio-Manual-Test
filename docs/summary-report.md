# Summary — Unciv 4.22.3 desktop

| | |
|---|---|
| Product | Unciv desktop, build 4.22.3 |
| Run date | 2026-09-25 |
| Tester | Seif El Islam Bouklab |
| OS | Linux Lite (Ubuntu 24.04 family) |
| Java | OpenJDK 21.0.7 |
| Launch | `./Unciv` |
| Planned | 24 |
| Run | 24 |
| Passed | 20 |
| Failed | 0 |
| Blocked | 4 |
| Not run | 0 |
| Defects filed | 0 |

Passed: TC-001, TC-002, TC-003, TC-004, TC-005, TC-006, TC-007, TC-008, TC-009, TC-010, TC-011, TC-014, TC-015, TC-016, TC-017, TC-018, TC-019, TC-020, TC-021, TC-023.

| Case | Why it is blocked |
|---|---|
| TC-012 | Warrior had no illegal neighbour. A click on the coast did not move it. Movement stayed 2/2. |
| TC-013 | Turn 4, 3760 BC. Barbarian brutes were on the map, none adjacent to the Ottoman warrior. No attack. |
| TC-022 | New Game fields all have defaults. No required control could be cleared. |
| TC-024 | Turn-4 save has no Road tile. Owned-road movement cost was not compared. |

Regression on this build: BUG-002 (Civilopedia) was checked with TC-014 and did not reproduce. BUG-001, BUG-003, and BUG-004 were not reached. BUG-005 is blocked with TC-024.

Not tested: multiplayer, mods, Android, every civilization, late-game victory, localisation.

Jira: project UQ, epic UQ-6, 21 Done, 4 To Do, epic In Progress. The readable copy is [jira/board.md](../jira/board.md) and [jira/issues.csv](../jira/issues.csv).

TestRail: project 1, closed run 1, same totals. The readable copy is [testrail/results.csv](../testrail/results.csv).
