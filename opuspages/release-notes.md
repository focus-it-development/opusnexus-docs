# OpusPages release notes

What changed in each version, newest first. All versions are Beta. Join the beta at [opusnex.us](https://opusnex.us).

## v0.1.3 Beta (2026-09-28)

### Added

1. The mark on the start screen animates: one sheet slides into place, then its top right corner folds over and stays. It plays each time the start screen opens, and shows the finished mark right away with reduced motion turned on.

## v0.1.2 Beta (2026-09-28)

One Save as, and a clearer Merge.

### Changed

1. The download button opens Save as directly (Ctrl+Shift+S too). It asks for a name, saves next to the original or in a folder you choose, and has a Pages choice: All pages (the default), Selected pages when thumbnails are selected, or Custom, such as 1-3, 5. Pages are saved in the order typed, and a range that does not fit the PDF gets a plain message before anything is saved.
2. The separate Save pages toolbar button is gone, since Save as covers it. Right-clicking thumbnails still offers Save these pages as a new PDF, which opens Save as with the selection chosen.
3. The Insert pages button is now Merge a PDF into this one, with a merge icon (two pages joining into one). Combine PDFs on the start screen uses the same icon.

## v0.1.1 Beta (2026-09-28)

Fixes from the first round of testing.

### Changed

1. Find fields gives each answer line its own text box, sitting right on the printed line, so typed text lines up with the form in every PDF reader. Before, stacked lines became one paragraph box, and readers spaced the text so it drifted off the lines. Stacked lines are numbered (Q7 Comments 1, 2, 3), only the first is marked required, and in OpusPages typing flows to the next line when one fills up. Enter or Down moves to the next line, Up and Backspace move back.
2. Save a copy asks for a name in a small box, saving next to the original, with Choose folder for anywhere else. It warns before replacing a file, and Ctrl+Shift+S opens it.
3. Save pages as a new PDF asks for a name the same way, instead of naming the file on its own.
4. The download button's hover text says Save a copy.

### Fixed

1. The Recent list on the start screen showed as plain bullets because its styles were missing. It now matches OpusType and OpusTables.
2. In dark mode, empty choice buttons on the page showed as black circles. Controls on the page now always use the light look, since pages stay white.

## v0.1.0 Beta (2026-09-28)

First release. A clean PDF app for Windows that reads, organizes, fills, signs, and marks up PDFs, and turns flat PDFs into fillable forms.

### Added

1. Start screen with Open PDF, Combine PDFs, and recent PDFs from anywhere on the PC. Nothing reopens on launch. PDFs can also be dropped on the window.
2. A page view built on pdf.js: continuous scrolling, pages drawn as they come into view, fit to width, zoom (Ctrl and the mouse wheel, Ctrl+= and Ctrl+-), and selectable text.
3. Find across every page (Ctrl+F), with matches highlighted and Enter to step through them.
4. Page thumbnails with drag to reorder, multi-select, and a right-click menu. Rotate, delete, insert pages from another PDF, and save pages as a new PDF.
5. Combine PDFs into a new file in `Documents\OpusPages`.
6. Form filling: text, paragraph, checkbox, radio, and dropdown fields, saved as standard PDF form values.
7. Prepare form, with Find fields (auto-detect) and manual placing of Text, Paragraph, Checkbox, Dropdown, and Date fields. Auto-detect turns answer lines into text boxes, rows of boxes into pick-one groups named by their row and column labels, and ovals into radio buttons, names each field after its numbered question, and marks it required when the question has an asterisk. Tested on a Google Forms printout, which it turns into 14 working fields with no cleanup.
8. Signatures: draw once, kept on this PC, placed with a click, then moved and resized.
9. Markup: highlight and underline on selected text, pen, text boxes, and sticky notes that open in any PDF reader. All movable and deletable while the file is open.
10. Undo and redo for page changes, form fields, and markup.
11. Autosave in place about 1.5 seconds after each change, with safe saving (a temp file swapped into place), plus Save a copy.
12. Password protected PDFs open read only when they can be displayed.
13. The Appearance panel from OpusType and OpusTables: System, Light, or Dark, and two-color themes.
14. A first-run tour of four cards: autosave, pages, fill and sign, and Prepare form.
15. Placeholder app icon (the O with a teal folded page) and wordmark, until the designer's files arrive.
