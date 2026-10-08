StudyForge PWA v1.11.10

GitHub-ready update for the same StudyForge Pages URL.

Important:
1. Make a Complete JSON Backup in StudyForge first.
2. Upload this folder's CONTENTS to the root of the existing studyforge repository.
3. Replace index.html, sw.js, manifest.webmanifest, .nojekyll and icons as GitHub requests.
4. Commit and wait for the GitHub Pages deployment green check.
5. Open the site once in Chrome, refresh, then fully close/reopen the installed PWA.
6. Do NOT clear site data. Local decks remain under studyforge.v4 / library version 12.

Main fix: study cards no longer contain an internal scroll region; text and LaTeX are measured and fitted to the available card space. Swipe grading visibly follows the finger/mouse and exits left/right using compositor-only transforms.
