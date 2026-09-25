Date: 2026-09-25
Build: Unciv 4.22.3 (desktop launcher ./Unciv)
Java: OpenJDK 21.0.7 (build 21.0.7+6-Ubuntu-0ubuntu124.04)
OS: Linux Lite (Ubuntu 24.04 family)
Tester: Seif El Islam Bouklab

Planned 24 / Run 24 / Pass 20 / Fail 0 / Blocked 4 / Not run 0
Pass rate of executed cases: 20/24

Defects opened: none

Evidence zip: evidance/run/unciv-evidence-2026-09-25.zip
Workbook: evidance/run/test-run.xlsx
Parent: https://github.com/SeifCoderXC/Qa-Portfolio-Manual-Test/issues/1

Passed: TC-001 TC-002 TC-003 TC-004 TC-005 TC-006 TC-007 TC-008 TC-009 TC-010 TC-011 TC-014 TC-015 TC-016 TC-017 TC-018 TC-019 TC-020 TC-021 TC-023

Blocked:
TC-012 no illegal neighbour for the warrior
TC-013 barbarian brutes spawned, none adjacent by turn 4, no attack
TC-022 N/A, New Game fields all have defaults
TC-024 no road tile to measure

Regression on this build:
BUG-002 civilopedia open/close confirmed, no stall
BUG-001, BUG-003, BUG-004 not run
BUG-005 blocked with TC-024

Risk: smoke, city production, research across a turn, save/load, options, resize, and empty save-name all passed on 4.22.3. Combat contact and owned-road cost were not reached.
