# Hill Desk

A one-page dashboard for Capitol Hill staffers: side-by-side official livestreams of the
U.S. House (Office of the Clerk, YouTube) and U.S. Senate (Senate Recording Studio) floors,
links to every committee's official livestream, live bill activity via the Congress.gov API,
and a toolkit of official floor/vote/research links. No dummy or hardcoded data — everything
comes from official congressional sources at load time.

## Deploy on GitHub Pages

1. Upload **all files in this folder** (`index.html`, `.nojekyll`, `README.md`) to the
   **root** of your GitHub repository.
2. In the repo: **Settings → Pages → Build and deployment** → Source: **Deploy from a branch**,
   Branch: **main** (root). Save.
3. Your site goes live at `https://<username>.github.io/<repo-name>/` within a couple of minutes.
   (If the repo is named `<username>.github.io`, the site is served at `https://<username>.github.io/`.)

Any other static host (Netlify, office web server, etc.) works the same way — just serve `index.html`.

## Notes

- This is a fully static site: **no build step, no dependencies, no `package.json` needed.**
- The House YouTube player requires the page to be served from a real URL. It will show
  "Error 153" if you open `index.html` directly from disk — that disappears once deployed.
- `.nojekyll` tells GitHub Pages to publish the files as-is.

## Official sources used

- House floor: Office of the Clerk — live.house.gov / [US House Clerk on YouTube](https://www.youtube.com/@USHouseClerk)
- Senate floor: Senate Recording Studio — [senate.gov floor webcast](https://www.senate.gov/floor/live-floor-proceedings.htm) / floor.senate.gov
- House committees: each committee's official YouTube channel and .house.gov site
- Senate committees: each committee's hearing pages (Senate ISVP player)
- Legislative data: [Congress.gov API](https://api.congress.gov/) (visitors supply their own free key)
