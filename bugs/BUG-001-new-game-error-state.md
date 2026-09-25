# BUG-001 — New Game can reuse a broken previous start

**Severity:** Major  
**Priority:** High  
**Environment:** Unciv 4.22.0 changelog (desktop)  
**Related requirement:** REQ-02  
**Related test case:** TC-003  
**Frequency:** unknown — treated as regression  
**Source:** official 4.22.0 notes — “New game screen: Start fresh if the latest game start is erroring”

**Steps to reproduce**
1. Reach New Game.
2. Start a game that errors during generation (or use a build/mod combination known to fail start).
3. Return to New Game without restarting the process.
4. Start again with safe tiny-map settings.

**Expected result**  
New Game does not keep the failed start. A clean tiny map starts.

**Actual result (as shipped before 4.22.0)**  
The screen could keep the erroring start instead of resetting.

**Workaround:** Quit the process and launch again.  
**Evidence:** release note 4.22.0  
**Notes:** On 4.22.3 this check was not reached. TC-003 started a tiny map without a generation error.
