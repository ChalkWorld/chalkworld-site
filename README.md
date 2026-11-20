# chalkworld-site

Marketing + blog site for Chalk World (chalkworld.ai).

Built with Jekyll, hosted on GitHub Pages. Hosting is Phase 0 — expected
to move to a different host as CW development matures.

## Local preview

Requires Ruby 3.x and Bundler.

```bash
bundle install
bundle exec jekyll serve
# → http://127.0.0.1:4000
```

## Deploy

Push to `main`. GitHub Pages builds and serves automatically.

## Structure

- `_config.yml` — Jekyll site config
- `_layouts/` — HTML templates (default, post)
- `_includes/` — partials pulled into layouts (head, nav, footer)
- `_posts/` — blog posts (markdown, filename `YYYY-MM-DD-slug.md`)
- `assets/css/` — stylesheets
- `index.md` — homepage
- `blog.md` — blog index
- `CNAME` — custom domain (`chalkworld.ai`), read by GitHub Pages

## Companion repo

The CW engine lives at [`ChalkWorld/chalkworld`](https://github.com/ChalkWorld/chalkworld).
See `chalkworld.code-workspace` on Desktop for the Cursor multi-root
workspace spanning both repos.
