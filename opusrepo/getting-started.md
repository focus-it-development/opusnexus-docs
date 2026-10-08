# Getting started with OpusRepo

## Install

1. Download the installer from your beta invitation and run it. It installs for your account only, so no admin rights are needed.
2. Beta builds are not code signed yet, so Windows may show "Windows protected your PC." Click **More info**, then **Run anyway**.

## Set up your vault

1. Choose where the vault lives: on this PC, or in a folder you pick. Shortcuts are there for OneDrive, Google Drive, iCloud Drive, and Dropbox.
2. Choose a master password. Pick something long that you can remember, because it cannot be reset.
3. Print the recovery kit and keep it somewhere safe. It reopens the vault if you forget the master password. You can split the kit into 3 shares where any 2 recover the vault. Buttons open the Google Drive, iCloud Drive, and OneDrive websites so you can upload a copy yourself. OpusRepo never signs in to or stores anything in your cloud.
4. A short tour opens after setup. Reopen it any time from Settings, Show the tour.

Autosave in a cloud folder is not real-time sync. Use **Sync now**, or let OpusRepo check on launch and when the vault file changes.

## Add items

1. Pick a type: Login, Secure Note, Card, Identity, Server or Device, or Software License.
2. Add custom fields, folders, tags, and favorites. OpusRepo keeps the last 10 passwords for each item.
3. Use the password and passphrase generator for new logins.
4. Set a renewal or expiry date on any item. You can save a calendar reminder or copy text to paste into OpusLists.

## Import

Bring logins in from Chrome, Edge, Bitwarden, 1Password, LastPass, or KeePass CSV files. Delete the CSV afterward, because it holds your passwords in plain text.

## One-time codes

1. Open a login and add a one-time code.
2. Set it up by scanning your screen for a QR code (all monitors, no camera), pasting or dropping a picture, choosing an image file, or typing a setup key or `otpauth` link. Google Authenticator export links work too.
3. The code appears with a countdown and a copy button. Logins that have one show an OTP badge in the list.

## Browser extension

The extension fills logins and one-time codes from your vault in Chrome and Edge. It talks only to OpusRepo on this PC, with no server and no internet.

1. In OpusRepo, open Settings, turn on **Browser extension**, and press **Pair a browser**.
2. Install the extension from the [Chrome Web Store](https://chromewebstore.google.com/detail/dplbbieibohcedpahcnochmkceldpplb) or [Microsoft Edge Add-ons](https://microsoftedge.microsoft.com/addons/detail/pomjgagokpppokbljdohlldncjkkocdd). Settings has Get it for Chrome and Get it for Edge buttons that open the same listings. Edge needs OpusRepo v0.2.2 or later, and Chrome needs v0.2.3 or later. If you turned the extension on before updating, switch Browser extension off and on once in Settings. You can still load the copy that ships with the app unpacked from the folder shown in Settings.
3. Click the OpusRepo icon in the toolbar and type the 8 character pairing code. The code works once and expires in 5 minutes.
4. On a sign-in page, click the amber asterisk in a field and choose a login.

Fills are refused on look-alike domains, on http sites (except localhost), inside frames, and while the vault is locked. The extension only works while OpusRepo is open.

## Tray and quick generator

OpusRepo adds a tray icon. Its menu has Open OpusRepo, Generate password, Lock now, and Quit. Generate password offers a strong password (20 characters), a simple one (16 letters and numbers), a passphrase (5 words), or Custom, and works while the vault is locked. Copied passwords clear after your usual number of seconds. Two settings control the window: Minimize to the tray, and Keep running in the tray when I close the window.

## Sharing

Share one item as a locked page that opens in any browser, or as an OpusRepo share file. A passphrase of 5 words is generated for you, or you can choose your own. Send the passphrase by a different route than the file.

## Locking

OpusRepo locks after 5 minutes of non-use of the app itself, when minimized, on sleep, and on the lock screen. Activity from the browser extension does not restart the timer. Passwords stay masked until you click to reveal, and copied passwords clear after 30 seconds.
