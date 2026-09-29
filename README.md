# Goldilocks Web

Static HTML/CSS/JS source for [goldilocks.ac.uk](https://goldilocks.ac.uk/), the landing page for the Goldilocks ecosystem, split across three pages:

- `public/index.html` — home page: project overview, funders, and links to Data / ML / Core / Agent
- `public/core.html` — Core / Workbench entry point
- `public/agent.html` — Agent entry point (online + download)

An "About" overlay (project overview, challenge, solution, outcomes, people, organisations) and a "Contact" overlay are available from the nav on every page, powered by `public/script.js`.

## Run locally

No build step required. Either open `public/index.html` directly in a browser, or serve the folder:

```sh
cd public
python3 -m http.server 8000
```

Then visit `http://localhost:8000/index.html`.

## Deployment

Pushes to `main` trigger `.github/workflows/static.yml`, which publishes the `public/` folder to GitHub Pages behind the `goldilocks.ac.uk` custom domain. There is no build step — whatever is in `public/` on `main` is what goes live.
