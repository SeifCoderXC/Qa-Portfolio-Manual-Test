# BUG-003 — Two city-screen arrow buttons at once crash

**Severity:** Critical  
**Priority:** High  
**Environment:** Unciv 4.21.11 changelog  
**Related requirement:** REQ-05  
**Related test case:** TC-007 / CH-02  
**Source:** official 4.21.11 notes — “Fixed crash when activating 2 cityscreen arrow buttons at the same time”

**Steps to reproduce**
1. Found a city and open the city screen.
2. If two arrow / next-city controls are visible, activate both together (fast clicks or both sides).

**Expected result**  
One city is shown. No process death.

**Actual result (pre-fix)**  
Crash.

**Workaround:** Use one control at a time.  
**Evidence:** 4.21.11 release note  
**Notes:** Good interview example of a race on a UI control. Confirmation only — do not file it again on a post-4.21.11 build unless it still dies.
