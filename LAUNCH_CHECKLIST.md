# Launch checklist

Running list of items to work through before/as the site goes live. Not for public README — internal
tracking only.

## Analytics
- [ ] Pick a tool once the site is public (Cloudflare Web Analytics recommended: free, no cookie banner
      needed) and wire up the tracking snippet

## Mobile
- [x] Hamburger nav menu below 720px
- [ ] Full mobile QA pass across every page (Publications tabs, Projects tabs, Lab grids, News) — only
      Home has been checked on a narrow viewport so far

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
- [ ] Verify current status of every grant on Projects (Active/Completed/Ongoing) — some may need to
      move or be excluded
- [ ] Add CV PDF to `static/files/Vishnu_CV.pdf` (Download CV button currently 404s)
- [ ] Project briefs for 4 current UCF senior design students (Mariana Ramirez, Brett Labo, Daniel
      Bakos, William Bland) — currently placeholder text
- [ ] Real equipment photos + product links (EmotiBit, Muse 2, fNIRS, XR headsets)
- [ ] Real demo photos/video for the Demos page (currently placeholder tiles)
- [ ] 12 publications still missing a DOI/URL link (ask for the list again if needed — changes as new
      links come in)

## Before going live
- [ ] Flip repo to public (or upgrade to GitHub Pro) — GitHub Pages free tier requires a public repo
