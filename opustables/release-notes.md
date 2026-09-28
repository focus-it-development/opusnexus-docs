# OpusTables release notes

What changed in each version, newest first. All versions are Beta.

## v0.1.4 Beta (2026-09-28)

### Fixed

1. Toast messages and hover text could show with no visible text, because the Appearance colors set their text to the same color as their background. Both now keep their own text color in every theme and mode.

## v0.1.3 Beta (2026-09-28)

Appearance: light or dark, and a two-color theme.

### Added

1. An Appearance panel, opened from the palette button in the top bar or the Appearance link on the start screen.
2. Mode: System (follows Windows, the default), Light, or Dark. Changes apply right away and are remembered.
3. Five two-color themes, each an app bar color and a body color, with a tuned dark version of each: Slate (default), Harbor, Forest, Ember, and Plum. Each swatch shows both colors.
4. Custom: pick the app bar and body colors separately. It starts from the colors on screen, and Reset to Slate goes back to the default.
5. Text and icons on the app bar and body switch between dark and light ink to stay readable on any color, including custom ones. The start screen wordmark does the same.

### Changed

1. The app bar is now slate (#2A3038, the app icon tile color) by default, instead of matching the body.
2. Dark mode styles now follow the Appearance setting instead of reading Windows directly, so Light and Dark can be forced. Menus, scrollbars, and form controls follow along.

### Notes

1. The grid, menus, and dialogs always keep the plain light or dark colors, so the work area stays easy to read. Teal stays the accent in every theme. Exports are never affected.
2. The theme loads before the window draws, so there is no flash of the wrong colors at launch.

## v0.1.2 Beta (2026-09-27)

### Changed

1. The teal fx on the start screen types itself on a loop, the way the OpusType underscore blinks: f, then x, a hold, then backspace. One cycle is 4.4 seconds, four of the cursor's blinks. It replaces the one-time slide-in. With reduced motion turned on, the fx holds still.

## v0.1.1 Beta (2026-09-26)

### Changed

1. The fx tab shows only when there is something to use: on an empty cell with numbers above it or to the left, on a formula, or on a header over a column with numbers. Alt+= still works on any cell.
2. The start screen wordmark ends in the teal fx from the app icon instead of the blinking underscore. The fx slides in once each time the start screen opens, and holds still with reduced motion turned on.

### Fixed

1. Text on filled cells picks dark or light ink to match the fill, so it stays readable in dark mode. Before, a light fill from a file (like a pale header color) made white text disappear.

## v0.1.0 Beta (2026-09-26)

First release. A clean table editor for Windows that saves real Excel files.

### Added

1. Start screen with New table, Open file, and recent files. Nothing reopens on launch.
2. Autosave to `Documents\OpusTables` about 1.5 seconds after each change, with OneDrive detection, a Saved status, and safe saving (a temp file swapped into place).
3. A grid that draws only what is in view, so a 50,000-row CSV opens in about half a second and scrolls smoothly.
4. Typing, editing (F2 or double-click), Enter, Tab, and Tab-then-Enter back to the starting column, like Excel. Arrow keys, Ctrl+Arrow to the edge of the data, Page Up and Page Down, Shift to extend, Ctrl+A.
5. Insert, delete, resize, and drag to reorder rows and columns. Double-click a column edge to fit its contents.
6. Tabs: add, rename (double-click), reorder (drag), and delete, with Ctrl+Page Up and Ctrl+Page Down to switch.
7. Row 1 is the header by default, bold with a light fill, and stays in view while scrolling. Both can be turned off in the View menu. Files that open with a header-looking first row get it frozen, with a note and Undo.
8. Sort A to Z and Z to A, and filter by values with search, from the arrow in each header cell. A filtered or sorted column shows a teal dot. Total rows at the bottom stay put when sorting.
9. Formatting: bold, italic, underline, text color, fill color, alignment, borders (all, outside, bottom, thick bottom, none), and number formats (General, Number, Currency, Percent, Date, Text) with more or fewer decimal places. Selecting whole columns or rows formats them for cells typed later too.
10. Typed values are understood: `$1,200` becomes currency, `15%` a percent, `9/26/2026` a date. Leading zeros and long IDs stay exactly as typed.
11. Formulas with cell references and ranges, including other tabs (`=Budget!C4`, `=SUM('Q3 Sales'!B2:B9)`), `+ - * / ^`, `&`, comparisons, and `SUM`, `AVERAGE`, `COUNT`.
12. Automatic recalculation of only the formulas affected by a change, across tabs.
13. References follow the cells when rows or columns are inserted, deleted, or moved, and when tabs are renamed. Deleted cells become `#REF!`.
14. Clear errors: `#DIV/0!`, `#VALUE!`, `#REF!`, `#NAME?`, `#NUM!`, and `#CIRC!` with a message naming the cells in a circular reference. A formula with a typing mistake explains the problem and stays open for fixing. Missing closing parentheses are added.
15. Pointing: while typing a formula, click or drag cells (or use the arrow keys) to put their addresses in, including cells on other tabs. Referenced cells are outlined in color.
16. Quick formula: a rounded fx tab on the selected empty cell offers Sum, Average, and Count, with the range guessed from the numbers above or to the left and outlined before you choose. On a formula, the tab shows the formula. On a header cell, it adds a column total. Alt+= opens it.
17. New formulas take the number format of the first cell they use, so a total of prices shows as currency.
18. Status bar with Sum, Average, and Count of the selected cells.
19. Copy, cut, and paste of ranges. Pasted formulas shift their references. Paste from Excel, Google Sheets, and web pages keeps values, bold, italic, colors, fills, and number formats. Pasting a block into a larger selection repeats it to fill. Ctrl+D and Ctrl+R fill down and right.
20. Undo and redo for everything, one step per action.
21. Saves `.xlsx` with tabs, formatting, number formats, column widths, row heights, frozen header, header filters, and formulas with their calculated values, so Excel shows the right numbers right away.
22. Opens `.xlsx`, `.csv`, and `.tsv`. CSV files keep their delimiter, encoding, and line endings when saved, never run formulas from the file, and can be saved as a workbook with one click.
23. Opening an Excel file with charts, pivot tables, images, macros, merged cells, conditional formatting, comments, drop-down lists, links, Excel tables, or named ranges asks to edit a copy, so the original stays whole.
24. Formulas with functions OpusTables does not support yet keep the value Excel saved until something they use changes.
25. Export to PDF (US Letter, landscape for wide tables, scaled to fit, header repeated on each page) and to CSV.
26. Styled hover text on every icon button, with shortcuts.
27. A first-run tour of four cards, replayable from the start screen.
28. Light and dark themes that follow Windows.
