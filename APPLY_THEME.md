# How to apply this theme package

This zip contains the actual Hugo templates (`layouts/`), stylesheet (`static/css/main.css`), and two
**updated content files** that replace simpler versions from the first scaffold.

## What's new vs. the original scaffold

- `layouts/` — did not exist before; this is the real template code that turns your Markdown into the
  designed site (header, nav, hero, tabs, cards — everything from the mockup)
- `static/css/main.css` — the full stylesheet, ported directly from the approved mockup
- `content/projects/_index.md` — **replaces** the original file. Restructured to use YAML front-matter
  fields (`active`, `completed`, `ongoing`, `sponsors`) instead of one flowing Markdown body, so the
  tabbed Active/Completed/Ongoing layout can render each section independently.
- `content/lab/_index.md` — **replaces** the original file. Restructured to use YAML front-matter arrays
  (`currentStudents`, `committeeStudents`, `alumni`, `equipment`) so each card can pull structured fields
  (photo, role, brief) instead of freeform prose.
- `content/news/sample-article/index.md` — same article as before, with the image now using proper
  `<figure>`/`<figcaption>` markup instead of a placeholder.
- `content/news/press-mention-example/index.md` — new, demonstrates the "external link" news pattern
  (press mentions that open in a new tab, marked with an arrow icon).

**Publications, Service, and Teaching content files are unchanged** — the new `layouts/publications.html`,
`layouts/service.html`, and `layouts/teaching.html` templates render their existing Markdown as-is.

## Merge steps (Windows / PowerShell)

Assuming this zip is unzipped to `C:\Users\vishn\Claude\theme-package`, and your repo is at
`C:\Users\vishn\Claude\vishnuprabhu93.github.io`:

```powershell
Copy-Item -Path "C:\Users\vishn\Claude\theme-package\*" -Destination "C:\Users\vishn\Claude\vishnuprabhu93.github.io" -Recurse -Force
```

This will:
- Add the new `layouts/` folder and its templates
- Add `static/css/main.css`
- Overwrite `content/projects/_index.md` and `content/lab/_index.md` with the restructured versions
- Add the two new `content/news/` entries

## After merging

Preview it locally before pushing:

```powershell
cd C:\Users\vishn\Claude\vishnuprabhu93.github.io
hugo server -D
```

Open `http://localhost:1313` in a browser. If Hugo isn't installed yet, Claude Code can install it, or you
can grab it from https://gohugo.io/installation/windows/ (the `extended` version, needed for some asset
processing).

If it looks right, commit and push:

```powershell
git add .
git commit -m "Add Hugo theme templates and stylesheet"
git push
```

## What Claude Code should do next

This is a working first skeleton, not a finished site. Real next steps, in rough priority order:

1. Verify the site actually builds and renders correctly with `hugo server -D` — fix any template errors
2. Add a real portrait photo at `static/images/portrait.jpg` (referenced by `layouts/index.html`)
3. Pull the complete, verified publication list from the CV / Google Scholar into
   `content/publications/_index.md` (current content is a partial example, flagged with a TODO comment)
4. Double check every grant's actual current status before publishing — some may need to move between
   Active / Completed, or be excluded entirely if still under review (flagged with a TODO comment in
   `content/projects/_index.md`)
5. Add real student and equipment photos, referenced via the `photo` fields in `content/lab/_index.md`
6. Review typography/spacing on an actual rendered page vs. the original mockup — some fine-tuning is
   likely needed once real content (which will vary in length from the placeholder text) is in place
7. Decide on and add favicon, Open Graph / social share meta tags, and analytics (if wanted) — none of
   these exist yet
