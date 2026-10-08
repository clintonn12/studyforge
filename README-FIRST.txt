StudyForge PWA v1.11.8 — Performance & Stability

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
- Study screen is memo-isolated from background progress writes so deck progress updates cannot re-render the heavy card UI.
- Safer Chrome/Android 3D face composition; scrolling is moved inside the face content to avoid disappearing 3D layers.
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
