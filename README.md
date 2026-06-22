# Write Like a Native

A blog helping junior-school kids learning English as a second language improve
their writing skills. Built as a [Jekyll](https://jekyllrb.com/) site and served
via **GitHub Pages**.

## Adding a post
Add a markdown file to [`_posts/`](_posts/) named `YYYY-MM-DD-slug.md` with Jekyll
front matter (`layout: post`, `title`, `date`), then commit and push. GitHub Pages
rebuilds and the post goes live. New posts automatically appear in the calendar
and archive columns.

## Local preview (optional)
```bash
bundle install      # needs Ruby + the github-pages gem
bundle exec jekyll serve
```
Deployment itself needs no local build — GitHub Pages builds on push.

## Structure
- `_config.yml` — site config (theme: minima, jekyll-feed)
- `index.md` — home page: posts list + calendar/archive sidebar
- `archive.md` — full archive grouped by year/month
- `_posts/` — one markdown file per published post
