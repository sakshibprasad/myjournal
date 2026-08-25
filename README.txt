My Journal — single-file PWA
================================

WHAT'S IN THIS ZIP
-------------------
index.html   — the entire app. One file. The icon (quill design), the
               PWA manifest, and everything else is built directly into
               this file — nothing else to upload alongside it.

WHAT CHANGED IN THIS VERSION
--------------------------------
- New quill icon (matches the tan/coffee-brown reference you shared) —
  replaces the old book icon as the favicon, home-screen icon, and
  manifest icon.
- Loading screen now shows the quill mark plus a rotating journaling
  quote each time you open the app.
- Cover photo on Today now has real rounded corners (floating card look)
  instead of edge-to-edge.
- Fixed a real bug: a leftover reference to a "service-worker.js" file
  that no longer exists (left over from an earlier multi-file version)
  was silently failing every time the app loaded. It's been removed.
  Note: true offline support isn't possible in a single-file app — a
  service worker requires a real separate file, which conflicts with
  keeping everything in one index.html. If you want offline support,
  say so and we can go back to a multi-file structure for that.

HOW TO UPLOAD TO YOUR EXISTING REPO
--------------------------------------
1. Go to https://github.com/sakshibprasad/myjournal
2. Click "Add file" -> "Upload files"
3. Drag in index.html so it sits at the TOP LEVEL of the repo
   (overwrite the existing one)
4. Commit the changes
5. Visit https://sakshibprasad.github.io/myjournal/
   (hard-refresh with Ctrl+Shift+R / Cmd+Shift+R if you still see the
   old version — browsers cache aggressively)

IMPORTANT
-----------
- Entries, letters, and settings are stored only in your browser's local
  storage on that device. Use Settings -> "Export journal backup" to keep
  a copy you can restore later or move to another device.
- PIN lock, fingerprint/Face ID, and letter notifications only work once
  the app is served over HTTPS (i.e. live on GitHub Pages) — not when
  just opened as a local file.
