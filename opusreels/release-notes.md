# OpusReels release notes

What changed in each version, newest first. All versions are Beta. Join the beta at [opusnex.us](https://opusnex.us).

## v0.1.2 Beta

1. The Windows installer is published to a draft pre-release on every push to main, named after the version in package.json, the same way OpusFoundry does it. No tag push is needed, and nothing goes to Actions artifact storage.

## v0.1.1 Beta

1. The Layout tab note about the facecam now says how the box was set (found automatically, from a saved profile, or drawn by you).
2. The Windows build publishes the installer to a draft pre-release when you push a v* tag, instead of an Actions artifact, which avoids the artifact storage quota. Branch pushes build and test only.

## v0.1.0 Beta (first version)

OpusReels is the tenth app in the OpusNexus family: turn a long video into short vertical clips, locally.

1. Open MP4, MOV or MKV files, including variable frame rate recordings. Files that will not play in the preview get a small temporary preview copy. Exports always use the original.
2. Local transcription with word timing, with a progress bar and a time estimate. English only for now.
3. Ranked clip suggestions from a speech and pause finder plus a loud moment finder for gameplay. Each clip lists its reasons in plain words. No virality score. Trim by hand, add your own clips, or remove any.
4. Vertical layout editor with a live 9:16 preview. Five layouts: center crop, whole frame on blur, cam on top, cam on bottom, cam in a corner. Automatic facecam detection with draggable, resizable boxes for the cam and the gameplay window. Streamer profiles saved as fractions of the frame so they fit other resolutions.
5. Captions with the spoken word highlighted. Three styles, any installed font, text and highlight colors, size, words per line, position, and a button that places them away from the cam. Lines never run wider than the safe area.
6. Exact cuts and 1080 by 1920 export in one pass on NVENC, Quick Sync or AMF, with automatic fallback to the next encoder and finally to software. Output is constant frame rate so variable frame rate sources stay in sync. The length of every export is verified. SRT and VTT export.
7. Projects (`.opusreels`) save clip choices, layout, captions and transcript. The source video is never copied or changed. Double clicking a project opens it in the app.
8. Free edition branding: a small watermark at the top left (it moves to the top right when a face would sit under it) and a 2 second end card over the last moments of real footage. Both are drawn during the single export pass and no clean copy is written to disk. Pro removal comes in v0.2.0.
9. Family look: same window layout, theme and icon style as the other Opus apps.

Tested here: 24 layout, 13 caption, 11 clip finder and 10 project checks, a real ffmpeg export of a constant and a variable frame rate source (1080 by 1920, length verified, captions, watermark, end card, cancel), loading of the two native modules, and a full run of the real app (open, analyze on a gameplay video with a facecam, edit, export, save, reopen) with no page errors.

Not tested here: the hardware encoders (no graphics card in the test machine) and Windows itself. The Windows build workflow runs the same tests on Windows before it builds the installer.

Not in this version: AI helpers (bring your own key or a local model, free for everyone), the Pro license, lossless smart cut, cut list export for other editors, motion following crop, translation, a Mac build.
