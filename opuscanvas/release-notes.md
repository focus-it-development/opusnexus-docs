# OpusCanvas release notes

What changed in each version, newest first. All versions are Beta.

## v0.1.3 Beta (2026-09-29)

1. The walkthrough now shows the first time OpusCanvas opens. Earlier builds skipped it because saved settings and existing screenshots looked like a returning user. It shows once for everyone on this update.
2. Take the tour on the start screen still replays it any time.

## v0.1.2 Beta (2026-09-28)

1. Captures now save to Pictures\Screenshots, the same folder Windows uses, so Recent also shows screenshots taken with Windows tools.
2. When Snipping Tool's own auto-save is on, OpusCanvas opens the file Windows saved instead of making a second copy.
3. Older captures in Pictures\OpusCanvas stay where they are and still open with Open image.

## v0.1.1 Beta (2026-09-28)

1. Start screen mark: the crosshair drags a selection box over the word Canvas, top left to bottom right, then the box fades and the crosshair settles below the last letter.
2. The crosshair has a small dot at its center.
3. Tauri crates pinned to match the npm packages, which fixes the Windows build.

## v0.1.0 Beta (2026-09-28)

First release. Screen capture and markup for Windows.

### Added

1. New capture opens the Windows snip overlay for a region, a window, or a whole screen, and opens the snip for markup.
2. Ctrl+Shift+S from anywhere, with OpusCanvas waiting in the system tray. The tray menu has New capture, Full screen, Open, and Quit, and closing the window asks once whether to keep running.
3. Full screen capture of the main monitor, and a 3 or 5 second delay for either capture.
4. Markup tools: arrow, box, ellipse, line, pen, highlighter, text, numbered steps, and blur, with seven colors and three thicknesses. Shift keeps lines at 45 degree angles and boxes square.
5. Editing: select, move, reshape arrow ends and box corners, edit text in place, delete, crop, undo, redo, and zoom.
6. Copy puts the marked-up image on the clipboard, ready to paste anywhere.
7. Captures save at once as PNG files in `Pictures\OpusCanvas`, with changes saved a moment after you make them, plus Save as. Opened JPEG files stay untouched, and the marked-up version saves as a new PNG.
8. Open or drop a PNG or JPEG, or press Ctrl+V on the start screen to mark up an image from the clipboard.
9. Recent captures with Remove from list, Show in folder, Delete file, and Clear list, shared with the other OpusNexus apps.
10. The Appearance panel, the first-run tour, and a start screen mark where the crosshair drags out a dashed box, then settles.
11. Placeholder icon (the O with a teal crosshair) and wordmark.
12. Tests: markup shapes (10), tour (5), and backend (8).
