# BUG-005 — Owned roads charged as neutral roads

**Severity:** Minor  
**Priority:** Medium  
**Environment:** Unciv 4.22.0 changelog  
**Related requirement:** REQ-08  
**Related test case:** TC-024  
**Source:** official 4.22.0 notes — “fix: prevent owned roads from being charged as neutral roads”

**Steps to reproduce**
1. Own a tile with a road.
2. Move a unit along that road.
3. Compare movement cost with a road on a tile you do not own, if one exists.

**Expected result**  
Owned road uses the cheaper owned-road cost.

**Actual result (pre-fix)**  
Owned road could be charged as a neutral road.

**Workaround:** None needed for playability.  
**Evidence:** 4.22.0 release note  
**Notes:** Rules bug, not a crash. Still a valid confirmation case because movement math is player-visible.
