StudyForge PWA v1.11.3 — Topics & Bulk Card Tools
==================================================

This update is built directly on StudyForge PWA v1.11.2. Existing local flashcards are NOT reset or replaced.

NEW FEATURES
- Every deck has a Topic category enabled by default.
- Rename Topic to Chapter, Unit, Section, Module, etc., or turn it off per deck.
- Turning Topics off only hides/grouping UI; existing topic assignments remain saved.
- Terms in this set is organized into collapsible topic panels when Topics are enabled.
- Each topic panel has its own editable color.
- Multi-select cards → Assign tags / topic.
- Multi-select cards → Move / copy selected to another deck.
- Rearrange mode now shows term/definition image thumbnails. Tap a thumbnail for the full-screen image viewer.
- Batch create supports: Term: {...} Definition: {...} Topic: {...} Tags: {...}. Topic and Tags are optional.
- Flashcard Study settings have separate Show topic label and Show tags controls.
- Topic label is visually larger than the tag chips and is responsive on Android/mobile.
- Search now includes topic text.
- CSV/StudyForge card exports preserve topic information.

LOCAL DATA SAFETY
- StudyForge library version remains 12.
- Existing card IDs and deck IDs are preserved.
- Existing cards without a topic migrate to topic=""; no card is removed.
- Existing images, progress, stars, tags, deactivated-card state, order, folders, notes, and settings remain.
- Existing IndexedDB/localStorage keys are unchanged.
- The service worker update only replaces cached APPLICATION FILES. It does not delete browser site data.

IMPORTANT WHEN UPDATING GITHUB PAGES
1. Keep using the SAME GitHub Pages URL/origin you already use for StudyForge.
2. Upload/replace the new index.html, manifest.webmanifest, sw.js, icons/, and .nojekyll at the repository root.
3. Commit the changes. GitHub Pages redeploys automatically.
4. Open StudyForge and reload once. The PWA service worker updates to v1.11.3.
5. DO NOT use Chrome → Clear storage / Clear site data. That would erase local-only browser data.
6. A complete JSON backup before any major update is still recommended.

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
The existing responsive Android UI and swipe-study behavior from v1.11.2 are retained. If StudyForge is already installed, updating the files at the same GitHub Pages URL updates the installed PWA; you do not need to uninstall it.
