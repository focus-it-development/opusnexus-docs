# OpusEditor release notes

What changed in each version, newest first. All versions are Beta. Join the beta at [opusnex.us](https://opusnex.us).

## v0.1.1 Beta (2026-10-04)

1. HEIC and HEIF photos open now, including iPhone photos. They are read with libheif (WebAssembly), loaded only when you open one. A HEIC photo is kept as a lossless picture inside a project file.
2. HEIC and HEIF are added to Open and to the installer's file associations.
3. The interface files are now read directly instead of through a file URL, so they load the same from the installed app.
4. A third party notices file is added, with the libheif license notice.

## v0.1.0 Beta (2026-10-04)

First release. A quick photo editor with annotations that stay editable.

### Added

1. Adjustments with live preview: exposure, brightness, contrast, highlights, shadows, saturation, warmth, tint, sharpen, blur, Auto, and Compare.
2. Crop with fixed shapes and a thirds guide, rotate, flip, straighten, and resize.
3. Annotations: arrow, line, box, oval, text, marker, numbered steps, and pen. Move, resize, rotate, recolor, reorder, duplicate, lock, copy, and paste.
4. A Hide tool with blur, pixelate, and black box.
5. Project files (`.opusedit`) and Editable PNG exports keep annotations movable and editable.
6. Export PNG, JPG, and WebP with quality control. Copy to the clipboard. Paste a picture from the clipboard.
7. Open PNG, JPG, WebP, GIF, BMP, and project files, with file associations for these types.
8. Undo and redo (40 steps), zoom and pan, and light and dark themes that follow Windows.

### Good to know

1. Adjustments stay live inside a project file. An Editable PNG bakes adjustments into its picture, and only annotations stay live.
2. Crop, rotate, flip, straighten, resize, and Hide are applied to the picture itself.
3. Exports and re-encoded pictures drop camera and location metadata.
4. Pictures are limited to 16384 pixels on a side and 120 megapixels.
5. HEIC was not supported in this version. It arrived in v0.1.1.

### Planned

1. v0.2.0: batch export and export presets.
2. v0.3.0: layers and stickers.
