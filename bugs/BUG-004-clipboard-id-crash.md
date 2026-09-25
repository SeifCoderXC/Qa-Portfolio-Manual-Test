# BUG-004 — “ID from clipboard” crashes when clipboard is empty

**Severity:** Major  
**Priority:** Medium  
**Environment:** Unciv 4.22.1 changelog  
**Related requirement:** REQ-01 / multiplayer-adjacent control on menu  
**Related test case:** none in the core 24 — cover only if the button is visible  
**Source:** official 4.22.1 notes — “Fixed crash on 'ID from clipboard' when clipboard not set”

**Steps to reproduce**
1. Clear the OS clipboard (copy nothing, or copy empty).
2. On the Unciv screen that offers “ID from clipboard”, click it.

**Expected result**  
Button does nothing or shows a short message. Process stays up.

**Actual result (pre-4.22.1)**  
Crash.

**Workaround:** Paste a real ID first, or ignore the button.  
**Evidence:** 4.22.1 release note  
**Notes:** Negative test on an empty clipboard. Out of core smoke; useful if the control is on your build’s menu.
