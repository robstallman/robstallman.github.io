# robstallman.github.io

Personal site — coding projects, research, and experience. Built with [Jekyll](https://jekyllrb.com/) and served by GitHub Pages.

## Editing content (no code needed)

Everything lives in two places:

| What | Where |
|------|-------|
| Your name, tagline, bio, email, social links, résumé | [`_config.yml`](_config.yml) |
| Projects | [`_data/projects.yml`](_data/projects.yml) |
| Publications | [`_data/publications.yml`](_data/publications.yml) |
| Experience | [`_data/experience.yml`](_data/experience.yml) |

To add a project, publication, or job, copy an existing block in the relevant
`_data/*.yml` file and edit the fields. Each file has comments explaining the
fields. Empty sections show a friendly "coming soon" message automatically.

To add a résumé: drop `resume.pdf` in [`files/`](files/) and set
`resume: "/files/resume.pdf"` in `_config.yml`.

## Running locally

```bash
bundle install          # first time only
bundle exec jekyll serve # → http://localhost:4000
```

Edits to `_data/*.yml` require restarting `jekyll serve` to take effect.

## Deploying

This repo is a GitHub user site, so deployment is automatic:

1. Create a repo named **`robstallman.github.io`** on GitHub.
2. Push this directory to its `main` branch.
3. In the repo's **Settings → Pages**, set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. The site goes live at https://robstallman.github.io within a minute or two.

No build step or Actions workflow is needed — GitHub Pages builds the Jekyll
site for you, because it uses only supported plugins.
