# OpusGrid release notes

What changed in each version, newest first. All versions are Beta. Join the beta at [opusnex.us](https://opusnex.us).

## v0.3.1 Beta (2026-09-30)

New: zoom slider in the status bar, from 10% to 200%, with minus and plus buttons and a percent readout. Click the percent to fit the page. Two finger zoom and Ctrl+wheel still work.

## v0.3.0 Beta (2026-09-30)

Hardware and cabling: racks, device faceplates with real ports, port-to-port cables, a cabling table, cable labels, and printing.

### Added

1. Racks at 12U, 24U, 42U, 45U, or a custom height, with numbered U slots. Put as many racks on a page as you need. Each rack has a name, a location note, a size on the page, and a Front/Rear toggle (press F). Rear is the default. A rack elevation is a schematic, so it does not follow the page scale.
2. Every device lives in a rack and snaps to its slots. Drag a device to move it within its rack or into another rack. Devices cannot overlap or leave the rack.
3. Devices with real faceplates, drawn at true rack proportions and in one generic OpusGrid style, not vendor artwork: switches at retail port counts (5, 8, 16, 24, 48, plus 2 SFP for 10, 18, 26, and 50, or 4 SFP/SFP+ for 28 and 52), with PoE marked; patch panels (12, 24, 48); firewall; 1U and 2U servers; storage controller; disk shelf; UPS; PDU; blank panel; cable manager; and a custom device. Every device stores a front face (bezel, drive bays, status lights) and a rear face (ports).
4. A custom device builder. Every device, including the built-in ones, has editable port groups (name, type, count, rows, side, PoE), so the built-ins are presets of the same builder. Devices also take a label and an asset tag.
5. Port types: RJ45, SFP/SFP+, QSFP, SAS, console, USB, power, and fiber LC. Ports have editable labels (shown as hover text) and four states: free, used, reserved, and disabled. A per-device summary shows how many ports are used, free, reserved, and disabled.
6. Cables: drag from one port to another on the rear view. The drop snaps to the nearest free port. Cable types are Cat6, Cat6a, fiber OM3, OM4, OS2, DAC, SAS, power, and Other, each with a default color you can override. A purpose tag (management, storage, uplink, data, power, or your own) can also set the color. Used ports show a ring in the cable's color. A cable type that does not fit a port shows a warning.
7. Cable routing: rounded by default, with right angle and straight as options, per cable or for the whole diagram. Cables in a rack run down the side; cables between racks go over the top. Parallel cables are spread onto their own lines. Cables follow their devices when they move, and pointing at either end of a cable lights up its whole path.
8. Cable length: an optional length on each cable, in feet or meters (a document setting, feet by default). Lengths are kept exactly, so switching units and back loses nothing. For a cable inside one rack, a suggested length appears (the U distance plus a slack allowance you set once, rounded up to a stock length) and is only used when you accept it. Rack to rack cables get no suggestion.
9. A cabling table you drop on the page. It is live and updates as cables change. Columns: cable ID, from rack and U, from device, from port, to rack and U, to device, to port, type, color, length, purpose, and notes. Hide any column, sort by any column, group by rack, cable type, or color, and filter to a subset, such as only the storage cables. Totals per cable type sit at the bottom, for ordering.
10. Cable schedule export to CSV (Export menu, or from a selected table, which keeps its filter and sort). The CSV splits rack and U into separate columns. Cells that would run as a formula in a spreadsheet are made safe.
11. A cable label sheet: two labels per cable (one at each end, each showing where the other end goes) or one label per cable listing both ends. It prints on plain paper with cut lines or on label stock, and can be exported alone as a PDF. It is added to the PDF export and to printing automatically, and you can turn that off in the Page panel.
12. Print (Ctrl+P, or the Print button) sends the page at its real paper size to the system print dialog.
13. Templates: Storage cabling (2 controllers, 3 shelves, SAS paths down and back up the shelves), Switch stack with uplinks, Patch panel map, and 42U rack.
14. Copy, paste, and Duplicate work on devices and racks. Undo and redo cover everything above, including making a cable.

### Changed

1. The library has a new Racks and hardware group.
2. The Page panel has a Cabling section (unit, slack, default copper type, default routing, label style) once a diagram has a rack.
3. Files from disk are checked when opened. Damaged or hand-edited hardware data is cleaned up instead of causing errors.

### Not in this version

1. A logical network map generated from the cabling. Network topology stays on its own templates.
2. Automatic rack to rack cable length.
3. Smart cable bundling and crossing avoidance (parallel cables are only spread apart).
4. Vendor-specific faceplate artwork.

## v0.2.3 Beta (2026-09-30)

### Fixed

1. The door, window, and flowchart icons in the symbol library are visible in dark mode.

## v0.2.2 Beta (2026-09-30)

Page sizes, drawing scale, and a scale block on the page.

### Added

1. Page sizes: Letter, Legal, and Ledger/Tabloid (still the default); ARCH C (18 × 24), ARCH D (24 × 36), and ARCH E (36 × 48); A4 and A3; and a Custom size typed in inches, up to 120. Portrait or landscape for all of them.
2. Drawing scale in the Page panel: 1/8", 3/16", 1/4" (the default), 3/8", 1/2", and 1" = 1'-0". Real sizes stay the same, so a 12' wall stays 12' and the floor plan redraws larger or smaller on the paper, staying centered where it was. Doors, windows, and floor plan symbols scale with it. Text, labels, and network symbols keep their size so they stay readable.
3. A scale block on the page, added automatically once a diagram has walls: the written scale, a scale bar that stays accurate when a print is shrunk to fit, and the diagram name. Drag it anywhere, click it to add today's date or hide the name, and Back to the corner puts it back. Turn it off with Show scale on the page, or select it and press Delete. It is in every export.
4. The status bar shows the current scale.

### Changed

1. The grid follows the scale: Snap every 1 ft means a real foot at any scale, and the dot grid shows one dot per foot (or every few feet when that would be too dense).
2. New walls get the right depth at any scale.
3. Very large sheets are exported at a slightly lower resolution so the image stays a size Windows can handle.
4. The office floor plan template title no longer spells out the scale, since the scale block shows it.

## v0.2.1 Beta (2026-09-29)

### Changed

1. A selected wall shows three handles: one at each end and one in the middle.
2. Drag the middle handle to move the whole wall in any direction. Walls joined to it stretch to stay connected.
3. Drag an end handle to break that end away from its corner and move only this wall. Drop it on another corner to join it there.
4. Dragging a corner with no wall selected still moves every wall on it.
5. Copy, paste, and Duplicate (Ctrl+C, Ctrl+V, Ctrl+D) work on whatever is selected. A wall pastes as a copy nearby with its doors and windows. A door or window pastes onto the same wall, beside the original.
6. The office floor plan note explains the wall handles.

## v0.2.0 Beta (2026-09-29)

Doors and windows that live in walls.

### Added

1. A Doors and windows group in the library: door, double door, sliding door, pocket door, window, and a plain opening. Pick one, then click a wall. A preview follows the pointer along the wall before you click.
2. Each one cuts a real opening in its wall, lined up with the wall and matched to its depth.
3. They move with their wall. Drag a corner, move a wall, or change a wall's length and they ride along. They stay inside the wall and never slide past a corner.
4. Drag a door or window to slide it along its wall, snapping to the grid. Drag it onto a different wall to move it there.
5. Click one to set its type, width (standard sizes or typed, like 34" or 2' 10"), and its distance from either end of the wall.
6. Doors: Flip hinge side, and Swing to other side. A new door opens toward the side of the wall you click on.
7. Splitting a wall with a T joint keeps each opening on the right piece of the wall. Deleting a wall removes its openings.
8. The office floor plan template now has real windows, an office door, and a double entry door.
9. What's new cards for people updating from v0.1.0.

### Changed

1. The old door and window symbols are no longer in the library. Diagrams made with them still open and show them.

## v0.1.0 Beta (2026-09-29)

First release. Diagrams, network maps, and floor plans on a smart grid.

### Canvas

1. A ledger page (17 × 11 in, landscape) on an endless canvas with a dot grid. Letter and Legal, portrait or landscape, are in the Page panel.
2. Everything snaps to the grid: moving, drawing, and resizing by dragging a handle. Turn snapping off in the status bar, or change the snap step (1 ft, 6 in, 3 in, 1 in).
3. Pan with the scroll wheel, Space and drag, or the middle mouse button. Zoom with Ctrl and the wheel. The zoom button fits the page.
4. Select, Shift or Ctrl click to add, drag a box to select several, move, resize, nudge with the arrow keys (Shift for a fine nudge), rotate 90°, duplicate, copy and paste, group and ungroup, bring to front and send to back, align and space evenly.
5. Undo and redo for everything.

### Shapes and connectors

1. Box, rounded box, ellipse, diamond, text, and flowchart shapes (start and end, process, decision, data).
2. Connectors attach to shapes and stay attached when shapes move. Drag from one shape to another with the connector tool, or from the dots that appear on a shape's edges.
3. Connectors run at right angles or straight, with an arrow, arrows at both ends, or none, dashed or solid, and can carry a label. They branch downward like a tree when a shape sits below another.
4. Fill, line, thickness, and text size and color for any selection.

### Walls that join

1. The Wall tool draws walls corner to corner. Type a length while drawing (12, 12' 6", 12 6, 12.5) and press Enter to place it exactly. Walls lock to 45° steps unless Shift is held. Enter or double-click finishes.
2. The Room tool drags out four joined walls at once.
3. Walls that meet share one corner. Drag a corner and every wall on it follows. A wall drawn into the middle of another joins it as a T.
4. Corners are drawn from every wall that meets there, so they join cleanly even when the walls have different depths.
5. Click a wall to set its length, depth, stud size (2 × 3, 2 × 4, 2 × 6, 2 × 8, or custom), spacing (12", 16", 19.2", 24" on center), and finish. The stud count shows under Framing. Right-click a wall to jump straight to its depth.
6. Changing a wall's length stretches the room: the far side moves with it, so a 12' by 13' room stays square.
7. Show wall lengths and Show studs are in the Page panel. New walls use the framing set there.
8. Scale is ¼ inch = 1 foot.

### Symbols

1. Network: router, switch, firewall, access point, server, NAS, cloud, internet, desktop PC, laptop, printer, IP phone, camera, UPS, patch panel, rack, user, and mobile.
2. Floor plan, drawn to scale: door, window, desk, chair, round table, network drop, outlet, and stairs.
3. Search symbols at the top of the library.

### Templates

1. Small office network, Network stack (OSI and TCP/IP), Office floor plan, Flowchart, and Blank.

### Files

1. Diagrams save as .opusgrid files in Documents\OpusGrid, a moment after each change.
2. Export a PNG (twice the page size), a PDF at the real paper size, or an SVG. Copy image puts the page on the clipboard.
3. The start screen has the Recent list tools shared with the other OpusNexus apps, Appearance, and a first-run tour.
