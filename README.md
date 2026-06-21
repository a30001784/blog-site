# blog-site

The published blog application — a [Jekyll](https://jekyllrb.com/) site served via
**GitHub Pages**. Posts here are generated automatically by the
[blog-writer agent](https://github.com/a30001784/blog-writer-agent).

## How posts get here
The agent's `publish.py` converts each finished blog post into a Jekyll entry in
[`_posts/`](_posts/) (filename `YYYY-MM-DD-slug.md` with front matter), then
commits and pushes to this repo. GitHub Pages rebuilds and the post goes live.

## Local preview (optional)
```bash
bundle install      # needs Ruby + the github-pages gem
bundle exec jekyll serve
```
Deployment itself needs no local build — GitHub Pages builds on push.

## Structure
- `_config.yml` — site config (theme: minima, jekyll-feed)
- `index.md` — home page, lists posts newest-first
- `_posts/` — one markdown file per published post
