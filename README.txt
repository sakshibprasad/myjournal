My Journal — Web App / PWA (full file set)
==============================================

WHAT'S IN THIS ZIP
-------------------
index.html            — the app itself, with a loading splash screen on open
manifest.json          — PWA manifest: name, icons, colors, install behavior
service-worker.js      — enables offline support + real "Install app" prompts
icon-192.png            — app icon (Android home screen)
icon-512.png            — app icon (Android home screen, large / splash / maskable)
apple-touch-icon.png   — app icon (iPhone home screen)
favicon.png             — small icon shown in the browser tab

All 7 files must be uploaded together, at the TOP LEVEL of your GitHub repo
(not inside a subfolder, not as a zip).

WHAT'S NEW IN THIS VERSION
------------------------------
- Loading splash screen with the book logo on open (matches the app icon)
- Responsive layout: the app now scales up on wider screens instead of
  staying a narrow phone-width strip —
    - Phones: ~480px column (unchanged)
    - Unfolded Fold-style phones (~700px+): ~640px column
    - Tablets / Fold Ultra unfolded (~1000px+): ~760px column
- Fixed a real bug in the manifest that was silently breaking PWA install
  behavior (quotes inside the embedded manifest weren't URL-encoded, which
  cut the link short in the HTML). It's now a clean external manifest.json,
  so there's nothing to break.
- orientation set to "any" so it works properly in both portrait and
  landscape on tablets, instead of being locked to portrait.

HOW TO UPLOAD TO YOUR EXISTING REPO
--------------------------------------
1. Go to https://github.com/sakshibprasad/myjournal
2. Click "Add file" -> "Upload files"
3. Drag in all 7 files from this folder AT ONCE, so they land at the
   repo's root (GitHub will show a flat file list, not a folder)
4. Commit the changes
5. Go to Settings -> Pages, confirm Source = "main" branch, "/ (root)"
6. Wait a minute, then visit:
   https://sakshibprasad.github.io/myjournal/
   (hard-refresh with Ctrl+Shift+R / Cmd+Shift+R if you still see an old page)

INSTALLING AS AN APP (once it's live on GitHub Pages)
-----------------------------------------------------------
Android (Chrome), phone/Fold/Tab: open the URL -> tap the menu (⋮) ->
  "Add to Home screen" / "Install app"
iPhone/iPad (Safari): open the URL -> tap Share -> "Add to Home Screen"

It'll appear on the home screen with its own icon, its own loading screen,
and open full-screen like a native app — on phones, unfolded Folds, and
tablets alike.

ABOUT GETTING AN ACTUAL .APK FILE
-------------------------------------
Being fully honest here: I can't generate a signed .apk file directly —
that requires the Android build toolchain (Android Studio / Java / signing
keys), which isn't something I have access to. But your PWA is now built
to the exact standard those tools expect, so the process on your end is
short:

1. Get this app live on GitHub Pages first (steps above) — you need a
   real HTTPS URL for this to work.
2. Go to https://www.pwabuilder.com (free, made by Microsoft, no coding).
3. Paste in your GitHub Pages URL and let it scan the site.
4. It will detect the manifest, service worker, and icons automatically
   (all now properly set up) and offer an "Android" package download —
   this generates a real, installable .apk (or .aab for the Play Store)
   for you, signed and ready.
5. Download it, transfer to your phone (or any Android device — phone,
   Fold, Fold Ultra, Tab), and install it directly, no app store needed.

IMPORTANT
-----------
- Entries, letters, and settings are stored only in your browser's local
  storage on that device. Use Settings -> "Export journal backup" to keep
  a copy you can restore later or move to another device.
- PIN lock, fingerprint/Face ID, and letter notifications only work once
  the app is served over HTTPS (i.e. live on GitHub Pages) — not when
  just opened as a local file.
