# RC-001 — Living Pages Core Regression Checklist

**Checklist ID:** RC-001  
**Application:** Living Pages  
**Test Type:** Regression / Functional / Persistence  
**Platform:** iOS / iPadOS  
**Test Environment:** Physical Device  
**Overall Status:** PASS

## Purpose

Verify that core Living Pages functionality continues to work after code changes, bug fixes, persistence updates, layout changes, and multi-page feature work.

This checklist is intended to catch regressions across the areas most affected by recent development.

## Launch & Navigation

- [x] Application launches successfully.
- [x] Current journal day loads correctly.
- [x] Previous-day navigation works.
- [x] Next-day navigation works when available.
- [x] Same-day Page 1 / Page 2 navigation works.
- [x] Correct page number is shown.
- [x] Relaunch returns to the expected saved page state.

## Text Editing

- [x] Text can be entered and edited.
- [x] Text remains aligned with the writing area.
- [x] Text remains visible when the keyboard appears.
- [x] Bottom writing area remains accessible.
- [x] Portrait keyboard behavior works.
- [x] Landscape keyboard behavior works.
- [x] Text persists after page navigation.
- [x] Text persists after force-close and relaunch.

## PencilKit Drawing

- [x] Drawing mode opens successfully.
- [x] PencilKit strokes appear while drawing.
- [x] Drawings remain visible after portrait → landscape rotation.
- [x] Drawings remain visible after landscape → portrait rotation.
- [x] Repeated rotation does not remove or shift drawings unexpectedly.
- [x] Drawings remain associated with the correct page.
- [x] Drawings persist after leaving and returning to the page.
- [x] Drawings persist after force-close and relaunch.
- [x] Hover and touch interaction do not corrupt drawing state.

## Autosave & Saved State

- [x] Editing triggers the saving state.
- [x] Saved indicator updates after persistence completes.
- [x] Text changes are saved.
- [x] Drawing changes are saved.
- [x] Page 1 saves independently.
- [x] Page 2 saves independently.
- [x] Saved content restores correctly after relaunch.

## Multi-Page Persistence

- [x] Page 1 retains its own text.
- [x] Page 2 retains its own text.
- [x] Page 1 retains its own drawings.
- [x] Page 2 retains its own drawings.
- [x] Page 1 retains its own attachments.
- [x] Page 2 retains its own attachments.
- [x] Content does not transfer between Page 1 and Page 2.
- [x] Page content remains correct after navigation.
- [x] Page content remains correct after force-close and relaunch.

## Attachments & Media

- [x] Photo attachment can be added.
- [x] Video attachment can be added.
- [x] Existing attachments remain visible.
- [x] Attachments remain associated with the correct page.
- [x] Attachments persist after page navigation.
- [x] Attachments persist after force-close and relaunch.

## Orientation & Layout

- [x] Portrait layout renders correctly.
- [x] Landscape layout renders correctly.
- [x] Page geometry remains stable through rotation.
- [x] Keyboard viewport remains usable in portrait.
- [x] Keyboard viewport remains usable in landscape.
- [x] Media and drawings remain positioned correctly after rotation.

## Day & State Persistence

- [x] Switching journal days loads the correct content.
- [x] Returning to a previous day restores its content.
- [x] Page-specific content does not appear on another day.
- [x] Force-close and relaunch preserve saved journal state.
- [x] Midnight/day transition does not remove persisted drawing state.

## Regression Result

**PASS**

Core Living Pages functionality remained stable across the tested navigation, text editing, PencilKit drawing, autosave, keyboard, multi-page persistence, attachment, rotation, relaunch, and day-state scenarios.