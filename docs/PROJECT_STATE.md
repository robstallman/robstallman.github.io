# Project State / Handoff

_Last updated: 2026-06-19_

> Not published to the site (`docs/` is excluded in `_config.yml`), but this
> repo is **public** on GitHub — keep nothing sensitive here.

## What this is
Rob Stallman's personal site. **Primary purpose: job-seeking.** Audience is
recruiters / hiring managers, for both SWE/ML-eng and research-leaning roles
(no single focus). Designed to grow over years with minimal maintenance.
Full confirmed intent: [intent/personal-site.md](intent/personal-site.md).

## Status: LIVE ✅
- URL: https://robstallman.github.io/
- Repo: https://github.com/robstallman/robstallman.github.io (public)
- Hosting: GitHub Pages, native Jekyll build from `main` branch, root folder.
  No Actions workflow — uses only Pages-supported plugins (`jekyll-seo-tag`).
- Verified: HTTP 200, sections render, publications empty-state shows.

## Tech decisions (and why)
- **Jekyll**, because it's GitHub Pages' native generator → zero build tooling.
- **Data-driven content**: sections render from `_data/*.yml`. Adding a
  project/publication/job = edit a YAML file, commit, push. No HTML editing.
- **Single config point**: identity/links/résumé in `_config.yml`.
- Design: clean, minimal, one accent color (`theme_color` in `_config.yml`),
  system font stack, responsive. Custom CSS, no heavy theme.

## File map
- `_config.yml` — name, tagline, bio, email, social links, résumé path, accent color
- `_data/projects.yml` — project entries (currently 1 placeholder)
- `_data/publications.yml` — empty; renders "research in progress" empty-state
- `_data/experience.yml` — 1 placeholder role
- `_includes/{hero,projects,publications,experience,contact}.html` — sections
- `_layouts/default.html` — header/nav/footer/SEO
- `assets/css/style.css` — theme
- `files/` — drop `resume.pdf` here, then set `resume:` in `_config.yml`

## Local dev (note: user prefers NOT to install gems locally)
Verification has been done via the live GitHub Pages build, not local builds.
If ever needed: `bundle install` then `bundle exec jekyll serve`.

## Outstanding / next steps
1. **Replace placeholder content** — the 3 `_data/*.yml` files still hold
   placeholders. Next planned task: draft real `projects.yml` writeups from
   Rob's public repos at github.com/robstallman (survey → shortlist → draft).
2. Fill in real **bio**, **experience**, and **social links** in `_config.yml`
   / `experience.yml` (LinkedIn currently blank).
3. Add **résumé PDF** to `files/` and wire up `resume:`.
4. Publications added over time as research is published.

## Out of scope (v1)
Blog, custom domain, dark mode, contact forms/backends, analytics.
