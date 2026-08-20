# TC-002 — Multi-Page Content Persistence After Relaunch

**Test Case ID:** TC-002  
**Application:** Living Pages  
**Feature:** Multi-Page Persistence  
**Test Type:** Functional / Persistence / Regression  
**Priority:** High  
**Platform:** iOS / iPadOS  
**Test Environment:** Physical Device  
**Final Status:** PASS

## Objective

Verify that content saved to an individual Living Pages journal page remains associated with the correct page after navigation, force-close, and application relaunch.

The test verifies page-scoped persistence for text, PencilKit drawings, and media attachments.

## Preconditions

- Living Pages is installed and launches successfully.
- A journal day containing multiple pages is available.
- Page 1 and Page 2 can be navigated independently.
- Autosave is functioning.
- Page 2 is available for test content.

## Test Data

Add distinguishable content to Page 2 so restored content can be visually identified:

- Text
- PencilKit drawing
- Photo attachment
- Video attachment

## Test Steps

1. Launch Living Pages on the physical test device.
2. Open a journal day containing multiple pages.
3. Navigate to Page 2.
4. Enter identifiable text on Page 2.
5. Add a PencilKit drawing.
6. Add a photo attachment.
7. Add a video attachment.
8. Verify all test content is displayed on Page 2.
9. Wait for the application to display the Saved state.
10. Navigate away from Page 2.
11. Return to Page 2.
12. Verify the correct Page 2 content is restored.
13. Force-close Living Pages.
14. Relaunch the application.
15. Return to the same journal day and Page 2.
16. Verify the text is restored.
17. Verify the PencilKit drawing is restored.
18. Verify the photo attachment is restored.
19. Verify the video attachment is restored.
20. Verify Page 2 content has not appeared on Page 1.

## Expected Result

Page 2 should retain its own text, drawing, photo, and video after navigation and application relaunch.

All content should restore to the correct page without disappearing, duplicating, or transferring to another page.

Page 1 and Page 2 should maintain independent persisted state.

## Actual Result

Page 2 restored its saved text, PencilKit drawing, photo, and video after navigation and application relaunch.

The test content remained associated with Page 2 and did not transfer to Page 1.

## Verification Results

| Verification | Result |
| --- | --- |
| Page 2 text restored | PASS |
| PencilKit drawing restored | PASS |
| Photo attachment restored | PASS |
| Video attachment restored | PASS |
| Page navigation preserved content | PASS |
| Force-close / relaunch preserved content | PASS |
| Page 1 remained independent | PASS |
| Page 2 remained independent | PASS |

## Evidence

Physical-device testing captured Page 2 operating with text, PencilKit drawing, photo and video attachments, page navigation, keyboard interaction, and the Saved state active together.

## Final Result

**PASS**

Multi-page content remained page-scoped and persisted correctly through navigation, force-close, and application relaunch.