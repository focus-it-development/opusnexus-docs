# OpusRepo

A local-first password manager for one person. Your logins, notes, cards, and licenses live in one encrypted vault file that you keep on your PC or in a cloud folder you choose.

Website: [opusrepo.app](https://opusrepo.app)

1. [Getting started](getting-started.md)
2. [Keyboard shortcuts](shortcuts.md)
3. [Release notes](release-notes.md)
4. [Known issues](known-issues.md)

OpusRepo is a Beta and has not been independently reviewed. Read [Known issues](known-issues.md) before trusting it with anything important.

## What it does

1. Keeps logins, secure notes, cards, identities, server logins, and software licenses in one encrypted vault file.
2. Locks with a master password (Argon2id) and can always be reopened with a printed recovery kit.
3. Generates one-time (TOTP) codes, and can set them up by reading a QR code off your screen. No camera is used.
4. Shares one item as a locked file that opens in any browser, or as an OpusRepo share file.
5. Works from a folder you choose, including OneDrive, Google Drive, iCloud Drive, and Dropbox folders, with item-level merging when two PCs have changed the same vault.
6. Fills logins and one-time codes in Chrome and Edge through a browser extension. Nothing fills until you click.
7. Sits in the system tray with a quick password generator.

There is no account, no server, and no telemetry. The app makes no network calls unless you turn on the optional breach check.

## Security in plain words

1. The vault is encrypted with XChaCha20-Poly1305, and the master password is stretched with Argon2id, tuned to take roughly a second.
2. OpusRepo protects against a stolen vault file or a breached cloud account.
3. It does not protect against malware that is already running as you.
4. If you forget your master password and lose your recovery kit, nobody can recover your data. Print the kit and keep it somewhere safe.

OpusRepo is part of the [OpusNexus](../README.md) family.
