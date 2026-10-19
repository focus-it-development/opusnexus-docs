# OpusFoundry release notes

What changed in each version, newest first. All versions are Beta. Join the beta at [opusnex.us](https://opusnex.us).

## v0.4.3 Beta (the real cause of the A)

1. Fixed the capital A losing its counter. Illustrator writes the counter as a relative move followed by more pairs, for example `m-5.49-16.22-11.75-37-12.13,37Z`. The extra pairs after a move are lines, but OpusFoundry read them as more moves, so the triangle collapsed to nothing and the A came out solid. Any letter drawn this way is fixed.
2. The update sheet exported from Illustrator is now a test file (`test/fixtures/update-sheet.svg`). It checks 65 shapes, the update layout, the A counter, and that every character fits.

## v0.4.2 Beta (the A, and tags at the edge)

1. Fixed a letter whose counter is drawn as its own shape, such as the triangle inside the capital A in the update sheet. It was filled in, so the A came out solid. A separate inner shape now always cuts a hole, whichever way it was drawn.
2. The character tags and boxes on the Find the letters step are no longer cut off at the top and left edges of the sheet. The first row of tags was hidden before. The sheet now has a margin around it.

## v0.4.1 Beta (sheets with columns)

1. Fixed a sheet that holds several columns side by side, such as the OpusNexusType update sheet with capitals, lowercase and punctuation on one page. The letters were read in rows straight across the columns, so the character tags landed on the wrong shapes. A wide empty gap that runs the full height of the sheet now starts a new column. Each column is read top to bottom, and the columns are read left to right.
2. New sheet type: Capitals, lowercase, then ! ? & ( ) . , ; : ' " * $ (65 shapes). It is picked automatically when a sheet has 65 shapes. Each column keeps its own baselines.
3. Ordinary single column sheets read exactly as before. 6 new logic checks use a three column test sheet (`test/fixtures/three-columns.svg`).

## v0.4.0 Beta (Mac build)

1. OpusFoundry now builds for macOS: a DMG and a ZIP for Apple Silicon (arm64) and for Intel (x64). The GitHub Actions workflow builds them on a Mac runner next to the Windows installer.
2. The Mac build is unsigned for now. It is not notarized, so macOS will block it the first time. See README for the one-time steps.
3. On Mac the app has a standard menu bar (OpusFoundry, Edit and Window), so Cmd+Q, Cmd+C and Cmd+V work. Cmd+S and Cmd+O already worked.
4. Double-clicking a `.opusfoundry` project, or dropping one on the Dock icon, opens it.
5. A tag push (`v*`) now also creates a draft pre-release holding the Windows installer and the Mac files, so builds are not limited by the Actions artifact storage quota.
6. Not tested on a Mac yet. The first Mac run is the first real test.

## v0.3.1 Beta (kerning preview)

1. The text preview in the Kerning step now scales to fit the window, so the whole line shows with no side scrolling.

## v0.3.0 Beta (kerning and the final check)

1. New Kerning step. OpusFoundry measures the gap between pairs like AV, To, Ty, P. and r. and compares it with your ordinary pairs. Each suggestion is a before and after picture with Apply or Skip, plus Apply all. Pairs that touch are always offered.
2. Kerning is written into the fonts. OTF and TTF both carry a GPOS kern feature, and a legacy kern table for older Windows software. Applied kerning is saved in the project and used in the type tester and the export preview. Checked by shaping the exported fonts with HarfBuzz and reading them back with fontTools.
3. New Final check step before export. Up and down: floating edges near the baseline and guide lines, ascenders that miss the cap height by a hair, round letters with the wrong overshoot, and descenders of different depth. Side to side: stem weights, off-centre symmetrical letters, and touching pairs.
4. Every Final check flag waits for you. Fix, or Accept current state. Where there is no automatic fix only Accept is offered, with a hint to fix it in the artwork. Nothing blocks export, and the Export step lists anything undecided.
5. The vertical fixes feed the spacing step, so spacing and kerning are measured on the corrected letters.
6. Tested on the OpusNexusType artwork: it finds the d stem that floats 14 to 18 units above the baseline, the ascenders a few units over the cap height, and the G and a edges.
7. 30 new logic checks (`test/kern.test.js`) and 19 new app checks.

## v0.2.1 Beta (wordmark and hammer)

1. New wordmark: "OpusFoundry" set in the OpusNexusType letters with the designer's tight spacing, followed by a single-color teal hammer standing on the baseline. The anvil is gone.
2. The hammer now strikes the "y". When you apply a fix, Apply all, or spacing, the hammer swings back and hits the y, which gives a little. Saving a font does the same with the bigger sound. It respects the system "reduce motion" setting.
3. New app icon: the family layout, a white O with the teal hammer as its accent mark. Installer, window and shortcut icons are updated.
4. The wordmark is drawn from OpusNexusType outlines, so nothing depends on an installed font. The d is corrected to sit on the baseline and meet the cap height.
5. Checks added: the header shows the wordmark with its hammer and y, and the hammer is moving during a strike.
6. The OpusNexusType written license is still pending. See THIRD_PARTY_NOTICES.md.

## v0.2.0 Beta (branding)

1. New wordmark: OpusFoundry with a small teal anvil after the last letter, about half the height of the "y". The anvil and the app icon are placeholders drawn here until the designer supplies the final art.
2. New app icon: the anvil on the dark tile.
3. Hammer strike: the anvil in the header takes a hammer strike whenever you apply something (a fix, Apply all, or spacing) and a bigger one when a font is saved. Skip, Undo and browsing stay quiet. It respects the system "reduce motion" setting.
4. Anvil sound: a short strike sound on the same actions. It is made in code, so there is no audio file to license. A Sound switch sits in the status bar and your choice is remembered.
5. Checks added: the sound is audible, is not clipped, and is short, and the animation and switch behave.

## v0.1.0 Beta (first release)

The first working version of OpusFoundry.

What is in it:

1. Opens SVG letter sheets (drag and drop or Open), as many as you like. Reads fills, groups, transforms, classes and all common shapes.
2. Finds letters and joins pieces such as the dots on i and j. Assigns characters in reading order from a sheet type (capitals, lowercase, numbers, punctuation, combinations, or your own list). Relabel or skip any shape.
3. Fit and align: scales to your cap height and x-height, finds row baselines from flat-bottomed letters, and checks every letter against the grid. Flat edges must sit on the line, round and pointed edges may overshoot by up to 3 percent. Each off-grid letter is shown as a red and teal overlay with Apply, Skip and Undo.
4. Fill the gaps: a grid of 83 common characters. Builds 11 punctuation marks from your own stems and dots, previewed one by one, marked "derived". Lists what still needs real drawings.
5. Spacing: optical side gaps from each letter's shape, compared live against even gaps, with a tighter or looser slider and word space width.
6. Clean outlines: finds overlaps, specks, doubled points and open paths, circles them on the letter, and heals with a before and after point count.
7. Type tester and an export checklist.
8. Exports OTF (CFF) and TTF (TrueType) with name, designer, copyright, license and embedding permission. Asks you to confirm you have the rights to the artwork.
9. Project files (.opusfoundry) keep sheets and every decision.

Checks run on every build: 52 engine checks and 22 font file checks on real artwork, plus a test that drives the real app through every step and verifies the exported fonts with fontTools. Spacing was compared with the finished OpusNexusType font: 50 of 52 letters match within 6 units (the two exceptions were replaced by hand in that font).

Known limits:

1. The app icon is a placeholder until the designer provides one.
2. No kerning yet.
3. SVG only. Save a copy as SVG from Illustrator, Inkscape or Affinity.
4. Windows installer is not code signed, so SmartScreen may warn on first run.

Planned for v0.2.0: kerning suggestions with before and after previews, reading .ai, EPS and PDF directly, tracing from pictures, accented letters, and a stem and weight consistency check.
