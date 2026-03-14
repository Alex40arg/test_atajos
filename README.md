# test_atajos
Motivation
Provide an interactive, single‑page web app to train common office keyboard shortcuts in Spanish with multiple modes (Learn, Practice, Campaign).
Support safe practice by excluding browser/system reserved shortcuts in Practice mode and giving contextual hints and feedback.
Track basic performance, mistakes and campaign progression to guide repetition and review.
Description
Adds a new index.html implementing a full UI and styles, including home, game and result screens and responsive layout.
Implements client state and logic in inline JavaScript with question generation via buildQuestionPool, mode handling (A, B, CAMPAIGN), HUD rendering, and phased campaign flow with phaseResults tracking.
Implements keyboard detection and normalization via normalizeComboFromEvent, blocks known browser shortcuts with shouldPreventBrowserShortcut, and handles user answers in handleAnswer (including beep feedback using AudioContext).
Adds practice helpers such as scheduled hints (scheduleHint), simple spaced repetition by requeueing wrong items in Mode A (maybeRequeueWrongA), mistake aggregation (collectTopMistakes), and UI controls (questionCount, helpToggle, soundToggle).
Testing
No automated tests were added or executed as part of this change.
