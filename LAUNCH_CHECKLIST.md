# Launch checklist

Running list of items to work through before/as the site goes live. Not for public README — internal
tracking only.

## Analytics
- [x] Cloudflare Web Analytics live site-wide (token set in hugo.toml, beacon confirmed rendering on
      every page). Won't show real traffic data until the site is actually public.

## Mobile
- [x] Hamburger nav menu below 720px
- [x] Full mobile QA pass across every page (Home, Publications, Projects, Lab, Demos, Service, Teaching,
      News, article page). Found and fixed one real bug: `.proj-tabs` had no `flex-wrap`, so the tab row
      on Publications/Projects overflowed off-screen on narrow viewports instead of wrapping — some tabs
      (e.g. "Working Papers") were completely unreachable. Fixed; all grids/tables/nav confirmed clean.

## Technical SEO / visibility
- [x] Open Graph + Twitter card meta tags
- [x] Person schema.org JSON-LD on Home
- [ ] Verify `sitemap.xml` and `robots.txt` are generating correctly (Hugo defaults should cover this,
      not yet confirmed)
- [ ] Submit site to Google Search Console once public
- [ ] Cross-link from Google Scholar, ORCID, LinkedIn, and the UCF SMST faculty directory back to this
      domain (backlinks from these sources carry real weight for an academic site)
- [ ] Consider a dedicated 1200x630px social share image (currently reusing the portrait photo as
      `og:image`)
- [ ] Custom 404 page (currently Hugo's bare default)

## Content still pending
- [x] Verify current status of every grant on Projects (Active/Completed/Ongoing) — confirmed correct
- [ ] Add CV PDF to `static/files/Vishnu_CV.pdf` (Download CV button currently 404s)
- [x] Project brief for the 4 UCF senior design students — all 4 share one project (Wearable Haptic
      Glove for VR Training Simulation); moved from Current/Undergraduate to As Committee Member since
      Dr. Prabhu is committee member, not primary advisor, on that project
- [ ] Real equipment photos + product links (EmotiBit, Muse 2, fNIRS, XR headsets)
- [ ] Real photos/video for the 1 remaining placeholder Demos tile (Surgical digital twins) — both
      Closed-Loop Biosensing and Neuroadaptive XR for Clinical Training are now real interactive pages
- [ ] 11 publications still missing a DOI/URL link (ask for the list again if needed — changes as new
      links come in)
- [ ] More interactive demos, if there are others like the closed-loop biosensing one — that pattern
      (partial + shortcode + dedicated /demos/<slug>/ page + linked card) is now in place and reusable

## Before going live
- [ ] Flip repo to public (or upgrade to GitHub Pro) — GitHub Pages free tier requires a public repo
