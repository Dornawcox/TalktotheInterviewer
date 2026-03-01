# Talk to the... — Interviewer Guide & Recording Tool

A participatory ecosystem mapping interview tool developed through the OpenTEAM, Farm Hack, GOAT, and Agricultural Knowledge Concordance communities.

## Deploy to GitHub Pages

### Option A: Quickest (use `main` branch directly)

1. Create a new repo on GitHub (e.g., `talk-to-the-interviewer`)
2. Upload `index.html` to the **root** of the `main` branch
3. Go to **Settings → Pages**
4. Under "Build and deployment":
   - Source: **Deploy from a branch**
   - Branch: **main** / **/ (root)**
5. Click **Save**
6. Wait 1–2 minutes, then visit `https://YOUR-USERNAME.github.io/talk-to-the-interviewer/`

### Option B: Use `gh-pages` branch

```bash
git checkout -b gh-pages
git add index.html README.md
git commit -m "Initial deploy"
git push origin gh-pages
```

Then in Settings → Pages, set source to `gh-pages` / `/ (root)`.

### Option C: Use `/docs` folder

1. Create a `docs/` folder in your repo
2. Put `index.html` inside `docs/`
3. In Settings → Pages, set source to `main` / `/docs`

## What's Included

- **5 versioned question sets**: Core, Grazing Lands, Conservation District LWG, Farm Hack, GOSH/Open Science Hardware
- **Built-in audio recording** via browser MediaRecorder API (saves .webm locally)
- **Structured transcript export** (.txt, saves locally — nothing touches a server)
- **Consent capture** with visibility/quoting preference fields
- **Feedback mechanism** for question set improvement
- **Mobile-responsive** for field interviews on phones

## No Build Step Required

This is a single self-contained HTML file. React 18, ReactDOM, and Babel load from CDN. No npm, no webpack, no Node.js needed. Just serve the HTML file.

## Troubleshooting 404

If you see a 404 after enabling Pages:

- **Check the file is named exactly `index.html`** (lowercase, no typos)
- **Check it's in the right location** — root of the branch/folder you configured
- **Wait 2–3 minutes** — GitHub Pages can take time to build on first deploy
- **Check Settings → Pages** — it should show "Your site is live at..."
- **Check Actions tab** — look for a "pages build and deployment" workflow; if it failed, click in for details
- **Hard refresh** your browser (Ctrl+Shift+R / Cmd+Shift+R) to clear cache

## License

MIT
