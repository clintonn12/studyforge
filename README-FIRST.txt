StudyForge PWA v1.11.9 — Flip & Performance Hotfix

IMPORTANT BEFORE UPDATING
1. In StudyForge, make a Complete JSON Backup.
2. Keep using the SAME GitHub Pages repository and SAME URL.
3. Upload/replace the files in this folder at the repository ROOT.
4. Do NOT clear Chrome site data; your local library lives on that origin.

WHAT CHANGED
- Stability-first flashcard renderer: front and back stay mounted together.
- Flip is now a direct compositor transform and no longer causes a React render on every tap.
- Swipe movement uses requestAnimationFrame and no React state updates during drag frames.
- Current card images on BOTH sides are decoded before Study opens; upcoming images are warmed in the background.
- Study progress writes are batched during idle time instead of refreshing the full application after every grade.
- Corrected Chrome/Android flip composition: mirrored/reversed faces are prevented by a compositor-timed face handoff while keeping the same rotateY animation.
- Android hardware/system Back button is handled inside the PWA: close modal -> exit study -> close mobile nav -> deck to library -> library/settings to home.
- Topic toolbar has Open all and Close all icon buttons.
- Study all/topics/tags/progress selection is unified in one Study selection window.

LOCAL DATA COMPATIBILITY
Storage key remains: studyforge.v4
Library version remains: 12
The update does not intentionally clear localStorage or IndexedDB.

GitHub Pages update
- index.html
- sw.js
- manifest.webmanifest
- .nojekyll
- icons/
Commit to main; Pages redeploys automatically.
