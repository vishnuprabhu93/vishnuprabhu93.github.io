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
- [x] `sitemap.xml` generates automatically (Hugo default). `robots.txt` did not (404) — added
      `enableRobotsTXT = true` plus a custom `layouts/robots.txt` template with an explicit
      `Sitemap:` directive; verified in a full production build.
- [x] Google Search Console ownership verified (HTML file method) now that the site is public.
- [ ] Sitemap submitted to Search Console (Jul 9, 2026), currently shows "Couldn't fetch." The file
      itself is confirmed valid and fetchable directly — this is very likely just Google's normal
      processing delay after a fresh public deploy. Check back in a day or two; only worth digging
      into further if it's still failing after ~48 hours.
- [x] Cross-linked from Google Scholar, ORCID, and LinkedIn back to the site. UCF SMST faculty
      directory still outstanding (likely needs a request through department staff, not self-service).
- [ ] Consider a dedicated 1200x630px social share image (currently reusing the portrait photo as
      `og:image`)
- [x] Custom 404 page — on-brand, links back to Home/Publications/Projects/Lab, verified returns a
      real HTTP 404 status

## Content still pending
- [x] Verify current status of every grant on Projects (Active/Completed/Ongoing) — confirmed correct
- [ ] Add CV PDF to `static/files/Vishnu_CV.pdf` (Download CV button currently 404s)
- [x] Project brief for the 4 UCF senior design students — all 4 share one project (Wearable Haptic
      Glove for VR Training Simulation); moved from Current/Undergraduate to As Committee Member since
      Dr. Prabhu is committee member, not primary advisor, on that project
- [ ] Real equipment photos + product links (EmotiBit, Muse 2, fNIRS, XR headsets)
- [ ] Current graduate student photos: Sayed Dariush Sajjadi added; Franklin Castillo and Siddharth
      Abrol still placeholder
- [ ] Real photos/video for the 1 remaining placeholder Demos tile (Surgical digital twins) — both
      Closed-Loop Biosensing and Neuroadaptive XR for Clinical Training are now real interactive pages
- [x] 11 working papers will not get a DOI/URL for now (confirmed) — left unlinked intentionally,
      not an oversight
- [ ] More interactive demos, if there are others like the closed-loop biosensing one — that pattern
      (partial + shortcode + dedicated /demos/<slug>/ page + linked card) is now in place and reusable

## Before going live
- [x] Repo flipped to public, Pages source set to GitHub Actions, workflow run manually triggered.
      **Site is live at https://vishnuprabhu93.github.io/** — confirmed loading real content.
