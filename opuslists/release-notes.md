# OpusLists release notes

What changed in each version, newest first. All versions are Beta. Join the beta at [opusnex.us](https://opusnex.us).

## v0.2.0 Beta (2026-10-03)

Sync foundation. Nothing visible changes and the app still makes no network connections. This release prepares the data so that copies on different devices can be merged safely later.

### Added

1. Every list and item records when it last changed and which device changed it.
2. Deleted items and lists leave a small hidden record, purged after 90 days, so a delete on one device cannot be undone by another device later.
3. A merge function combines two copies. The most recent change to each item wins. A delete beats an older edit, and an edit made after a delete brings the item back.
4. Each device keeps a hybrid clock, so a device whose clock runs slow still wins after it has seen the other device's change.
5. Finishing the same repeating task on two devices produces one finished copy, not two.
6. Alert state and settings stay on the device they belong to. An item that arrives from elsewhere already past due does not fire an alert.
7. If a list is deleted on one device while another adds an item to it, the item moves to the first list.
8. A two-device simulator test (three devices, 200 random runs) checks that all copies end up identical, plus tests for the upgrade and for alert state.

### Changed

1. The data file is now version 2. The first launch upgrades it automatically and keeps `opuslists-data.v1-backup.json`, an untouched copy of the old file. Old items are stamped with the time the old file was last saved.
2. Backups exported from this version include the new fields. Backups from 0.1.x still import.
3. Finished copies of repeating tasks get predictable IDs.

### Known limits

1. Nothing syncs yet. There is no sync service, no pairing, and no web or mobile app.
2. Conflicts are settled per item. If two devices edit the same task offline, the later edit replaces the whole task, not just the field it touched.
3. Settings are per device and do not sync.

## v0.1.1 Beta (2026-10-02)

Brand pass to match the rest of the OpusNexus family.

1. New app icon: charcoal tile, white ring O, teal check.
2. New wordmark with a teal check, used in the app header and the quick add window.
3. The app is recolored to the family palette (teal accent, charcoal dark mode, cool gray light mode).
4. Roboto is now bundled with the app, so the look is the same on every machine.
5. New lists default to teal.
6. The wordmark is a typeset stand-in until the final artwork is ready.

## v0.1.0 Beta (2026-10-02)

First build.

### Added

1. Tabs: Today, Scheduled, Lists, All, and Done, with counts. The overdue count shows in red on Today.
2. Lists with name, color, and icon. Drag to reorder items inside a list. Each list has a Completed section with Clear completed.
3. Items with a checkbox, notes, steps, priority, due date, optional time, repeat (daily, weekdays, weekly, monthly, custom), and an optional early alert.
4. Completing a repeating item rolls it to the next date and leaves a finished copy in Done. Undo for complete, delete, and clear.
5. Native Windows toast alerts, an optional alert card with Complete and Snooze, or both.
6. Tray resident with Open, Quick Add, Pause Alerts, and Quit. Optional start with Windows.
7. A global quick add window (default Ctrl+Alt+L, changeable) with a live preview of what it understood.
8. Quick add syntax for dates, times, repeats, priority, and #list.
9. Share: copy as checklist, Markdown, and `.ics`.
10. Local storage, a rolling backup, and export and import.
11. Light and dark themes (match Windows or choose).
12. Keyboard: Ctrl+1 to 5 for tabs, Ctrl+N to focus the add bar, Ctrl+F to search, Ctrl+, for settings.

### Known limits

1. Toasts do not have buttons. Use the alert card for Complete and Snooze.
2. Alerts only fire while the app is running. Items missed while it was not running are summarized once on the next launch.
