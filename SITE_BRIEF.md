# Site brief — vishnuprabhu93.github.io

Read this file first. It captures every decision made while planning this site so Claude Code doesn't need it re-explained.

## Who this is for

Dr. Vishnunarayan Girishan Prabhu — Tenure-Track Assistant Professor, School of Modeling, Simulation, and Training (SMST), University of Central Florida. Director, XR BioSim Lab.

Combined faculty portfolio + lab site under one domain. Not a personal blog — a professional, citable presence for grant reviewers, prospective students, and clinical collaborators.

## Stack

- **Static site generator**: Hugo
- **Hosting**: GitHub Pages, repo `vishnuprabhu93.github.io` (user site — publishes at root domain, no subpath)
- **Deployment**: GitHub Actions, auto-builds on push to `main`
- **Repo visibility**: currently private during content assembly; will go public (or upgrade to GitHub Pro) before publishing, since GitHub Pages requires a public repo on free-tier accounts
- **Content format**: plain Markdown with YAML front matter — no CMS, no database
- **License stance**: fully open source tooling, no vendor lock-in (this replaced a Wix site for that reason)

## Site structure (final, approved)

Nav order: **Home · Publications · Projects & Funding · XR BioSim Lab · Service · Teaching · News**

### Home
- Name, title, photo, quick links (Google Scholar, LinkedIn, email, CV PDF download)
- Short intro — current role/focus only. **No career-trajectory narrative** (explicitly do not include the Kerala→Clemson→UNCC→UCF path — nobody cares, per explicit instruction)
- Research expertise tag list: Stochastic Modeling & Simulation, Biosensing & Physiological Computing, Health Systems Modeling, Digital Twins, Extended Reality (VR/AR/XR), Reinforcement Learning & Optimization, Human Behavior Modeling
- News snippet: 3-4 latest items, "See all" link to full News page
- No separate About page — identity/bio lives only on Home

### Publications
Order matters — confirmed: **Book Chapters → Journals → Conference Proceedings** (in that order, not alphabetical, not chronological across categories)
- Citation count / h-index stat block at top
- Pull from CV / Google Scholar (https://scholar.google.com/citations?user=3yTyszMAAAAJ&hl=en)

### Projects & Funding
- Three states, tabbed: **Active**, **Completed**, **Ongoing research** (research threads not tied to a specific grant)
- **Never show "Under Review" proposals** — explicit exclusion, confirmed twice
- **No dollar amounts anywhere** on this page — explicit exclusion
- 2-3 sentence plain-English description per project (not the grant-speak title alone)
- **Sponsors** section below the tabs — a simple logged list of all funder names across active/completed work (NIOSH, Stanford Health Care, NSF, NIH, Toyota Research Institute, Meta, Epic Games, Florida Blue Foundation, UCF Space Hospitality Research Awards, Montana Dept of Commerce, etc.)

### XR BioSim Lab
Four distinct subsections, in this order:
1. **Lab mission/intro** (short paragraph, teal-background highlight block in the mockup)
2. **Current students** — photo placeholder + name + role/dates + one-line project brief, card-per-student grid. Only currently active students (not full historical roster).
3. **Committee member students** — different header from "current students." Format: name, program description inline (e.g. "— Doctoral student in Industrial Engineering"), one-line description of their work. **No photo for this group.**
4. **Lab alumni** — past students/committee roles, listed with their actual thesis/dissertation title (this is the differentiator from the other groups — alumni entries center on the completed thesis title)
5. **Lab equipment & facilities** — photo placeholder per device + name + short description. Note in the mockup: "Photos and product links for each device to be added" — treat current entries as placeholders pending real photos/links (EmotiBit, Muse 2, fNIRS, XR headsets confirmed real equipment from memory notes)

### Service
Balanced detail level — confirmed explicitly: condense the long journal-reviewer list into one line ("Reviewer for 30+ journals, including JMIR, Sensors, and IEEE venues"), but **keep the full department/school/college committee list** (Faculty Search Committee, SMST Admissions Committee, SMST Student Award Committee, SMST Website Liaison, AI Initiative Rep, TIP Award Committee, etc.) — do not condense that group.

Subsections: Conference leadership, Grant review & panels, Editorial roles, Journal reviewing (condensed), Outreach (AIRE summer camps — two of them), Department/School/College committees (full).

### Teaching
- Chronological, **latest to oldest**, spans all institutions (UCF → UNC Charlotte → Clemson)
- Include ratings — confirmed explicit
- Correction on record: Spring '26 IDS 6146 rating is **4.7/5.0** (not blank/TBD as originally placeholder'd)

### News
- Own top-nav item (not just reachable via Home snippet — confirmed explicit)
- Full chronological feed
- Three entry types, all supported:
  1. Plain text entry, no link (internal update, nothing to click through)
  2. **Internal article link** → full Markdown article page on this site, own folder under `content/news/`, can include inline images with captions (see below)
  3. **External link** → opens in new tab, marked with an external-link icon, for press mentions / third-party coverage
- Original articles get full treatment: eyebrow (category + date), title, byline, body paragraphs, optional figure images with captions, related-links block at the end

## Explicit exclusions (do not add these back)

- No career-trajectory/origin-story narrative on Home
- No dollar amounts anywhere on Projects & Funding
- No "Under Review" grant listings anywhere on the public site
- No full 30+ journal reviewer list spelled out (condense to one line)
- No footer "Built with Hugo · Hosted on GitHub Pages" credit line (removed per explicit feedback)

## Design system (established in mockup, carry forward)

- **Palette**: warm paper background (#F7F5F0), deep teal (#3D5A5C / #263F41 darker variant), single burnt-clay accent (#B85C2E / #8C4520 darker variant) used sparingly — active nav state, primary CTA only. Warm gray (#85806F) for secondary/meta text. Deliberately avoided the generic "AI-generated" cream+terracotta (#D97757-adjacent) look and dark+neon look.
- **Type**: Fraunces (serif, display/headings) + Inter (body) + IBM Plex Mono (dates, stats, labels, category tags — reads like instrumentation/data-logging output, which fits a biosensing lab)
- **Signature element**: a thin waveform/signal-trace line (SVG), used as a header divider and as the small logo icon next to "XR BioSim Lab" in the nav bar. This is deliberate — it's a literal reference to the EEG/fNIRS/EDA traces the lab's actual instruments produce. Used sparingly — once as a page divider, once as the icon mark. Not overused as decoration elsewhere.
- **Logo/brand mark**: icon (small waveform SVG) + "XR BioSim Lab" wordmark, single line, no wrapping. The person's own name does NOT appear in the header/logo — only in the Home hero.
- Corners: small radius (3-4px), not heavily rounded
- No dark mode requirement specified yet — ask if it comes up

## Content sourcing

- Primary source: `Vishnu_CV.docx` (already extracted once via pandoc — ask the person if they have an updated version before re-extracting)
- Google Scholar profile: https://scholar.google.com/citations?user=3yTyszMAAAAJ&hl=en (for citation count / h-index refresh and BibTeX-style pub data)
- LinkedIn: http://www.linkedin.com/in/vgirishp

## Working style notes

- The person iterates in short, specific feedback rounds (e.g. "reorder these three things," "add a log of sponsors," "fix this one rating") — expect incremental edits, not big rewrites
- Confirm structural/content assumptions before generating large amounts of new copy — this person has corrected placeholder assumptions multiple times (e.g. rating fix, exclusion of career narrative, exclusion of dollar amounts)
- When in doubt about whether to include a piece of CV content, default to NOT including it and ask, rather than including everything by default — this person wants a curated site, not a CV dump
