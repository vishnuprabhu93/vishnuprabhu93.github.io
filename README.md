# Vishnunarayan Girishan Prabhu — Faculty Portfolio & XR BioSim Lab

Faculty website for Dr. Vishnunarayan Girishan Prabhu, Tenure-Track Assistant Professor in the School of
Modeling, Simulation, and Training (SMST) at the University of Central Florida, and Director of the XR BioSim
Lab. The site combines a faculty portfolio — publications, teaching, and service — with the lab's own
site: current students, alumni, equipment, and research.

**Live site:** https://vishnuprabhu93.github.io

## About the lab

The XR BioSim Lab (eXtended Reality, Biosensing and Simulation) studies how extended reality, multimodal
biosensing, and adaptive digital twins can be combined to improve training, decision-making, and human
performance in complex systems, with healthcare among the primary application areas.

- Google Scholar: https://scholar.google.com/citations?user=3yTyszMAAAAJ&hl=en
- LinkedIn: http://www.linkedin.com/in/vgirishp
- Email: vishnunarayan.girishanprabhu@ucf.edu

## Tech stack

- [Hugo](https://gohugo.io/) static site generator, with a custom theme (no external theme dependency)
- Hosted on GitHub Pages
- Deployed automatically via GitHub Actions on every push to `main`
- Content is plain Markdown with YAML front matter — no CMS, no database

## Running locally

Requires [Hugo (extended)](https://gohugo.io/installation/):

```
hugo server -D
```

Then open `http://localhost:1313`.

## Site structure

```
content/
  _index.md            Home page
  publications/        Book chapters, journals, conference proceedings, working papers
  projects/             Active / Completed / Ongoing research + Sponsors log
  lab/                  XR BioSim Lab — students, alumni, equipment
  service/              Community and institutional service
  teaching/             Course history table
  news/                 News feed + individual article pages
static/images/          Photos — portrait, students, equipment, logo
static/files/           Downloadable files (e.g. CV)
layouts/                Page templates
static/css/main.css     Stylesheet
```

## Status

This site is under active development; some content is still being finalized.

## For maintainers

`SITE_BRIEF.md` documents the structural and content decisions behind the site (page layout, design system,
content rules) for anyone picking up future edits.
