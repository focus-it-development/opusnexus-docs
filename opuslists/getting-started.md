# Getting started with OpusLists

## Install

1. Download the installer from your beta invitation and run it. It installs for your account only, so no admin rights are needed.
2. Beta builds are not code signed yet, so Windows may show "Windows protected your PC." Click **More info**, then **Run anyway**.

Use the installed app rather than running from source. Windows only shows toast alerts reliably for an installed app.

## Add items

1. Type in the add bar at the top and press Enter. Press **Ctrl+N** to jump to it.
2. Open an item to add notes, steps, a priority, a due date, an optional time, a repeat, and an early alert.
3. A checklist item with no date and a dated task are the same thing. Add a due date to any item whenever you want an alert.

## Quick add

The add bar and the quick add window both understand plain phrases. Turn this off in Settings if you would rather type plain titles.

| Type this | You get |
| --- | --- |
| tomorrow, today, tonight | That date. "tonight" defaults to 8:00 PM |
| monday, fri, next week | The next such day. "next week" means next Monday |
| in 20 minutes, in 2 hours, in 3 days, in 1 week | A relative due date and time |
| 3pm, 3:30pm, at 15:30, at 5, noon | A due time. Without a date, today (or tomorrow if the time has passed) |
| 10/15, 10/15/2026, 2026-10-15 | A specific date |
| every day, daily, every weekday, every week, every month, every 2 weeks | A repeat |
| !, !!, !!! | Low, medium, high priority |
| #groceries | Puts the item in that list (partial names work, like #groc) |

Example: `call the dentist tomorrow at 9am #inbox !`

Press **Ctrl+Alt+L** from any app to open the quick add window. It shows what it understood as you type. You can change the shortcut in Settings.

## Alerts

1. OpusLists checks for due items every 15 seconds while it is running. It runs in the tray, so closing the window does not stop alerts.
2. Items without a time alert at the all-day alert time in Settings, which is 9:00 AM by default.
3. If something came due more than 5 minutes ago while the app was not running (PC off, asleep, or the app quit), you get one summary notification instead of a pile of old alerts. Those items show as overdue.
4. Alert style is a setting: Windows toast, alert card, or both. The alert card is a small window with Complete, Snooze, Open, and Dismiss buttons. Clicking a toast opens the app to that item.

## Repeating tasks

Completing a repeating item rolls it to the next date and leaves a finished copy in Done. Undo covers complete, delete, and clear.

## Share

Use Share to copy a list as a checklist, export Markdown, or export a calendar file. The plain checklist is the most dependable way to move a list into Apple Reminders.

## The tray

Right-click the tray icon for Open, Quick Add, Pause Alerts, and Quit. Start with Windows is optional.

## Where your data lives

`%APPDATA%\OpusLists\opuslists-data.json`

A rolling backup is made on each launch. Settings has Show data file, Export backup, and Import backup.
