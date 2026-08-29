StudyForge PWA v1.11.6 — UI, Settings & Mobile LaTeX Cleanup
============================================================

This release is built directly on StudyForge PWA v1.11.5. It keeps the same local library data version and the same browser-storage key. Updating these app files at the SAME GitHub Pages URL does NOT intentionally reset, replace, or delete your local flashcards.

MAIN CHANGES
- Fixed Android/mobile inline LaTeX in Terms in this set. Inline math stays in the surrounding sentence; display math can scroll horizontally when it is wider than the phone.
- Reworked tool icons so study, batch create/import, selection, rearranging, move/copy, and include/exclude-from-study actions are more visually distinct.
- Removed the duplicate hover-label behavior. Desktop icon controls use one StudyForge tooltip; mobile does not depend on hover.
- Reduced repeated per-card buttons. Primary actions stay visible; Duplicate, Move/Copy, and Delete are grouped under one More menu.
- Consolidated set-specific controls under one Flashcard Set Settings panel. The redundant deck-header and preview settings gears were removed; the sticky Terms gear is the single deck-settings entry point.
- Flashcard Set Settings now includes:
  * first side (Definition first / Term first)
  * shuffle new sessions
  * show/hide card images
  * fit content automatically
  * automatic read aloud
  * show Topic in study
  * show tags in study
  * study text size
  * flip animation speed
  * mobile swipe sensitivity (Easy / Normal / Firm)
  * text alignment
  * image alignment
  * show/hide tags in Terms in this set
  * show/hide Topic label on each term
  * Topic grouping, category name, topic order, and topic panel colors
  * mark the set 100% studied
  * reset progress
- Existing Topics, study-by-topic filters, bulk selection, bulk tags/topics, move/copy, image-aware rearranging, PWA/offline shell, and Android swipe remain.

LOCAL DATA SAFETY
- Library data version remains 12.
- Main localStorage key remains studyforge.v4.
- Existing cards/decks are migrated additively; unknown older fields are spread back into each object rather than discarded.
- Existing IDs, Terms, Definitions, LaTeX, images, tags, Topics, progress, stars, deactivation state, card order, folders, and study sessions are not intentionally replaced by this update.
- The service worker only updates cached app-shell files. It does not call localStorage.clear() or indexedDB.deleteDatabase().

SAFE GITHUB UPDATE
1. In your currently working StudyForge, make a Complete JSON Backup first.
2. Keep the SAME repository and SAME GitHub Pages URL, for example:
   https://clintonn12.github.io/studyforge/
3. Extract this ZIP.
4. Upload the CONTENTS directly to the repository ROOT, replacing matching files such as index.html, sw.js, manifest.webmanifest, and icons.
5. Commit to main. GitHub Pages redeploys automatically.
6. Wait for the Pages deployment to show a green check.
7. Open the StudyForge website in Chrome and reload once so the v1.11.6 service worker/app shell becomes active.
8. Close and reopen the installed Android PWA.
9. Do NOT clear Chrome site data/storage.

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

ANDROID UPDATE NOTE
If StudyForge is already installed, do not uninstall it just to update. Keep the same HTTPS URL, publish v1.11.6 there, reload that URL once in Chrome, then reopen the installed StudyForge PWA.
