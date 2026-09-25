# BUG-002 — Civilopedia open can stall the UI

**Severity:** Major  
**Priority:** Medium  
**Environment:** Unciv 4.21.11 changelog  
**Related requirement:** REQ-14  
**Related test case:** TC-014  
**Source:** official 4.21.11 notes — “Avoid ANRs when opening civilopedia”

**Steps to reproduce**
1. From menu open Civilopedia.
2. Open an entry.
3. Watch whether input still works within a few seconds.

**Expected result**  
Entry opens. Back works. Map or menu accepts input after close.

**Actual result (pre-fix)**  
UI could stall (ANR) on open.

**Workaround:** Avoid Civilopedia on a suspect build; keep the session short.  
**Evidence:** 4.21.11 release note  
**Notes:** Checked on 4.22.3 in TC-014. One entry was opened and Civilopedia was closed. The UI stayed responsive.
