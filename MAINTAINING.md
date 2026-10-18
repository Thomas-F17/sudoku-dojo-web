# Maintaining Sudoku Dojo

Notes for whoever hosts the app. Players only need README.md.

## Put it online with GitHub Pages (free, no command line)

1. Sign in at [github.com](https://github.com) (create a free account if needed).
2. Click **+** (top right) → **New repository**. Name it `sudoku-dojo`, set it to **Public**, and click **Create repository**.
3. On the empty repo page, click **uploading an existing file**. Drag in every file from this folder, then click **Commit changes**.
   - `.nojekyll` is hidden on a Mac (press Cmd+Shift+. in Finder to show it). It's optional, so skip it if it's fiddly.
4. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
5. After a minute or two the page shows your address: `https://YOUR-USERNAME.github.io/sudoku-dojo/`

## Install it on your iPhone

Open the address in **Safari** → tap **Share** → **Add to Home Screen**.

Do this before you build up much progress. On iPhone, the Home Screen app and Safari keep separate storage, and Safari can clear a site's data after about a week without a visit. The installed app is not cleared. If you've already played in Safari, use **Progress → Save backup** there, then **Restore** inside the installed app.

## Updating the app

Upload the new `index.html` over the old one (repo page → **Add file → Upload files**). Players get the new version the next time they open the app; the first launch after an update still shows the old one while the new one downloads in the background.

If you ever add new files that must work offline, add them to the `SHELL` list in `sw.js` and change `CACHE` to `sudoku-dojo-v2`.

## Donations

Open `index.html` on GitHub, click the pencil icon, search for `DONATE_URL`, and replace the placeholder with your page: Ko-fi or Buy Me a Coffee take a few minutes to set up; GitHub Sponsors needs an application first. On the web, Apple's in-app purchase rules don't apply, so a plain link is fine.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app: solver, generator, game, training, progress tracking. |
| `README.md` | The player guide shown on the GitHub repo page. Replace `YOUR-USERNAME` in it with your GitHub username. |
| `screenshots/` | Images used by README.md. |
| `manifest.webmanifest` | Name, icon and colours used when installed. |
| `sw.js` | Makes the app work offline. |
| `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | App icons. |
