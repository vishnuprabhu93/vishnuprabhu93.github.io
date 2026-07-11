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
- [x] Fixed two more bugs user caught in the wild: (1) Home page portrait had `display: none` below
      720px, hiding the photo entirely on mobile — now shows centered above the name at 160x190. (2) The
      closed-loop biosensing demo's intro block used a bare `<header>` tag, which inherited the site's
      global `header { position: sticky; top: 0; }` nav rule and pinned it to the viewport top while
      scrolling, on both desktop and mobile. Changed to a `<div>`; scrolls normally now, matching the
      neuroadaptive-xr-training demo.

## Technical SEO / visibility
- [x] Open Graph + Twitter card meta tags
- [x] Person schema.org JSON-LD on Home
- [x] `sitemap.xml` generates automatically (Hugo default). `robots.txt` did not (404) — added
      `enableRobotsTXT = true` plus a custom `layouts/robots.txt` template with an explicit
      `Sitemap:` directive; verified in a full production build.
- [x] Google Search Console ownership verified (HTML file method) now that the site is public.
- [ ] Sitemap submitted to Search Console (Jul 9, 2026), still shows "Couldn't fetch" as of the last
      check. The file itself is confirmed valid and fetchable directly (200, correct content-type).
      Likely still just Google's indexing delay for a new github.io property; worth a fresh
      remove-and-resubmit if it's still stuck.
- [x] Cross-linked from Google Scholar, ORCID, and LinkedIn back to the site. UCF SMST faculty
      directory still outstanding (likely needs a request through department staff, not self-service).
- [x] Dedicated 1200x630px social share image (`static/images/social-share.jpg`) using the site's
      brand mark + name/role/affiliation/research tags, wired as `og:image`/`twitter:image`. Person
      schema `image` still points at the real portrait photo (kept separate intentionally).
- [x] Custom 404 page — on-brand, links back to Home/Publications/Projects/Lab, verified returns a
      real HTTP 404 status
- [x] "XR BioSim Lab" mentions on Home ("Director, XR BioSim Lab") and the footer are now clickable
      links to `/lab/`. Nav logo left linking Home (standard convention).
- [x] Fixed a real bug: `.article-body` had no link styling anywhere on the site, so any in-body link
      (e.g. the Healthy Aging Fair video link) was invisible — same color/no underline as plain text.
      Added teal/clay underline treatment matching `.news-link` used elsewhere.

## Content still pending
- [x] Verify current status of every grant on Projects (Active/Completed/Ongoing) — confirmed correct
- [ ] Add CV PDF to `static/files/Vishnu_CV.pdf` (Download CV button currently 404s)
- [x] Project brief for the 4 UCF senior design students — all 4 share one project (Wearable Haptic
      Glove for VR Training Simulation); moved from Current/Undergraduate to As Committee Member since
      Dr. Prabhu is committee member, not primary advisor, on that project
- [ ] Real equipment photos + product links (EmotiBit, Muse 2, fNIRS, XR headsets)
- [x] Current graduate students: Sayed Mohammad (Dariush) Sajjadi, Siddharth Abrol, Franklin Castillo,
      and Ishita Pathuri all added with photos and full bios (Ishita's rewritten to third person to
      match the others). Ordered Dariush, Sid, Frank, Ishita per Dr. Prabhu's request. Cards are
      visibly different heights since brief lengths vary — confirmed intentional.
- [ ] Real photos/video for the 1 remaining placeholder Demos tile (Surgical digital twins) — both
      Closed-Loop Biosensing and Neuroadaptive XR for Clinical Training are now real interactive pages.
      Explicitly deferred by Dr. Prabhu ("We will do this demo later"); a ready-to-use build prompt
      already exists from an earlier session.
- [x] 11 working papers will not get a DOI/URL for now (confirmed) — left unlinked intentionally,
      not an oversight
- [ ] More interactive demos, if there are others like the closed-loop biosensing one — that pattern
      (partial + shortcode + dedicated /demos/<slug>/ page + linked card) is now in place and reusable
- [x] Added a 2026 Swami et al. journal publication (Environment International) to Publications;
      totalPubs 52 -> 53
- [x] Added 3 outreach news stories with photo/video galleries: UCF Healthy Aging Fair (March 2026,
      includes a YouTube link to Dr. Prabhu's Meta smart glasses demo), Rosen Summer Institute (June
      2026), and NeoCity Summer Camp (July 2026, corrected to be framed as a separate cohort from
      Rosen, not the same one)
- [x] Built a reusable photo/video gallery system: any news story with `gallery` front matter (+
      optional `relatedDemo`) automatically renders on both its own article page and grouped under
      "From the field" on the Demos page. Currently populated for all 3 outreach stories above.
- [ ] NeoCity has 7 raw video clips (~89MB total) that were never used — too large to commit directly
      to the repo. If Dr. Prabhu uploads them to YouTube (unlisted is fine), they can be wired into the
      NeoCity gallery the same way the Healthy Aging Fair video was.

## Before going live
- [x] Repo flipped to public, Pages source set to GitHub Actions, workflow run manually triggered.
      **Site is live at https://vishnuprabhu93.github.io/** — confirmed loading real content.
