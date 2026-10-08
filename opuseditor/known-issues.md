# OpusEditor known issues

These are the current Beta limits. Most are on the plan.

1. Windows x64 only for now. A Mac version is planned.
2. Not in this beta: batch export, export presets, layers, and stickers. Batch export and presets are planned for v0.2.0, and layers and stickers for v0.3.0.
3. There is no autosave. Save a project with Ctrl+S to keep your work editable.
4. Crop, rotate, flip, straighten, resize, and Hide are applied to the picture itself. Hide cannot be undone in a saved file.
5. An Editable PNG bakes your adjustments into its picture. Only the annotations stay live. A project file keeps adjustments live too.
6. Pictures are limited to 16384 pixels on a side and 120 megapixels.
7. HEIC support was tested with sample files. Real iPhone photos, including rotation and Display P3 color, still need more testing, so please report any HEIC picture that looks wrong.
8. The installer, file associations, and high DPI screens have had less testing on real Windows PCs than the rest of the app. Please report anything odd.
9. Beta installers are not code signed, so Windows shows a SmartScreen warning the first time. See [Getting started](getting-started.md).

Found something not listed here? Open an issue in this repository or email beta@opusnex.us.
