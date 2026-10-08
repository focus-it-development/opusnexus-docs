# OpusRepo known issues

These are the current Beta limits. Most are on the plan.

1. OpusRepo has not been independently reviewed. Keep another copy of anything critical until it has been.
2. Windows x64 only for now. A Mac version is planned.
3. If you forget your master password and lose your recovery kit, nobody can recover your data.
4. OpusRepo protects a stolen vault file or a breached cloud account. It does not protect against malware already running as you.
5. The Chrome Web Store extension needs OpusRepo v0.2.3 or later to pair, and the Microsoft Edge Add-ons extension needs v0.2.2 or later. After updating, switch Browser extension off and on once in Settings so the browser bridge picks up the new ID.
6. Not in this beta: file attachments, one-time share links, timed emergency access, Windows Hello unlock, and any sync server.
7. Cloud folder sync is autosave into a folder, not real-time sync. Use Sync now if two PCs share a vault.
8. The Windows installer and Windows-only behavior (lock on minimize, hiding from screen capture, the cloud folder shortcuts) had limited testing on real Windows PCs before release. Please report anything that does not behave.
9. The Add another button on an item's one-time code adds an extra code. Remove the old one with the cross.
10. Beta installers are not code signed, so Windows shows a SmartScreen warning the first time. See [Getting started](getting-started.md).

Found something not listed here? Open an issue in this repository or email beta@opusnex.us.
