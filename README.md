# Unciv 4.22.3 — manual QA

Independent test of the open-source game [Unciv](https://github.com/yairm210/Unciv), desktop build 4.22.3, run on 25 September 2026.

This is not employment and not affiliated with the Unciv maintainers. It is a finished manual-QA pack: requirements, test plan, 24 cases, a full execution, screenshots, Jira, and TestRail.

**Tester:** Seif El Islam Bouklab
**Machine:** Linux Lite (Ubuntu 24.04), OpenJDK 21.0.7, 1366×768, English UI, no mods
**Launch:** `./Unciv`

The written step for TC-001 still says `java -jar Unciv.jar`. On this PC that command has no display, so the run used the native launcher. The main menu showed version 4.22.3.

## Result

| Planned | Run | Passed | Failed | Blocked | Not run | Defects filed |
|---|---|---|---|---|---|---|
| 24 | 24 | 20 | 0 | 4 | 0 | 0 |

Jira project UQ and TestRail run 1 hold the same totals. Both sites ask for a login. The files in this repository are the copy a reviewer can open.

## What was covered

Launch and the main menu, New Game, a tiny map with one AI opponent, first-turn controls, a game with no mods, founding a city, queuing production and changing it, choosing a technology and keeping it across a turn, moving a unit, save, load, and continue after quit, an option kept after restart, resizing the window, Civilopedia open and close, an empty save name, and the smallest map the screen allows.

## Blocked, not defects

- **TC-012** — the warrior had no illegal neighbour, so a refused move could not be observed.
- **TC-013** — barbarians were on the map by turn 4, and none were adjacent, so no attack was made.
- **TC-022** — New Game fields all have defaults, so an empty required field could not be submitted.
- **TC-024** — no road tile by turn 4, so owned-road movement cost was not measured.

## Regression

The five files in [bugs/](bugs/) are checks rewritten from the official 4.21 and 4.22 release notes. They are not bugs found in this run. On this build the Civilopedia stall (BUG-002) was checked in TC-014 and did not reproduce. BUG-001, BUG-003, and BUG-004 were not reached. BUG-005 stayed blocked with TC-024.

Out of scope, and not claimed: multiplayer, mods, Android, automation, performance testing, and an ISTQB certificate.

## Where to read it

| File | What it is |
|---|---|
| [jira/board.md](jira/board.md) | Every Jira issue: status, steps, expected, actual, and the screenshot |
| [jira/issues.csv](jira/issues.csv) | The same 26 issues in a spreadsheet |
| [testrail/results.csv](testrail/results.csv) | Closed TestRail run, one row per case |
| [tests/test-cases.csv](tests/test-cases.csv) | The 24 cases with the result filled in |
| [docs/summary-report.md](docs/summary-report.md) | One-page report |
| [docs/test-plan.md](docs/test-plan.md) | Scope, risks, and exit |
| [docs/execution-log.md](docs/execution-log.md) | Time and evidence for each case |
| [evidence/test-run.xlsx](evidence/test-run.xlsx) | Execution workbook |
| [evidence/eod-report.pdf](evidence/eod-report.pdf) | End-of-day counts |

## Line for a CV

Manual QA of Unciv 4.22.3 (open-source desktop game): designed and executed 24 test cases on Linux, recorded the results in Jira and TestRail — 20 passed, 4 blocked, no defects filed. https://github.com/SeifCoderXC/Qa-Portfolio-Manual-Test
