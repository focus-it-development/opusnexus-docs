# OpusType known issues

These are the current Beta limits. Most are on the plan.

1. Windows x64 only for now. A Mac version is planned.
2. Windows may keep a default app you chose earlier for a file type. Use Make OpusType your default on the start screen to change it in Windows Settings.
3. Images, tables, and colors in RTF files are removed when OpusType saves the file. Tables come through as tab separated text. For files with images or tables, OpusType offers to edit a copy instead. Fonts and sizes are kept.
4. Dragging files onto the window does not open them. Turning that on in Windows would stop dragging text within a document and dropping text in from other apps. Double-click a file, use Open with, or press Ctrl+O.
5. A document that uses a font not installed on your PC shows the font's name in italics and displays in Roboto until the font is installed. The file keeps the original font name.
6. A plain document switched to Code with the Plain Text language opens as Plain the next time, since both are `.txt` files.
7. Files that are not UTF-8 open correctly but save back as UTF-8. Older Notepad "Unicode" files save as UTF-8 with a byte order mark.
8. `.jsonc` files with comments cannot use Format, since comments are not valid JSON.
9. Tabs are not restored when OpusType starts. It opens on the start screen.
10. In rich text, Find and Replace matches stay inside one paragraph.
11. Beta installers are not code signed, so Windows shows a SmartScreen warning the first time. See [Getting started](getting-started.md).

Found something not listed here? Open an issue in this repository or email beta@opusnex.us.
