THOUGHT RECORD — Make an APK using ONLY your phone
====================================================
No computer needed. Total time: ~10 minutes.
You'll: (1) put the app online via GitHub, (2) use PWABuilder to
get the APK, (3) install it.


WHAT YOU HAVE
-------------
A zip with a "pwa" folder inside containing:
  index.html, manifest.json, sw.js, and an icons folder.
Unzip it on your phone first (tap the zip → Extract). Keep all the
files together — do NOT separate them.


------------------------------------------------------------
PART 1 — Put the app online with GitHub (free, phone browser)
------------------------------------------------------------
1. In your phone browser go to github.com and make a free account
   (or log in).

2. Tap the + (top right) → "New repository".
   - Name it: thought-record
   - Set it to PUBLIC
   - Tick "Add a README"
   - Tap "Create repository".

3. In the new repo, tap "Add file" → "Upload files".
   - Tap "choose your files" and select EVERYTHING from the pwa
     folder: index.html, manifest.json, sw.js, and the 4 icon files.
   - IMPORTANT: the icons must end up in a folder named "icons".
     Easiest fix if uploading is fiddly on mobile: see PART 1B below.
   - Tap "Commit changes".

4. Turn on the website:
   - In the repo, tap "Settings" → "Pages" (left menu / dropdown).
   - Under "Branch" choose "main" and "/ (root)", tap Save.
   - Wait ~1 minute. The page shows a URL like:
       https://YOURNAME.github.io/thought-record/
   - Open that URL on your phone. The app should load.
     (If it 404s, wait another minute and refresh.)

PART 1B — if mobile upload won't keep the icons folder
   - Open manifest.json and sw.js and change every "icons/icon-..."
     path to just "icon-..." (remove the icons/ prefix), then upload
     all images into the repo root alongside index.html.
   - OR simpler: the app still WORKS without icons; PWABuilder will
     just use a default. You can upload index.html, manifest.json,
     sw.js only and proceed.


------------------------------------------------------------
PART 2 — Generate the APK with PWABuilder (phone browser)
------------------------------------------------------------
1. Go to  www.pwabuilder.com
2. Paste your GitHub Pages URL and tap Start.
3. It analyzes the app. The manifest + service worker should show
   green/valid. (Warnings are fine.)
4. Tap "Package for stores" → choose "Android".
5. In the options, the default "Signed test package" is fine for
   installing it yourself. Tap "Download".
6. You get a .zip. Open it on your phone and extract — inside is:
   - app-release-signed.apk   ← this is the one to install
   - (also an .aab — only needed for Google Play later)


------------------------------------------------------------
PART 3 — Install the APK on your phone
------------------------------------------------------------
1. Tap the .apk file.
2. Android will warn about "unknown apps". Tap "Settings" → allow
   your file manager / browser to install unknown apps → go back.
3. Tap Install.
4. The Thought Record icon appears in your app drawer. Open it —
   it runs fully offline.


------------------------------------------------------------
KEEPING YOUR ENTRIES SAFE
------------------------------------------------------------
Entries are stored inside the app on your device. They are NOT
backed up automatically and do NOT sync.

Use the built-in backup:
  - Open the app → "Saved" tab → tap "⬇ Backup".
    This saves a .json file to your Downloads.
  - To restore (new phone, reinstall): "Saved" tab → "⬆ Restore"
    → pick that .json file.

Do a backup now and then, especially before reinstalling or
switching phones.


------------------------------------------------------------
TROUBLESHOOTING
------------------------------------------------------------
- PWABuilder says "no manifest": your GitHub Pages URL is wrong or
  not live yet. Open the URL yourself first; it must show the app.
- Icons missing in PWABuilder: harmless, or follow PART 1B.
- APK won't install: make sure "install unknown apps" is allowed
  for the app you're tapping the .apk from.


A note: this is a tool for reflection, and it clearly matters to
you to have it close at hand. If what you're working through gets
heavy, it's worth using alongside support from a person you trust
or a professional — not on its own.
