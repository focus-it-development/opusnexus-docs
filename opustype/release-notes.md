# OpusType release notes

What changed in each version, newest first. All versions are Beta.

## v0.4.6 Beta (2026-09-28)

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

1. The document page, menus, and dialogs always keep the plain light or dark colors, so the work area stays easy to read. Teal stays the accent in every theme. Exports are never affected.
2. The theme loads before the window draws, so there is no flash of the wrong colors at launch.

## v0.4.5 Beta (2026-09-26)

A short welcome, and a safety net for RTF files.

### Added

1. A first-run tour of four cards: autosave to Documents\OpusType, the Rich, Plain, and Code switch, clean paste, and the clean launch. Each card has a small drawing of the real control, and the teal cursor from the logo blinks after each title and slides along the progress marks. It ends on New document, with Close as a quieter way out.
2. What's new cards after an update, showing only what changed since the version last opened (at most four cards). People updating from 0.4.0 or earlier see Code mode, line endings and encoding, and the RTF safety check.
3. Take the tour, next to the version number on the start screen, replays the tour any time.
4. When an RTF file has images or tables, OpusType asks before opening it, since saving would remove them. Edit a copy (the default) opens a copy in the OpusType folder and leaves the original alone. Open anyway edits the file as before.

### Notes

1. The tour and What's new are shown at most once each. OpusType records that they were seen before showing them, so closing the app mid-tour does not bring the tour back.
2. Arrow keys move between cards and Esc closes. With reduced motion turned on in Windows, the cursor holds still and the progress mark jumps instead of sliding.
3. The tour is skipped for anyone who already has documents or saved settings from an earlier version, since they get What's new instead.

## v0.4.0 Beta (2026-09-26)

Code mode.

### Added

1. Code, a third document type next to Rich and Plain, picked with the new three-part switch in the top bar. Files open in Code from their extension.
2. Syntax colors for PowerShell, Batch, Bash, Python, JSON, YAML, XML, INI, CSV, HTML, CSS, JavaScript, SQL, and Markdown, with separate light and dark palettes built from the brand colors. Every color is at least 4.5:1 against its background. Batch and INI use highlighters written for OpusType, since no ready-made ones exist.
3. A language box in the top bar. Changing the language changes the colors and renames the file to match (`notes.txt` becomes `notes.py`), keeping extensions like `.config` that already fit.
4. Switching a plain document to Code detects the language from the text (shebang lines, JSON, XML, HTML, Batch, PowerShell, Python, SQL, INI, YAML, Markdown). When nothing is clear, the language list opens.
5. Line numbers on by default in Code, matching bracket highlight, auto-indent, and Tab and Shift+Tab to indent or outdent selected lines.
6. View menu settings for Code: Auto-close brackets (off by default) and Indent with Tabs, 2 spaces, or 4 spaces, detected from the file when it opens. Line numbers and word wrap are remembered separately for Plain and Code.
7. Format for JSON files (button or Shift+Alt+F). Broken JSON gets a message with the line number, and the cursor jumps there.
8. Code exports: PDF with colors and line numbers, HTML page with colors that follows the reader's light or dark setting, and Copy as colored code for pasting into email, Teams, or Word.
9. Save a copy as another type, for Plain and Code.
10. Roboto Mono, bundled with the app, as the default Code font at 11 pt. The Display font and Text size in the View menu are separate for Plain and Code.
11. The New document dialog has a Code option with a language list. The Open dialog and the recent list include code files, and recent code files show their language.

### Changed

1. Plain and code files keep their own line endings and UTF-8 byte order mark when saved. Before, plain text was always saved with Windows line endings and any BOM was dropped, which could break Bash scripts and PowerShell scripts with special characters.
2. New files get line endings and encoding suited to their type: LF for Bash, Python, and web files, CRLF for Batch, PowerShell, and Windows config files, a BOM for PowerShell, and never a BOM for Batch. Changing a file's language applies its defaults and shows what changed. Both can be switched in the View menu.
3. The Rich and Plain toggle is now a three-part Rich, Plain, Code switch. It also works with the Left and Right arrow keys.
4. Leaving Rich for Code shows the same confirmation as leaving Rich for Plain.
5. File extensions sent to the file system are checked (letters and digits only, up to 10 characters).

### Fixed

1. Typing right after picking a font or size could lose the first few characters.

## v0.3.0 Beta (2026-09-26)

Fonts and sizes.

### Added

1. Font and Size boxes in the rich text toolbar. The font list comes from the fonts installed on the PC, including fonts installed just for the current user. Names show in their own typeface, the last five fonts used sit at the top, and typing filters the list. Sizes from 1 to 400 pt can be picked or typed, and "Default" clears a size.
2. RTF files save and open fonts and sizes. Files from Word and WordPad now keep their fonts and sizes instead of switching to Roboto.
3. A font missing from the current PC shows in italics in the Font box, with its name kept in the file.
4. Word exports carry fonts and sizes, and include Roboto inside the file so they look right on PCs without it. Only the Roboto styles a document uses are included.
5. Display font and Text size for plain text, in the View menu. They change how plain text looks on screen without changing the file.
6. A "Get Roboto free" link to Google Fonts in the Export menu and after the first Word export. Links open in the default browser.

### Changed

1. Default text is 12 pt everywhere: on screen, in RTF files, and in Word and PDF exports. Before, the screen showed 12 pt while files and exports used 11 pt. Headings are 22, 17, and 14 pt. Documents saved by earlier versions open looking the same as before.
2. The toolbar wraps onto a second line in narrow windows instead of overflowing.
3. GitHub Actions updated to versions that run on Node.js 24 (checkout v6, setup-node v6, upload-artifact v6), which clears the Node.js 20 deprecation warning.

## v0.2.1 Beta (2026-09-26)

App icon update.

### Changed

1. App icon tile lifted from near-black to slate (#2A3038) with a faint light edge, so the icon keeps its shape on dark taskbars and in dark Start menus.
2. The cursor in the app icon uses a brighter teal (#1A9BB5) so it stays visible at taskbar sizes. The wordmark and the rest of the brand keep #087388.
3. Full Windows icon set, installer icon, and `brand/mark` files regenerated. The tile and cursor colors are set in one place in `tools/make_brand.py`.

## v0.2.0 Beta (2026-09-26)

Layout, plain text tools, and export.

### Added

1. Export menu with Word (.docx) and PDF, available in both rich and plain text.
2. Word export built into the app (no Office needed), with Word heading styles, bold, italic, underline, strikethrough, tabs, line breaks, alignment, and bulleted and numbered lists. Each numbered list restarts at its own number.
3. One-click PDF export through the WebView2 PDF engine: US Letter, 1 inch margins, no header or footer, black on white in any theme, Roboto embedded. Falls back to the Windows print dialog if direct export fails.
4. View menu in plain text with Line numbers (off by default) and Word wrap (on by default). Both are remembered.
5. Plain text editor rebuilt for correct line numbers with wrapping and much better performance on large files. It keeps the same look, with no code coloring or autocomplete.

### Changed

1. Rich text shows a US Letter width page (8.5 in) with 1 inch margins, one continuous sheet.
2. Plain text fills the whole window edge to edge, like Notepad. Clicking anywhere below the text moves the cursor to the end.
3. The formatting toolbar shows a thin divider once the document scrolls.

### Fixed

1. A scrollbar appeared on short or empty documents.

## v0.1.1 Beta (2026-09-26)

Branding update.

### Added

1. Official OpusType wordmark on the start screen, with light and dark versions that switch with Windows. The teal underscore is drawn separately and blinks as the cursor, and holds still when reduced motion is turned on.
2. New app icon: the O mark with the underscore cursor in white on a rounded near-black tile. The 16, 24, and 32 pixel sizes use a thicker underscore so it stays visible in the taskbar.
3. `brand/` folder with the source logo files, light and dark wordmarks, the full icon set, color specs, and a README.
4. `tools/make_brand.py` to regenerate the wordmark variants and icons from the source files.

### Changed

1. Accent color is now the brand teal (#087388) for buttons, the text caret, active toolbar buttons, the Rich/Plain switch, and focus outlines. Dark mode uses a lighter teal (#5CC0D3) so controls stay readable.
2. Wordmark underscore set to #087388 to match the other brand files.

### Removed

1. Placeholder app icon and text wordmark.

## v0.1.0 Beta (2026-09-25)

First build.

### Added

1. Desktop app for Windows x64 with an NSIS installer that installs per user, no admin rights needed.
2. Rich text editor, using Roboto as the base font, bundled for offline use.
3. Formatting toolbar: bold, italic, underline, strikethrough, headings 1 to 3, bulleted and numbered lists, left, center, and right alignment.
4. New document dialog with a prefilled name (Untitled plus today's date) and a choice of rich or plain text.
5. Autosave to `Documents\OpusType`, about 1.5 seconds after typing stops, with an Edited, Saving, Saved status.
6. OneDrive detection through the Windows Documents known folder, with a cloud icon when the folder syncs.
7. Plain text paste in rich documents: formatting is removed, line breaks, tabs, and spaces are kept. Dropped text behaves the same way.
8. Rich and Plain toggle per document. Rich saves as `.rtf`, plain saves as `.txt`, and the file is renamed to match. Switching to plain asks for confirmation, with a Don't ask again option.
9. RTF reader and writer covering paragraphs, headings, bold, italic, underline, strikethrough, alignment, nested bulleted and numbered lists, line breaks, tabs, and full Unicode. Reads RTF from Word and WordPad, including both list formats they use.
10. Start screen with New document, Open file, and a recent documents list. Nothing reopens on launch.
11. Rename from the title bar (click the name or press F2).
12. Open `.rtf`, `.txt`, and other text files from anywhere on the PC.
13. Safe saving through a temp file swap, with retries when OneDrive has a file locked.
14. Reads UTF-8, UTF-8 with BOM, UTF-16 (older Notepad Unicode files), and legacy ANSI text.
15. Light and dark themes that follow Windows.

### Known limitations

1. Placeholder app icon (replaced in v0.1.1).
2. Not yet offered as a default app for `.txt` or `.rtf`.
3. RTF content OpusType does not edit (images, tables, colors, fonts) is dropped on save.
4. Dragging files onto the window does not open them.
