# ProVid · 1st Workshop on Proactive Video Models (CVPR 2027)

Placeholder website for the ProVid workshop proposal: one static page, no build step, no JavaScript.

## Preview locally

```bash
python3 -m http.server 8000   # run inside this folder, then open http://localhost:8000
```

Or open `index.html` directly in a browser.

## Edit

- **Text**: `index.html`, one commented block per section (Overview, Topics, Call for Papers, Competition, Schedule, Invited Speakers, Organizers).
- **Colours and spacing**: the variables at the top of `assets/css/style.css`.
- **Photos**: `assets/img/people/<firstname-lastname>.jpg`, square, 400×400. `placeholder.svg` is the fallback.

## Deploy on GitHub Pages

Every link and asset path is relative, so this folder works at any address. On a free GitHub plan, Pages only works with a **public** repository.

- **Organization site** (`https://<org>.github.io/`): create the org, create a public repository named exactly `<org>.github.io`, and push the contents of this folder to `main`.
- **Project site** (`https://<owner>.github.io/<repo>/`): push this folder to a public repository, then go to Settings → Pages → Build and deployment → "Deploy from a branch" → `main` / `(root)`.

Run these commands **inside this `website/` folder**. Don't run them in the parent folder: it holds the proposal PDF, and `git add .` there would publish it.

```bash
git init -b main
git add .
git commit -m "ProVid placeholder site"
git remote add origin https://github.com/<owner>/<repo>.git
git push -u origin main
```

For either option, check under Settings → Pages that the source is `main` / `(root)`. The empty `.nojekyll` file makes Pages serve the files as they are, without running Jekyll.
