StudyForge PWA v1.11.7 — Classic + Spaced Repetition + Performance

IMPORTANT — KEEP YOUR LOCAL CARDS
StudyForge remains local-first and keeps the same site-storage key (studyforge.v4) and library data version (12). Updating the GitHub Pages files at the SAME URL does not intentionally clear your cards.

Before updating:
1. Open your current StudyForge.
2. Make a Complete JSON Backup.
3. Do NOT clear Chrome/site data and do NOT change the GitHub Pages URL.

GitHub Pages update:
1. Extract this ZIP.
2. Upload the CONTENTS of this folder directly to the root of your existing studyforge repository.
3. Replace/overwrite index.html, sw.js, manifest.webmanifest, .nojekyll, and icons as needed.
4. Commit to main and wait for the GitHub Pages deployment green check.
5. Open the same https://...github.io/studyforge/ URL in Chrome and reload once.
6. Close and reopen the installed Android PWA.

WHAT IS NEW
• Classic desktop study counters now use the requested Still learning / Know layout with colored outlined count pills.
• New Start Flashcards chooser: Classic or Spaced repetition. It can remember the default per set.
• Spaced repetition UI: New/Learning/Review status, progress bar, Repeat / Hard / Okay / Easy rating buttons, and live next-review interval labels.
• SRS settings per set: new-card limit, review limit, include-new, due-only, Repeat/Hard/Okay learning steps, graduating interval, Easy interval, starting ease, Hard interval factor, Easy bonus, and maximum interval.
• Performance path rebuilt for study mode: swipe movement is rendered directly with requestAnimationFrame instead of rerendering React/LaTeX on every touch move; card faces are memoized; transforms are compositor-friendly.
• Images are preloaded and decoded ahead of the current card. The first study window is prepared before the session appears, then a bounded rolling window is warmed in the background.
• SRS progress is additive inside each card's existing progress object. Existing card IDs, images, topics, tags, stars, Classic progress and custom fields remain compatible.

IMAGE PERFORMANCE NOTE
The app prepares current/upcoming card images before displaying them and uses decoded browser cache for fast card changes. No browser can guarantee literal zero milliseconds for every extremely large/corrupt image or a device under severe memory pressure, but this build is designed to avoid visible image-loading flashes during normal local StudyForge use.
