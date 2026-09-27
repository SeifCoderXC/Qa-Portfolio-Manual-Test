# Unciv 4.22.3 — manual test report

Seif El Islam Bouklab, I tested the desktop build of [Unciv](https://github.com/yairm210/Unciv) 4.22.3. Unciv is an open-source strategy game. This test is independent and is not affiliated with the maintainers.

**Environment:** Linux Lite (Ubuntu 24.04), OpenJDK 21.0.7, 1366×768, English UI, no mods
**Launch:** `./Unciv`

`java -jar Unciv.jar` did not open a window on this machine, so the run used the native launcher. The main menu showed version 4.22.3.

## Result

| Planned | Run | Passed | Failed | Blocked | Not run | Defects filed |
|---|---|---|---|---|---|---|
| 24 | 24 | 20 | 0 | 4 | 0 | 0 |

The same totals are in Jira project UQ and in TestRail run 1. On the Jira board, passed work is Closed, the four blocked cases are Open, and the epic is In Progress. Both sites require an account. This repository holds the cases, the results, and the screenshots.

## What was tested

Launch and the main menu, New Game, a tiny map with one AI opponent, first-turn controls, a game with no mods, founding a city, queuing production and changing it, choosing a technology and keeping it across a turn, moving a unit, save, load, and continue after quit, an option kept after restart, resizing the window, Civilopedia open and close, an empty save name, and the smallest map the screen allows.

## Blocked

These four cases did not fail. The condition they needed was not on the board.

- **TC-012** — the warrior had no illegal neighbour, so a refused move could not be observed.
- **TC-013** — barbarians were on the map by turn 4, and none were adjacent, so no attack was made.
- **TC-022** — New Game fields all have defaults, so an empty required field could not be submitted.
- **TC-024** — no road tile by turn 4, so owned-road movement cost was not measured.

## Release checks

The files in [bugs/](bugs/) are checks taken from the official 4.21 and 4.22 release notes. They are not defects found in this run. On this build the Civilopedia stall (BUG-002) was checked in TC-014 and did not reproduce. BUG-001, BUG-003, and BUG-004 were not reached. BUG-005 stayed blocked with TC-024.

Not part of this run: multiplayer, mods, Android, automation, and performance testing.

## Where to read it

| File | Contents |
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
