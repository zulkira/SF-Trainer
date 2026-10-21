# Ryu Training Lab — iPhone Home Screen PWA

A static, mobile-friendly PWA starter for personal SF6 practice. It does not connect to Buckler or request credentials.

## Features
- Home dashboard with current/target MR, focus cue and reset routine
- Replay review logs, including Replay Takeover test and next-match cue
- Pro Replay Lab: YouTube watchlist, player/matchup metadata, timestamped observations, guided analysis prompts, and applied-lesson tracking
- FT5/FT10/FT15 long-set logs with opponent habits and adaptations
- Playbook and progress page
- Local browser storage, JSON export and merge-import (keeps existing replay and long-set entries; duplicate IDs are skipped), and clear-data control
- PWA manifest, service worker and app icons for Home Screen installation

## Publish free with GitHub Pages
1. On your Mac, unzip the project.
2. Sign in to GitHub and create a **public** repository named `ryu-training-lab`.
3. Upload the contents of this folder to the repository root (`index.html`, `manifest.webmanifest`, `sw.js`, `icons/`, `README.md`). Do not upload the ZIP itself as the only file.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**, choose `main` and `/(root)`, then Save.
6. Wait for GitHub Pages to publish. The URL will usually be `https://YOUR-USERNAME.github.io/ryu-training-lab/`.
7. Open that URL in Safari on your iPhone, tap **Share → Add to Home Screen**, enable **Open as Web App** if shown, then tap Add.

## Pro Replay Lab workflow
1. Open **Pro Lab → Add pro match** and paste a YouTube HTTPS link (`youtube.com` or `youtu.be`).
2. Add player names, characters, tournament/set, and a question you want to answer.
3. Save timestamped observations. For each, record what happened, why it worked or failed, and what you normally do.
4. Write one cue for your own matches, then track whether you practised or applied it and what happened.
5. Use **Progress → Export backup JSON** regularly. The export includes Pro Replay Lab entries and observations.

## Important data note
Logs are stored in localStorage in the browser profile that uses the app. They do not automatically sync across devices. Export a JSON backup before clearing Safari website data or moving to another device. Import now merges entries and skips duplicate IDs, which helps preserve existing replay and long-set logs. It does not automatically reconcile edits to an entry with the same ID; the current local entry is kept.

## Updating the app
Upload updated files to the repository. The service worker cache version has been bumped for this release. If an old version remains visible, close the Home Screen app fully, reopen it, and refresh the site in Safari. Export your logs before major changes.

## Scope and privacy
This is a static PWA, not a native iOS `.ipa`. It has no account system, analytics, server-side database, passwords, session cookies, or Buckler integration. Treat any public repository as public source code; personal logs stay in the browser unless you export them yourself.
