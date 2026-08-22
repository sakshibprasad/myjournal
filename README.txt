My Journal — single-file PWA (Daybook-style)
================================================

WHAT'S IN THIS ZIP
-------------------
index.html   — that's it. One file. Everything — the app, the icon, the
               PWA manifest — is built into this single file, the same
               way your other apps (Daybook, Tend, Ledger) work.

HOW TO UPLOAD TO YOUR EXISTING REPO
--------------------------------------
1. Go to https://github.com/sakshibprasad/myjournal
2. Click "Add file" -> "Upload files"
3. Drag in index.html so it sits at the TOP LEVEL of the repo
   (not inside any folder)
4. Commit the changes
5. Go to Settings -> Pages, confirm Source = "main" branch, "/ (root)"
6. Wait a minute, then visit:
   https://sakshibprasad.github.io/myjournal/
   (hard-refresh with Ctrl+Shift+R / Cmd+Shift+R if you still see an old page)

INSTALLING IT AS AN APP (once it's live on GitHub Pages)
-------------------------------------------------------------
Android (Chrome): open the URL -> tap the menu -> "Add to Home screen" / "Install app"
iPhone (Safari):   open the URL -> tap Share -> "Add to Home Screen"

It'll appear on your home screen with its own icon and open full-screen.

IMPORTANT
-----------
- Entries, letters, and settings are stored only in your browser's local
  storage on that device. Use Settings -> "Export journal backup" to keep
  a copy you can restore later or move to another device.
- PIN lock, fingerprint/Face ID, and letter notifications only work once
  the app is served over HTTPS (i.e. live on GitHub Pages) — not when
  just opened as a local file.
