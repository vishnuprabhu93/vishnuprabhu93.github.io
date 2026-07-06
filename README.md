# vishnuprabhu93.github.io

Faculty portfolio + XR BioSim Lab site. Built with Hugo, deployed via GitHub Actions to GitHub Pages.

## Start here

Read `SITE_BRIEF.md` first — it has the full set of structural and content decisions already made, so you
don't need to re-derive them. This applies whether you're Claude Code or a future human editor.

## Local development

```
hugo server -D
```
Then open `http://localhost:1313`.

## Structure

```
content/
  _index.md          Home page
  publications/       Book chapters, journals, conference proceedings (in that order)
  projects/           Active / Completed / Ongoing research + Sponsors log
  lab/                XR BioSim Lab — students, alumni, equipment
  service/            Community and institutional service
  teaching/           Course history table
  news/               News feed + individual article pages
static/images/        Photos — students, equipment, logo
```

## Deployment

Push to `main` → GitHub Actions (`.github/workflows/hugo.yml`) builds and publishes automatically. No manual
deploy step. Repo is currently **private** — GitHub Pages on the free tier requires a public repo to actually
serve the built site, so this needs to flip to public (or the account needs GitHub Pro) before the site goes
live.

## Outstanding TODOs

- [ ] Choose/build the actual Hugo theme (currently unset in `hugo.toml`) — matches the mockup's design system
      described in `SITE_BRIEF.md` (warm paper background, teal + clay accent, Fraunces/Inter/IBM Plex Mono)
- [ ] Pull complete, verified publication list from CV / Google Scholar
- [ ] Verify current funding status of each grant before publishing (Active vs Completed vs excluded)
- [ ] Add real student photos
- [ ] Add real equipment photos + product links
- [ ] Add CV PDF to `static/files/`
- [ ] Decide on repo visibility / GitHub Pro before going live
