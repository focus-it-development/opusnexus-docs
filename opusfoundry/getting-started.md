# Getting started with OpusFoundry

## Install

1. **Windows:** download the installer from your beta invitation and run it. Beta builds are not code signed yet, so Windows may show "Windows protected your PC." Click **More info**, then **Run anyway**.
2. **Mac (Apple Silicon or Intel):** open the DMG and drag OpusFoundry to Applications. The Mac build is unsigned and not notarized, so the first time:
   1. Try to open it once. macOS says it cannot verify the app.
   2. Open System Settings, Privacy & Security, scroll down and click **Open Anyway**.
   3. If macOS says the app is damaged, run `xattr -cr /Applications/OpusFoundry.app` in Terminal and open it again.

## Get your artwork ready

1. Letters must be filled shapes, not lines with a stroke.
2. Lay them out in rows, left to right, in alphabet order. A sheet can also hold several columns side by side, such as capitals, lowercase and punctuation on one page.
3. Save a copy as SVG. In Illustrator that is File, Save a Copy. Inkscape and Affinity work too.
4. Keep all sheets at the same drawing scale.

## Make a font

1. Open your SVG sheets with **Ctrl+O** (Cmd+O on Mac), or drop them on the window.
2. Check the character tags on **Find the letters** and relabel anything that is wrong.
3. Work through the steps in order: Fit and align, Fill the gaps, Spacing, Kerning, Clean outlines and Final check. Each suggestion shows a before and after picture. Press **Apply** or **Skip**, or **Apply all**.
4. Try the font in the type tester.
5. On **Export**, fill in the font name, designer, copyright and license, confirm you have the rights to the artwork, and save the OTF and TTF files.

## Save your work

**Ctrl+S** (Cmd+S on Mac) saves a project file (`.opusfoundry`) with your artwork and every decision. Double-click a project to open it again.

## The hammer

The hammer after the name strikes the y when you apply a fix or save a font, with a short anvil sound. Turn the sound off with the **Sound** switch in the status bar. The animation stays still when your system asks to reduce motion.
