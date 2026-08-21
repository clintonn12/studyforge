StudyForge PWA v1.11.2
=========================

This package is built from your StudyForge Standalone v1.11 HTML. The flashcard/library data format is unchanged.

WHAT CHANGED
- Proper installable PWA: manifest, service worker, Android icons, standalone display mode.
- Offline app-shell reopening after the PWA has been loaded once.
- In Settings: Install StudyForge button / Android install guidance.
- Android swipe repair: native touch fallback, adaptive swipe threshold, fast-swipe recognition, and horizontal gesture locking.
- Mobile Jump back in panel uses normal content flow so its title, progress bar, and Continue button are not clipped.
- Study images are warmed when a deck/recent deck is opened, the first visible card is decoded before Study renders, and the upcoming rolling window is decoded in the background.
- Card changes wait for the next card's images only if they somehow missed the preload; normally this is already resolved and feels immediate.
- Removed whole-deck image decoding during study to avoid Android memory/CPU spikes. Decoded study image cache is bounded.
- Existing mouse-wheel suppression inside flashcards remains.
- Requests persistent browser storage when the browser supports it.

ANDROID INSTALL
A PWA cannot be installed directly from a file:// HTML file because service workers require a secure origin.
Serve this entire folder from HTTPS (or localhost on the Android device). Then in Chrome:
1. Open index.html through that HTTPS URL.
2. Open StudyForge Settings → Install StudyForge, or Chrome menu → Install app / Add to Home screen.
3. Launch StudyForge from the new Home Screen icon. It opens in standalone app mode.
4. After the first successful load, the app shell is cached for offline reopening. Flashcards continue to use StudyForge's local browser storage.

IMPORTANT LOCAL DATA NOTE
PWA data belongs to the origin/domain where you install it. Installing the same files at a different domain creates a separate browser storage area. Use StudyForge's complete JSON backup/restore when moving between origins/devices.

FILES
- index.html              StudyForge app
- manifest.webmanifest    Android/PWA install metadata
- sw.js                   offline cache/service worker
- icons/                  install icons
- README-FIRST.txt        this guide
- VALIDATION.txt          checks performed

RECOMMENDED DEPLOYMENT
Upload the whole folder, preserving names/paths, to any static HTTPS host you control. The app itself does not require a backend or cloud database; all flashcard data stays local in the browser.
