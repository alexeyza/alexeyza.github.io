# alexeyza.com

Source of my personal website: a short bio, CV, publications, and a few old blog
posts. Built with [Jekyll](https://jekyllrb.com/) 3 via the
[`github-pages`](https://github.com/github/pages-gem) gem and served by GitHub Pages
at https://alexeyza.com.

## How it deploys

Every push to `master` runs `.github/workflows/pages.yml`, which installs the gems
pinned in `Gemfile.lock`, runs `github-pages build` (safe mode, GitHub's plugin
whitelist), and deploys the result to GitHub Pages. The site is live a minute or so
after the push. Build logs: repository → Actions → "Deploy site to GitHub Pages".

Dependabot opens weekly PRs for gem and workflow-action updates
(`.github/dependabot.yml`). If a merged update breaks the build, the site keeps
serving the last successful deploy until the PR is fixed or reverted.

## Editing content

- **Pages** are Markdown files in the repository root (`about.md`, `publications.md`,
  ...) with a `layout: page` front matter and a `permalink`. Links from the home page
  live in `index.html`.
- **Posts** go in `_posts/` as `YYYY-MM-DD-title.markdown` with `layout: post` front
  matter (see existing posts for the fields used).
- **PDFs** (CV, papers) live in `pdf/`; images in `assets/images/`.
- Site-wide settings (title, social links, plugins) are in `_config.yml`.

## Building locally

Nothing needs to be installed on the host. Use a throwaway Ruby container:

```bash
docker run --rm -it -p 4000:4000 \
  -v "$PWD":/srv/site -w /srv/site \
  -v az-pages-bundle:/bundle -e BUNDLE_PATH=/bundle \
  ruby:3.3 bash -c 'bundle install && bundle exec jekyll serve --host 0.0.0.0'
```

Then open http://localhost:4000. To clean up afterwards:

```bash
docker volume rm az-pages-bundle
docker rmi ruby:3.3
```

## Updating dependencies

`github-pages` pins the whole Jekyll/plugin set that GitHub Pages supports. To move to
a newer release of it, run `bundle update github-pages` inside the container above and
commit the resulting `Gemfile.lock`.
