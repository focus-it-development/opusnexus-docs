# Getting started with OpusTables

## Install

1. Download the installer from your beta invitation and run it. It installs for your account only, so no admin rights are needed.
2. Beta builds are not code signed yet, so Windows may show "Windows protected your PC." Click **More info**, then **Run anyway**.

The first time OpusTables opens, a short tour shows the basics. **Take the tour** on the start screen replays it.

## Your first table

1. Click **New table** (or press Ctrl+N) and give it a name.
2. Type your headings in row 1. Row 1 is the header: bold, lightly filled, and it stays in view as you scroll.
3. Fill in the rows below. Press Enter to move down and Tab to move right.

## Where your tables live

OpusTables saves to `Documents\OpusTables` about 1.5 seconds after each change. The status in the top right shows Edited, Saving, or Saved. If OneDrive backs up your Documents folder, OpusTables saves there and shows a cloud icon.

New tables are real Excel workbooks (`.xlsx`). Excel, Numbers, and Google Sheets open them with the right numbers already showing.

## Typing values

OpusTables understands what you type.

| You type | You get |
| --- | --- |
| `$1,200` | Currency |
| `15%` | A percent |
| `9/26/2026` | A date |
| `TRUE` or `FALSE` | A true or false value |
| `'00123` | Text, kept exactly as typed |

Leading zeros and long ID numbers stay as they are.

## Formulas

Start with `=`. Examples:

1. `=A1+B1`
2. `=SUM(A1:A10)` or a whole column with `=SUM(B:B)`
3. `=Budget!C4` to use a cell on another tab
4. `=A1&" "&B1` to join text

Supported functions are `SUM`, `AVERAGE`, and `COUNT`, along with `+ - * / ^` and comparisons. Everything that depends on a cell updates the moment it changes, across tabs.

While typing a formula, click or drag cells to add their addresses, even on another tab. The cells a formula uses are outlined in color.

When you insert, delete, or move rows and columns, formulas follow the cells they point at. Renaming a tab updates formulas on other tabs.

## Quick formula

Select an empty cell under or beside some numbers and click the rounded **fx** tab (or press Alt+=). Pick Sum, Average, or Count. On a header cell, the fx tab adds a total below the column.

The status bar at the bottom always shows the Sum, Average, and Count of what is selected.

## Sort and filter

Click the arrow in any header cell to sort A to Z or Z to A, or to filter by value with search. A total row at the bottom stays put when you sort.

## Formatting

The toolbar has bold, italic, underline, text and fill color, alignment, borders, and number formats with more or fewer decimals. Format a whole column or row and cells typed there later pick it up too.

## Rows, columns, and tabs

1. Right-click a row or column header to insert or delete. Drag headers to reorder, drag edges to resize, and double-click a column edge to fit its contents.
2. Add a tab with **+**, double-click a tab to rename it, drag to reorder, and right-click to delete.

## CSV files

OpusTables opens `.csv` and `.tsv` files and saves them back with the same delimiter, encoding, and line endings. Formulas in a CSV are never run. **Save as workbook** turns a CSV into an `.xlsx`.

## Copy and paste

Paste from Excel or Google Sheets keeps values, bold, colors, fills, and number formats. Ranges copied within OpusTables keep their formulas, adjusted to where you paste.

## Export

The export button in the top bar saves a PDF (US Letter, landscape for wide tables, header on every page), a CSV of the current tab, or a copy as an Excel workbook.

## Excel files with features OpusTables cannot keep

If an Excel file has charts, pivot tables, images, macros, merged cells, or similar features, OpusTables offers to **Edit a copy** so the original stays whole.
