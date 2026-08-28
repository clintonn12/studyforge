StudyForge PWA v1.11.5 — Mobile Terms + Progress Controls
=========================================================

This update is built directly on StudyForge PWA v1.11.4. It keeps the same StudyForge local library version and the same browser-storage keys. Updating these app files at the SAME GitHub Pages URL does NOT intentionally reset, replace, or delete your local flashcards.

WHAT CHANGED
- Rebuilt the Android/mobile "Terms in this set" card layout so Term content, Definition content, LaTeX, and attached images remain visible instead of being squeezed or clipped.
- On phones, each term row is now a clean full-width stack with a compact action strip, a Term block, and a Definition block.
- Small saved image widths are given a practical minimum preview size in the Terms list on mobile, without changing the saved image itself.
- Selection mode now includes Select all cards.
- Every Topic panel gets Select topic / Deselect topic while selection mode is active.
- Study-mode Topic labels are compact content-sized pills instead of stretching across the card.
- Removed the duplicate Install StudyForge button from the sidebar. Installation/checking remains in Settings.
- Replaced the sidebar storage paragraph with a cleaner relative status such as "Saved just now" or "Saved 2 min ago".
- Added Set settings for each flashcard set:
  * Mark set completely studied — marks every card Known so the set reads 100%.
  * Reset progress — uses the existing reset workflow, including the existing star-preservation choice.
- The sticky Terms action strip now keeps Add card, Batch create, Topic settings, Set settings, Study, Hide Terms, Select, Rearrange, and Sort available while scrolling.
- Removed the redundant Add another card action from the very bottom of Terms in this set.
- Removed the large Flashcards mode tile from the upper deck page. Flashcard studying remains available from the preview and sticky Terms actions.
- Existing Topics, topic ordering/colors, study-by-topic filters, bulk tags/topics, move/copy, image-aware rearranging, PWA/offline support, and mobile swipe support remain.

LOCAL DATA SAFETY
- Library data version remains 12.
- Main localStorage key remains studyforge.v4.
- Existing IndexedDB/local-storage persistence remains in place.
- makeCard and makeDeck data constructors are unchanged from v1.11.4.
- Existing card/deck IDs, Terms, Definitions, LaTeX, images, image settings, tags, Topics, progress, stars, deactivation state, card order, folders, and unknown legacy fields are preserved by the existing migration logic.
- The service worker only refreshes cached application-shell files. It does NOT call localStorage.clear(), IndexedDB deleteDatabase(), or erase your StudyForge library.

SAFE GITHUB UPDATE
1. In the currently working StudyForge app, make a Complete JSON Backup first. This is strongly recommended even though this update is designed to preserve local data.
2. Keep the SAME repository and SAME GitHub Pages URL, for example:
   https://clintonn12.github.io/studyforge/
3. Extract this ZIP.
4. Upload the CONTENTS directly to the repository ROOT, replacing matching files such as index.html, sw.js, manifest.webmanifest, and icons.
5. Commit to main. GitHub Pages should redeploy automatically.
6. After the Pages deployment is green, open the website in Chrome and reload once so the v1.11.5 service worker/app shell becomes active.
7. Reopen the installed Android PWA.
8. Do NOT clear Chrome site data/storage. Do NOT move the app to a different GitHub Pages origin if you want the same locally stored cards.

GITHUB ROOT SHOULD LOOK LIKE
studyforge/
  index.html
  manifest.webmanifest
  sw.js
  .nojekyll
  icons/
    icon-192.png
    icon-512.png
    maskable-512.png

ANDROID
If StudyForge is already installed, do not uninstall it just to update. Publish v1.11.5 at the same HTTPS URL, open/reload that URL once in Chrome, then reopen the installed StudyForge PWA.
