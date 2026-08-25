My Journal — full multi-file web app
========================================

WHAT'S IN THIS ZIP
-------------------
index.html            — the app itself
manifest.json          — PWA manifest: name, icons, colors, install behavior
service-worker.js      — enables real offline support + proper "Install app" prompts
icon-192.png            — app icon (Android home screen) — new quill design
icon-512.png            — app icon (large / splash / maskable) — new quill design
apple-touch-icon.png   — app icon (iPhone home screen) — new quill design
favicon.png             — browser tab icon — new quill design

All 7 files must be uploaded together, at the TOP LEVEL of your GitHub repo
(not inside a subfolder, not as a zip).

WHY MULTI-FILE THIS TIME
-----------------------------
A single index.html can embed a manifest and icons just fine, but it
CANNOT have real offline support — browsers flatly refuse to register a
service worker from anything other than a genuine external file (this is
a hard security rule, not a workaround-able limitation). So this version
splits things back out into separate files specifically so
service-worker.js can actually do its job.

WHAT'S NEW IN THIS VERSION
------------------------------
- New quill icon (replaces the old book icon) on every icon file
- Loading screen shows the quill mark + a rotating journaling quote
- Cover photo on Today has real rounded corners now
- A working service worker — offline support and proper "Install app"
  behavior actually function this time, verified directly (not assumed)

HOW TO UPLOAD TO YOUR EXISTING REPO
--------------------------------------
1. Go to https://github.com/sakshibprasad/myjournal
2. Click "Add file" -> "Upload files"
3. Drag in all 7 files from this folder AT ONCE, so they land at the
   repo's root (GitHub will show a flat file list, not a folder)
4. Commit the changes — this will overwrite the old single-file version
5. Visit https://sakshibprasad.github.io/myjournal/
   (hard-refresh with Ctrl+Shift+R / Cmd+Shift+R, or fully close and
   reopen if it's installed as an app, since browsers cache aggressively)

IMPORTANT
-----------
- Entries, letters, and settings are stored only in your browser's local
  storage on that device. Use Settings -> "Export journal backup" to keep
  a copy you can restore later or move to another device.
- PIN lock, fingerprint/Face ID, letter notifications, and offline mode
  only work once the app is served over HTTPS (i.e. live on GitHub
  Pages) — not when opened as a local file.
