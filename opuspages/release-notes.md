# OpusPages release notes

What changed in each version, newest first. All versions are Beta.

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
