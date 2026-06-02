# jhforster.github.io
Personal website / blog.

Mostly a playground to learn Jekyll and other tech stuff that interests me. But I do like having a presence online that I can host for free and maintain myself.

## Local development

This site is built with Jekyll and GitHub Pages. The repo uses `rbenv`; `.ruby-version` should select the expected Ruby version automatically.

Install dependencies:

```sh
rbenv exec bundle install
```

Run the site locally:

```sh
rbenv exec bundle exec jekyll serve
```

Then open:

```text
http://localhost:4000
```

If you change `_config.yml`, restart the Jekyll server. Jekyll does not reliably reload config changes while the server is running.

Build the static site:

```sh
rbenv exec bundle exec jekyll build
```

The generated output goes into `_site/`, which is ignored by git.

## Deployment

This is a GitHub Pages repo. To deploy, commit the source changes and push to `master`:

```sh
git status
git add .
git commit -m "Update site"
git push origin master
```

GitHub Pages builds and publishes the site from the pushed source.

## Project structure

- `_config.yml` - site-wide Jekyll config, collections, metadata, and plugins.
- `index.html` - homepage content and feature grid.
- `about.md` - About page copy.
- `blog/index.html` - blog listing page.
- `_posts/` - dated blog posts.
- `_drafts/` - unpublished draft posts.
- `_writing/` - older writing collection.
- `_features/` - homepage feature cards for writing, projects, podcasts, talks, and games.
- `_layouts/` - page templates.
- `_includes/` - shared template partials, such as nav, head, footer, analytics, and favicons.
- `_sass/` - source Sass partials.
- `css/styles.scss` - Sass entrypoint that imports the site styles.
- `assets/` - site images, icons, and share images.
- `tumblr_files/` - imported Tumblr-era media.
- `_site/` - generated static output from Jekyll; do not edit directly.
