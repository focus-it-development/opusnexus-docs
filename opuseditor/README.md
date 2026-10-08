# OpusEditor

A quick photo editor for Windows where your annotations stay editable. Adjust, crop, mark up, hide sensitive parts, and export, without an account or an internet connection.

Website: [opuseditor.app](https://opuseditor.app)

1. [Getting started](getting-started.md)
2. [Keyboard shortcuts](shortcuts.md)
3. [Release notes](release-notes.md)
4. [Known issues](known-issues.md)

## What it does

1. Adjusts a picture: exposure, brightness, contrast, highlights, shadows, saturation, warmth, tint, sharpen, and blur, with an Auto button and a Compare button.
2. Crops (free or fixed shapes), rotates, flips, straightens, and resizes.
3. Annotates with arrows, lines, boxes, ovals, text, a highlight marker, numbered steps, and a pen.
4. Hides sensitive parts with blur, pixelate, or a black box. Hidden pixels are removed from the picture, not just covered.
5. Exports PNG, JPG, or WebP, or copies the picture to the clipboard.
6. Opens PNG, JPG, WebP, GIF, BMP, AVIF, and HEIC (iPhone) photos.

## Annotations stay editable

Annotations are kept as objects, not painted onto the picture, until you export.

1. A project file (`.opusedit`) holds the original picture, your adjustments, and every annotation. Reopen it any time to move, resize, rotate, recolor, or retype anything.
2. An Editable PNG is an export option that stores the annotation data inside an ordinary PNG. Any viewer shows the flattened picture. Opened in OpusEditor, the annotations come back live.

Two things are applied to the picture on purpose. Crop, rotate, flip, straighten, and resize change the picture itself, and annotations move along with them. Hide changes the pixels, so a saved file cannot give the hidden part back.

## Privacy

OpusEditor makes no network calls and has no telemetry. Exports never carry camera, location, or other metadata. An Editable PNG does carry your annotation text, so turn that option off before sharing a picture whose notes are private.

OpusEditor is part of the [OpusNexus](../README.md) family.
