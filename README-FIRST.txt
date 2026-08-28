StudyForge PWA v1.11.4 — Flashcard-Only + Topic Workflow Refinement
=======================================================================

This update is built directly on StudyForge PWA v1.11.3. It keeps the same local library version and storage keys. Updating the app files does NOT intentionally reset or replace your local flashcards.

WHAT CHANGED
- Flashcards is now the only study mode shown in the app. Learn and Test entry points were removed from the UI.
- Upload study material and Materials & notes were removed from the visible workflow. Manual cards, Batch create, and flashcard import/export remain.
- Terms in this set controls are sticky while scrolling so Hide terms, Select cards, Rearrange, and Sort remain reachable.
- Several deck/term actions are compact icon buttons. Desktop hover uses clear labels/tooltips and stronger hover contrast.
- Hide Terms now hides only the TERM side of each row; definitions remain visible.
- Topic labels inside individual term rows are hidden by default. Topic Settings has an option to show them.
- Topic Settings now supports drag-and-drop / touch-drag topic ordering. Saved order controls the Topic panels.
- Topic panel colors remain editable.
- Study only can filter by one or multiple Topics in addition to the existing tag/star/progress filters.
- Android/mobile Terms cards use a full-width stacked layout, horizontally scrollable action row, safer math overflow, and no clipped content.
- Existing image-aware card rearranging and multi-card bulk tools remain.

LOCAL DATA SAFETY
- Library data version remains 12.
- localStorage and IndexedDB keys are unchanged.
- Existing deck/card IDs, text, LaTeX, images, tags, progress, stars, deactivation state, order, folders, and unknown legacy fields are preserved by migration.
- Topic settings are additive. Older decks receive showInTerms=false and an empty topic order list; no cards are removed.
- Service-worker activation only replaces cached app-shell files. It does NOT call clear(), deleteDatabase(), localStorage.clear(), or erase browser site data.

SAFE GITHUB UPDATE
1. In StudyForge, create a Complete JSON Backup first (recommended).
2. Keep the SAME repository and SAME GitHub Pages URL, e.g. https://clintonn12.github.io/studyforge/
3. Upload the contents of this ZIP to the repository ROOT and replace matching files.
4. Commit to main. GitHub Pages redeploys automatically.
5. Open the website in Chrome and reload once so the v1.11.4 service worker activates.
6. Do NOT clear Chrome site data/storage and do NOT change to a different GitHub Pages origin if you want the same local cards.

ROOT FILES
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
If already installed, keep the app installed. Update the files on the same GitHub Pages URL, open/reload the site once in Chrome, then reopen the installed StudyForge PWA.
