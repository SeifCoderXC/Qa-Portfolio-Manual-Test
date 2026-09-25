# Decisions

- 2026-09-24 — One product. Unciv desktop only. A second game would empty the week.
- 2026-09-24 — Software QA only. No electronics, no Postman-against-a-game, no Appium.
- 2026-09-24 — Requirements reverse-engineered from player-facing screens (New Game, first turns, save, options). Unciv does not publish a player spec.
- 2026-09-24 — 24 cases, not 80. Covers launch → first city → tech → unit → persist. Combat deep trees and multiplayer stay out.
- 2026-09-24 — Defects in `/bugs` are official changelog items rewritten as reports. They are regression targets, not “I clicked this today.” Source link on every file.
- 2026-09-24 — Java 21 is accepted. Unciv asks for 17; 21.0.7 on Ubuntu 24.04 is what the tester already has.
- 2026-09-24 — English UI only. Localisation is a later pack.
- 2026-09-24 — Mods out. They change the ruleset and poison repro.
- 2026-09-24 — CSV not TestRail. Junior ads want the fields, not the licence.
- 2026-09-24 — No invented Pass. Execution status stays READY / REGRESSION until the jar is run on the tester PC.
- 2026-09-25 — Execution closed on the tester PC. 24 run, 20 passed, 4 blocked, 0 failed. No bug filed. Case status in `tests/test-cases.csv` is from this run.
- 2026-09-25 — TestRail project 1, closed run 1, is the case-and-run record, together with Jira project UQ. The 2026-09-24 line "CSV not TestRail" is superseded.
- 2026-09-25 — Jira and TestRail both require a login. The recruiter copy is `jira/board.md`, `jira/issues.csv`, and `testrail/results.csv`.
