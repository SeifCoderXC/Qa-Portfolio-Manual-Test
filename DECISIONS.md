# Scope choices

- One product: Unciv desktop 4.22.3. Multiplayer, mods, and Android are out of this run.
- Requirements were taken from the player-facing screens. Unciv does not publish a player specification.
- 24 cases cover launch, the first city, technology, one unit move, and save/load. Deep combat trees are out.
- The files in `bugs/` are official 4.21 and 4.22 release notes written as regression checks. A source link is on each file. They are not defects from this run.
- Java on the test machine is OpenJDK 21.0.7. Unciv documents Java 17 or newer.
- The UI language for the run was English.
- Mods were off. A mod changes the ruleset and makes a failure harder to repeat.
- Results were recorded in Jira project UQ and in TestRail run 1, and copied into this repository because those sites require an account.
- A case is Passed or Blocked only when the 2026-09-25 run produced that result. No result was filled in before the run.
