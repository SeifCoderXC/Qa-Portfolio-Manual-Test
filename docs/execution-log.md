# Execution log

Build Unciv 4.22.3. Tester Seif El Islam Bouklab. Date 2026-09-25.

The 2026-09-24 rows were the analysis pass only. The table below is the executed run.

| TC | Jira | Title | Status | Finished | Evidence |
|---|---|---|---|---|---|
| TC-001 | UQ-7 | Launch reaches main menu | Pass | 2026-09-25 00:09 | `../evidence/screenshots/2026-09-25_0009_TC001_main-menu.png` |
| TC-002 | UQ-8 | New Game screen opens | Pass | 2026-09-25 00:13 | `../evidence/screenshots/2026-09-25_0013_TC002_newgame-screen.png` |
| TC-003 | UQ-9 | Start a tiny single-player game | Pass | 2026-09-25 00:14 | `../evidence/screenshots/2026-09-25_0014_TC003_game-started.png` |
| TC-004 | UQ-10 | First turn controls exist | Pass | 2026-09-25 00:15 | `../evidence/screenshots/2026-09-25_0015_TC004_first-turn-controls.png` |
| TC-005 | UQ-11 | New Game with no mods | Pass | 2026-09-25 00:14 | `../evidence/screenshots/2026-09-25_0014_TC003_game-started.png` |
| TC-006 | UQ-12 | Found a city with the settler | Pass | 2026-09-25 00:22 | `../evidence/screenshots/2026-09-25_0022_TC006_city-founded.png` |
| TC-007 | UQ-13 | Queue a production item | Pass | 2026-09-25 00:23 | `../evidence/screenshots/2026-09-25_0023_TC007_queued.png` |
| TC-008 | UQ-14 | Change production before completion | Pass | 2026-09-25 01:27 | `../evidence/screenshots/2026-09-25_0127_TC008-reopened-monument.png` |
| TC-009 | UQ-15 | Open tech picker and select a tech | Pass | 2026-09-25 00:25 | `../evidence/screenshots/2026-09-25_0025_TC009-step3_backtomap.png` |
| TC-010 | UQ-16 | Research selection survives Next Turn | Pass | 2026-09-25 01:31 | `../evidence/screenshots/2026-09-25_0131_TC010-after-turn.png` |
| TC-011 | UQ-17 | Move a unit one tile | Pass | 2026-09-25 00:26 | `../evidence/screenshots/2026-09-25_0026_TC011_moved-confirm.png` |
| TC-012 | UQ-2 | Unit cannot enter illegal tile | Blocked | 2026-09-25 01:33 | `../evidence/screenshots/2026-09-25_0133_TC012-water-click.png` |
| TC-013 | UQ-3 | Attack an adjacent hostile if present | Blocked | 2026-09-25 01:49 | `../evidence/screenshots/2026-09-25_0149_back-to-map.png` |
| TC-014 | UQ-18 | Civilopedia opens and closes | Pass | 2026-09-25 00:27 | `../evidence/screenshots/2026-09-25_0027_TC014_closed-responsive.png` |
| TC-015 | UQ-19 | Resize window mid-game | Pass | 2026-09-25 01:35 | `../evidence/screenshots/2026-09-25_0136_TC015-small-clicked.png` |
| TC-016 | UQ-20 | Change an option and read it back | Pass | 2026-09-25 00:28 | `../evidence/screenshots/2026-09-25_0028_TC016_reopened-persists.png` |
| TC-017 | UQ-21 | Option survives restart | Pass | 2026-09-25 01:05 | `../evidence/screenshots/2026-09-25_0103_TC017_checkbox-zoom.png` |
| TC-018 | UQ-22 | Save a named game | Pass | 2026-09-25 00:17 | `../evidence/screenshots/2026-09-25_0017_TC018_saved.png` |
| TC-019 | UQ-23 | Load the named save | Pass | 2026-09-25 00:19 | `../evidence/screenshots/2026-09-25_0019_TC019_loaded-match.png` |
| TC-020 | UQ-24 | Continue after quit | Pass | 2026-09-25 00:21 | `../evidence/screenshots/2026-09-25_0021_TC020_resumed-match.png` |
| TC-021 | UQ-25 | Smallest map still playable | Pass | 2026-09-25 00:22 | `../evidence/screenshots/2026-09-25_0022_TC006_city-founded.png` |
| TC-022 | UQ-4 | Start blocked when a required choice is empty | Blocked | 2026-09-25 00:14 | `../evidence/screenshots/2026-09-25_0013_TC002_newgame-screen.png` |
| TC-023 | UQ-26 | Save name rejected or trimmed if empty | Pass | 2026-09-25 01:40 | `../evidence/screenshots/2026-09-25_0140_TC023-after-enter.png` |
| TC-024 | UQ-5 | Owned roads not charged as neutral — regression | Blocked | 2026-09-25 01:49 | `../evidence/saves/Autosave-turn4.json` |

## Notes

**TC-001** (Pass). Main menu clean, no crash dialog, version readable bottom-center

**TC-002** (Pass). Game Options / Map Options / Civilizations all present

**TC-003** (Pass). Tiny map, 1 human + 1 AI, Chieftain. Left New Game screen, map shown, no freeze.

**TC-004** (Pass). Settler auto-selected with Found-city prompt; Next unit (2 idle) visible/enabled

**TC-005** (Pass). No mods installed; game started on base Gods & Kings ruleset with no missing-mod dialog (cross-ref TC-003 evidence)

**TC-006** (Pass). City Istanbul founded; banner and stats visible

**TC-007** (Pass). Warrior queued as current construction, production panel highlighted green

**TC-008** (Pass). Warrior was current. Monument added, Warrior removed. Reopened city: Monument still current, queue empty.

**TC-009** (Pass). Pottery selected as current research, shown in top-left tech panel with progress

**TC-010** (Pass). Pottery was current at 0/22. After one Next turn it was still Pottery at 4/22.

**TC-011** (Pass). Warrior moved to Cattle tile, movement 2/2 -> 1/2

**TC-012** (Blocked). Selected warrior's six neighbours are land. Visible coast is next to the city, not the warrior. Double-click on that coast left the warrior at 2/2. No crash. No illegal neighbour to refuse.

**TC-013** (Blocked). Turn 4, 3760 BC. Barbarian Brutes at (1,-7) and (3,6). Ottoman warrior at (-2,5). Greece warrior at (2,-2). None adjacent. No attack. Worked-tiles tutorial kept stealing later Next-turn clicks.

**TC-014** (Pass). Opened Civilopedia, opened Contact Me entry, closed back to game screen; UI stayed responsive

**TC-015** (Pass). Window reduced to about 960x600, map and buttons redrawn, a tile click still registered. Restored to 1366x713. UI still usable.

**TC-016** (Pass). Toggled 'Ask for confirmation when pressing next turn' ON, closed+reopened Options, value still checked

**TC-017** (Pass). Ask for confirmation when pressing next turn still checked after quit and relaunch. Checkbox-center luminance 75.6 on the post-restart shot, matching the checked shot (74.5) and not the unchecked shot (46.3). GameSettings confirmNextTurn=true.

**TC-018** (Pass). Saved as QA-20260925; file confirmed at SaveFiles/QA-20260925, copied to ../evidence/saves/QA-20260925.json

**TC-019** (Pass). Loaded QA-20260925; turn 0/4000BC, Found-a-city prompt, same units match pre-save state

**TC-020** (Pass). Process fully exited via in-game Exit (confirmed via ps), relaunched, Resume loaded identical turn 0/4000BC state

**TC-021** (Pass). Same match as TC-003: Tiny map, 1 human + 1 AI, Chieftain. City Istanbul founded (TC-006). Map stayed playable through turn 4.

**TC-022** (Blocked). N/A. New Game fields seen on TC-002/TC-003 all have defaults (civ, difficulty, map size, AI count). No required control could be cleared to empty.

**TC-023** (Pass). Save dialog name cleared. Enter did not create a file. No zero-byte save. Process stayed up. Existing saves unchanged.

**TC-024** (Blocked). No Road improvement on any tile at turn 4. City center only. No worker. Roads not reached, so movement cost was not compared.
