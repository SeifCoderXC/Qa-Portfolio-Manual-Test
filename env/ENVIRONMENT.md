# Environment

Practice pack. Fill the game version after first launch on the tester PC.

| Field | Value |
|---|---|
| OS (tester PC) | Ubuntu 24.04 family (Java string already captured) |
| Java | OpenJDK 21.0.7 (`OpenJDK Runtime Environment (build 21.0.7+6-Ubuntu-0ubuntu124.04)`) |
| Unciv version | 4.22.3 (confirmed on-screen, main menu footer) |
| Install source | itch.io desktop zip |
| Launch | `./Unciv` (native launcher; `java -jar Unciv.jar` hit `HeadlessException` when run from Claude's sandboxed shell — no real X11 access there, unrelated to the game) |
| Display | 1366x768, LVDS-1 |
| Language | English |
| Mods | none |
| Save folder | next to the jar (`SaveFiles/`, `GameSettings.json`) |
| Evidence | `evidance/screenshots/`, `evidance/saves/` |
| Analysis date | 2026-09-24 |
| GUI execution date | 2026-09-25 |
| Tester | Seif El Islam Bouklab |

Oracle for “version”: the string in the UI, not `java -version`. Java 21 ≠ Unciv 4.21.
