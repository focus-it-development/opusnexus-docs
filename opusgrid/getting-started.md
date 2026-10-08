# Getting started with OpusGrid

## Install

1. Download the installer from your beta invitation and run it. It installs for your account only, so no admin rights are needed.
2. Beta builds are not code signed yet, so Windows may show "Windows protected your PC." Click **More info**, then **Run anyway**.

The first time OpusGrid opens, a short tour shows the basics. **Take the tour** on the start screen replays it.

## Start a diagram

Click **New diagram** for a blank page, or **From a template** for an office network, the network stack, an office floor plan, or a flowchart. Diagrams save in `Documents\OpusGrid` as you work.

## Shapes, symbols, and connectors

1. Pick a shape from the toolbar and drag on the page, or click a symbol on the left and click the page.
2. Everything snaps to the grid. Drag a handle to resize; Shift keeps the proportions.
3. Drag from one shape to another with the Connector tool (C), or from the dots that appear on a shape's edges. Connectors stay attached when shapes move.
4. Double-click a shape or connector to type a label.

## Walls and rooms

1. **Wall (W):** click corner to corner. Type a length while drawing, like 12 or 12' 6", and press Enter to place it exactly. Enter again or double-click finishes.
2. **Room (M):** drag out four joined walls at once.
3. Walls that meet share a corner. Drag a corner and every wall on it follows.
4. Click a wall to set its length, depth, studs, spacing, and finish. Changing the length stretches the room so it stays square. Right-click a wall to jump to its depth.
5. A selected wall shows three handles. The middle one moves the wall. An end handle breaks that end away from its corner.

## Doors and windows

Pick one under **Doors and windows**, then click a wall. It cuts a real opening and moves with the wall. Drag it along the wall or onto another wall. Click it to set its width, its distance from either corner, the hinge side, and which way it swings.

## Racks and cabling

1. Open **Racks and hardware** in the library and click the page to place a rack at 12U, 24U, 42U, 45U, or a custom height. Give it a name and a location note. Press **F** to flip between Front and Rear. Rear is the default, and it is the view where you make cables.
2. Add devices from the same group: switches at retail port counts, patch panels, a firewall, servers, a storage controller, a disk shelf, a UPS, a PDU, a blank panel, a cable manager, or a custom device. Devices snap to the rack's U slots and cannot overlap.
3. Click a device to edit its port groups, labels, and asset tag. Each port is free, used, reserved, or disabled, and a summary shows the counts.
4. Drag from one port to another to make a cable. The drop snaps to the nearest free port. Choose the cable type, color, routing, length, and purpose in the side panel. A cable type that does not fit a port shows a warning.
5. Drop a **cabling table** on the page. It updates as cables change, and you can sort it, group it, filter it, and hide columns. Export it as CSV for ordering.
6. A cable label sheet is added to Print (Ctrl+P) and to the PDF export automatically, with two labels per cable or one label listing both ends. It prints on plain paper with cut lines or on label stock, and it can be exported alone as a PDF. Change the label style, or turn the sheet off, in the Cabling section of the Page panel.
7. Start from a template: Storage cabling, Switch stack with uplinks, Patch panel map, or 42U rack.

## Page and scale

Click an empty spot on the page to see the Page panel: sheet size (Letter to ARCH E, or a custom size), orientation, drawing scale (1/8" to 1" = 1'-0"), grid, and wall options. Plans with walls get a scale block with a scale bar in the corner. Drag it anywhere, or turn it off.

## Share it

**Export** makes a PNG, a PDF at the real paper size, or an SVG. **Copy image** (Ctrl+Shift+C) puts the page on the clipboard.
