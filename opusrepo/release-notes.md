# OpusRepo release notes

What changed in each version, newest first. All versions are Beta. Join the beta at [opusnex.us](https://opusnex.us).

## v0.2.2 Beta (2026-10-04)

Edge Add-ons extension support.

### Changed

1. OpusRepo now accepts the browser extension from more than one source. The Microsoft Edge Add-ons build is allowed alongside the extension that ships with the app. Chrome Web Store support will be added with its ID once that listing is published.
2. The browser bridge registration lists every allowed extension ID. Turning Browser extension off and on again in Settings refreshes it.

### Security

1. Any other extension ID is still refused, for pairing and for every request.

No changes to the vault file, encryption, or data format.

## v0.2.1 Beta (2026-10-04)

Tray, quick generator, and tour.

### Fixed

1. The idle lock now counts only real use of OpusRepo (its window and quick search). Requests from the browser extension no longer restart the 5 minute timer, so the vault locks even while you keep browsing. The extension shows "locked" until you unlock in OpusRepo.

### New

1. A tray icon with Open OpusRepo, Generate password, Lock now, and Quit. Clicking the icon brings the window back.
2. Generate password from the tray: a strong password (20 characters), a simple one (16 letters and numbers), a passphrase (5 words), or Custom, which opens a small generator window. It works while the vault is locked. Copied passwords clear after your usual number of seconds. Nothing is saved.
3. Settings: Minimize to the tray (on by default) and Keep running in the tray when I close the window (off by default). The vault locks when the window is hidden if Lock when minimized is on.
4. A short tour with small screenshots opens after first-time setup. Reopen it from Settings, Show the tour.

### Changed

1. Logins that have a one-time code show an OTP badge in the list (it was 2FA). The One-time codes sidebar entry is gone. Codes are still kept inside each login, next to the username and password.

No changes to the vault file, encryption, or data format.

## v0.2.0 Beta (2026-10-04)

Browser extension for Chrome and Edge.

### New

1. A browser extension for Chrome and Edge. It fills logins and one-time codes from your OpusRepo vault. Nothing fills until you click the amber asterisk inside a sign-in field, then pick the login. There is no auto-fill.
2. Pairing. Turn on Browser extension in Settings, press Pair a browser, and type the 8 character code into the extension. The code works once and expires in 5 minutes. Unpair at any time.
3. Save new logins. After you sign in to a site that has no saved login, the extension offers to save it. Not now and Never for this site are available.
4. Password suggestions on sign-up and change-password fields.
5. Settings shows recent extension activity (fills, saves, pairing).

### Safety

1. The extension talks only to the OpusRepo app on this PC, through the browser's native messaging. No server, no internet.
2. Fills are refused on look-alike domains, on http sites (except localhost), inside frames, and while the vault is locked.
3. Matching uses the registrable domain from the Website field, so sub-domains of the same site match and look-alikes do not.
4. The extension only runs with OpusRepo open. If the app is closed, the extension says so.

### Install (beta)

1. The extension folder ships with the app and is also provided as a zip file. In Chrome or Edge open the extensions page, turn on Developer mode, choose Load unpacked, and pick the folder shown in OpusRepo Settings.
2. The extension has a fixed ID so the app can trust only it.

No changes to the vault file, encryption, or data format.

## v0.1.1 Beta (2026-10-04)

1. The OpusRepo wordmark now uses the same letterforms as the other Opus apps, instead of a different typeface. The a, b, c to asterisks flip is unchanged.
2. No changes to the vault, security, or data format.

## v0.1.0 Beta (2026-10-04)

First beta of OpusRepo, a local-first password manager for Windows. Not yet independently reviewed.

### Vault and security

1. One encrypted vault file. A master password (Argon2id, tuned for roughly a second) unlocks a random vault key. A separate recovery key opens the same vault key.
2. XChaCha20-Poly1305 encryption through libsodium. Every save is checked for tampering when opened.
3. Auto-lock after idle time, on minimize, on sleep, and on lock screen. Passwords stay masked until you click to reveal. Copied passwords clear after 30 seconds. The window is hidden from screen capture where Windows allows.
4. Atomic saves, with the last 10 versions kept in your app data folder.

### Setup and sync

1. First-run setup lets you keep the vault on this PC or in a folder you choose, with shortcuts for OneDrive, Google Drive, iCloud Drive, and Dropbox.
2. A clear notice that autosave is not real-time sync. A Sync now button, plus an automatic check on launch and when the vault file changes (can be turned off).
3. Item-level merge, so changes made on two PCs combine instead of one overwriting the other. Conflicted copies made by cloud services are merged and then moved to backups.
4. If the folder is unreachable, your changes are kept on this PC and saved when it comes back.

### Items

1. Login, Secure Note, Card, Identity, Server or Device, and Software License. Custom fields, folders, tags, favorites, search, and the last 10 passwords kept for each item.
2. A password and passphrase generator.
3. A renewal or expiry date on any item, with a one-click calendar reminder file and text you can paste into OpusLists.

### One-time codes

1. Built-in TOTP codes with a countdown and copy.
2. Set up by scanning your screen for a QR code (all monitors, no camera), pasting or dropping a picture, choosing an image file, or typing a setup key or `otpauth` link. Google Authenticator export links are supported.

### Sharing and recovery

1. Share an item as a locked page that opens in any browser, or as an OpusRepo share file. A 5 word passphrase is generated for you, or you can choose your own.
2. A printable recovery kit, with an optional split into 3 shares where any 2 recover the vault. Buttons open the Google Drive, iCloud Drive, and OneDrive websites so you can upload the kit yourself. OpusRepo never signs in to or stores anything in your cloud.

### Other

1. Import from Chrome, Edge, Bitwarden, 1Password, LastPass, and KeePass CSV files. An encrypted export, and a plain CSV export behind a warning.
2. A password health report. The optional breach check is off by default and only ever sends a 5 character hash prefix.
3. A quick search window on Ctrl+Alt+R.

### Not in this release

Browser extension, Mac build, file attachments, one-time share links, timed emergency access, Windows Hello unlock, and any sync server.
