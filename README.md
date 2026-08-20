# Sureal Report Reviewer — Manual (hosted)

This is the **public, canonical manual** for the Sureal Report Reviewer, served via
GitHub Pages. One hand-editable HTML file, no build step — that is a feature.

- Live page: enable GitHub Pages on this repo (Settings → Pages → Deploy from branch
  → `main`, root). The URL is `https://<owner>.github.io/<repo>/`.
- The app ships a **snapshot** of `index.html` as its offline Manual page. The
  snapshot is refreshed at normal app releases by copying `index.html` over the
  app's bundled `MANUAL.html`. Never edit two copies — this repo is the source
  of truth; snapshot staleness in the app is expected and bannered.

## How to update the manual

1. Edit `index.html` (it is self-contained: inline CSS, vanilla JS calculator).
2. Add a one-line entry to the changelog section at the bottom of the page and
   bump the header stamp if the change is substantive.
3. Commit and push. Live in about a minute. No app release, no fleet action.

## Rules for this page (it is PUBLIC)

- No client project/building names or addresses. No client company names.
- No reviewer or staff surnames. Maintainer credit is "Sureal", nothing more.
- No repository URLs, PAT mechanics, or installer internals — the only permitted
  phrasing is "Sureal sends you a personal installer".
- No screenshots or excerpts containing client data.
- Evidence in aggregate only ("14 real client reports across 12 credit modules").
- Every number must trace to the QA artifacts or run transcripts. Untraceable
  numbers do not go on the page.

The full checklist lives as a comment at the top of `index.html`, and
`publish_manual.sh` (kept in the private product tooling, not in this repo)
greps for known forbidden strings before every push.
