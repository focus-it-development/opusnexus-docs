# OpusLists known issues

These are the current Beta limits. Most are on the plan.

1. Windows only for now. A Mac version is planned.
2. Nothing syncs yet. There is no sync service, no pairing, and no web or mobile app. v0.2.0 prepared the data so copies on different devices can be merged safely later.
3. When sync arrives, conflicts will be settled per item. If two devices edit the same task offline, the later edit replaces the whole task, not just the field it touched.
4. Settings are per device and do not sync.
5. Toasts do not have buttons. Use the alert card for Complete and Snooze.
6. Alerts only fire while the app is running. Items missed while it was not running are summarized once on the next launch.
7. Windows behavior such as toast display, the tray icon, and start with Windows has had more testing in an automated harness than on real Windows PCs. Please report anything that does not behave.
8. Beta installers are not code signed, so Windows shows a SmartScreen warning the first time. See [Getting started](getting-started.md).

Found something not listed here? Open an issue in this repository or email beta@opusnex.us.
