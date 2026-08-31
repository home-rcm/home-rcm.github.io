# HOME

Jekyll site for HOME, a research platform for remote clinical monitoring. Deployed via GitHub Pages.

## Local development

1. Install `ruby`, `jekyll`, and `bundler` per the [Jekyll installation guide](https://jekyllrb.com/docs/installation/)
2. Install dependencies: `bundle install`
3. Serve the site and watch for markup/sass changes: `bundle exec jekyll serve`
4. View your website at http://127.0.0.1:4000/

## Structure

- `index.html` — home page (Hero)
- `_config.yml` — site configuration (name, collections, plugins)
- `_layouts/` — page layouts (`default.html`, `page.html`)
- `_includes/` — reusable partials (`meta.html`, `team_grid.html`)
- `_data/team.yml` — team members
- `_publications/*.md` — one file per publication with YAML front matter
- `style.scss` — styles (compiled to `style.css` by Jekyll)
- `script.js` — behavior (footer year, mobile nav toggle, contact form)
- `images/` — photos and logos (hero, platform, members, partners)

## Adding a team member

Add an entry to `_data/team.yml`:

| Field | Details |
| --- | --- |
| `name` | First and last name |
| `title` | Role and affiliation |
| `bio` | Short biography |
| `image` | Path to their photo in `images/members/` |

## Adding a publication

Create a new file in `_publications/` with the following fields:

| Field | Details |
| --- | --- |
| `title` | Publication title |
| `authors` | YAML list, one full name per line |
| `venue` | Full name of the publication venue |
| `date` | Publication date (e.g., `2026-02-01`) |
| `link` | External link to the paper |

Authors render as "First Last" read straight from the publication file. Team members can be listed by their `id` from `_data/team.yml` (e.g. `rob`, `andrea`); they render bold. If a name is still abbreviated (e.g. `"Wu, R."`), it renders highlighted so you can spot it — replace it with the full name directly in the file.

## Deployment

Pushes to `main` deploy automatically via GitHub Pages. Live at home-rcm.github.io