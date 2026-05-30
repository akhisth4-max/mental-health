THOUGHT RECORD — Make it an Android app (.apk)
================================================

You have a folder with: index.html, manifest.json, sw.js, and icons/.
Goal: get it to a public URL, then PWABuilder turns it into an installable APK.

------------------------------------------------
STEP 1 — Put the app online (free, ~2 min)
------------------------------------------------
EASIEST: Netlify Drop
  1. On a computer, go to:  https://app.netlify.com/drop
  2. Drag the ENTIRE folder (the one containing index.html) onto the page.
     -> Drag the folder itself, not the files one by one.
  3. It gives you a live URL like  https://your-name-123.netlify.app
  4. Open that URL on your phone to confirm the app loads.

(Alternative: GitHub Pages, Vercel, Cloudflare Pages — any static host works.)

------------------------------------------------
STEP 2 — Generate the APK (free)
------------------------------------------------
  1. Go to:  https://www.pwabuilder.com
  2. Paste your Netlify URL and click Start / Analyze.
  3. It should detect the manifest + service worker (green checks).
  4. Click "Package for stores" -> choose ANDROID.
  5. For just installing it yourself, pick the "Test"/unsigned option
     (or generate a signing key — PWABuilder walks you through it).
  6. Download the .zip. Inside is your .apk (and an .aab for Play Store).

------------------------------------------------
STEP 3 — Install on your phone
------------------------------------------------
  1. Transfer the .apk to your Android phone (email it to yourself,
     Google Drive, or USB).
  2. Tap the .apk. Android will ask to allow "Install unknown apps"
     for your browser/file manager — allow it.
  3. Install. The Thought Record icon appears in your app drawer.

DONE. It works fully offline and saves entries on your device.

------------------------------------------------
NOTES
------------------------------------------------
- Entries are stored locally (localStorage). Reinstalling or clearing
  app data erases them. Use the Edit/View screen to keep what matters.
- To later publish on Google Play, use the .aab file from PWABuilder
  (requires a $25 Google Play developer account).
