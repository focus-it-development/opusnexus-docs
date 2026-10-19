# OpusFoundry

Turn letter artwork into a working font. OpusFoundry reads SVG artwork of your letters, lines them up on a proper type grid, fills the gaps, spaces and kerns the letters, and exports an installable OTF and TTF. Every fix is shown as a before and after picture first, and nothing changes your font until you press Apply.

Website: [opusfoundry.app](https://opusfoundry.app)

1. [Getting started](getting-started.md)
2. [Keyboard shortcuts](shortcuts.md)
3. [Release notes](release-notes.md)
4. [Known issues](known-issues.md)

## What it does

1. **Add artwork.** Open one or more SVG sheets, or drop them on the window. A sheet can hold rows of letters, or several columns side by side.
2. **Find the letters.** Each letter is boxed and tagged with the character it will become. Dots on i and j join their letter. Relabel or skip any box.
3. **Fit and align.** Letters are scaled to your cap height and x-height and set on their baselines. Letters slightly off the line are shown in red and teal, before and after.
4. **Fill the gaps.** Shows which of 83 common characters exist, and builds 11 punctuation marks from your own stems and dots, marked "derived".
5. **Spacing.** Optical side gaps for every letter, compared against even gaps, with a tighter or looser slider.
6. **Kerning.** Finds pairs such as AV, To and Ty that look too loose or touch, with Apply, Skip or Apply all. Kerning is written into both font files.
7. **Clean outlines.** Finds overlaps, specks, doubled points and open paths, and heals them with a before and after point count.
8. **Final check.** Flags floating edges, ascenders that miss the cap height, uneven overshoot and descenders, stems of the wrong weight, off-centre letters and touching pairs. Each flag waits for you: Fix, or Accept current state.
9. **Try it out**, then **Export** OTF and TTF with name, designer, copyright, license text and embedding permission.

Project files (`.opusfoundry`) keep your artwork and every Apply and Skip decision.

## Privacy

OpusFoundry has no account, no server and no telemetry, and makes no network calls. Your artwork and fonts stay on your computer. Only use artwork you made or have permission to turn into a font.

OpusFoundry is part of the [OpusNexus](../README.md) family.
