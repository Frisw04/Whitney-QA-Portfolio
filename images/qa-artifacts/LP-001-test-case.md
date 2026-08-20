# LP-001 — PencilKit Drawing Persistence & Rotation Stability

**Test Case ID:** LP-001  
**Application:** Living Pages  
**Feature:** PencilKit Drawing Persistence  
**Test Type:** Functional / Regression / Persistence  
**Priority:** High  
**Platform:** iOS / iPadOS  
**Test Environment:** Physical iPad  
**Final Status:** PASS

## Objective

Verify that PencilKit drawings remain visible, correctly positioned, and persisted when the device rotates between portrait and landscape and when the application undergoes common state changes.

## Preconditions

- Living Pages is installed and launches successfully.
- A journal page is available for testing.
- Drawing mode is available.
- PencilKit canvas is active.
- Test page can be viewed in both portrait and landscape orientations.

## Test Steps

1. Open a journal page in Living Pages.
2. Enter drawing mode.
3. Draw multiple marks in different areas of the page, including near page boundaries.
4. Observe the position and scale of the drawings in portrait orientation.
5. Rotate the device from portrait to landscape.
6. Verify the drawings remain visible and correctly positioned.
7. Rotate from landscape back to portrait.
8. Verify the drawings remain visible and correctly positioned.
9. Repeat the orientation changes multiple times.
10. Leave the journal page and return to it.
11. Force-close and relaunch the application.
12. Return to the test page and verify the drawing persists.
13. Verify hover and touch interaction do not unexpectedly move or remove the drawing.
14. Verify drawing persistence through later page/day state changes.

## Expected Result

Drawings should remain visible, correctly positioned, correctly scaled, and associated with the correct journal page throughout rotation and persistence events.

No drawing should disappear, shift unexpectedly, clip because of rotation, or restore in an incorrect position.

## Actual Result

After the final fix, drawings remained stable through portrait-to-landscape and landscape-to-portrait rotation. Repeated rotation, page leave/return, application relaunch, hover/touch interaction, and persistence testing passed.

## Regression Results

| Test Scenario | Result |
| --- | --- |
| Portrait → Landscape | PASS |
| Landscape → Portrait | PASS |
| Repeated Rotation | PASS |
| Leave / Return to Page | PASS |
| Relaunch / Force Quit | PASS |
| Hover / Touch Behavior | PASS |
| Day / Midnight Persistence | PASS |

## Evidence

See the regression summary image included with LP-001. It documents the defect investigation, geometry debugging approach, test strategy, and final regression results.

## Final Result

**PASS — RESOLVED**

The PencilKit drawing and page geometry implementation remained stable throughout the tested rotation and persistence scenarios.