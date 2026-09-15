source 'https://rubygems.org'

# github-pages pins the exact Jekyll + plugin set that GitHub Pages builds
# with (see https://pages.github.com/versions/). Keep it as the single source
# of truth; upgrade with `bundle update github-pages`.
gem "github-pages", group: :jekyll_plugins

# Plugins listed in _config.yml. Both are already part of github-pages, but
# declaring them keeps the intent explicit.
group :jekyll_plugins do
  gem 'jemoji'
  gem 'jekyll-seo-tag'
end

# NOTE: bourbon is vendored under _sass/bourbon/ and loaded from there, so the
# bourbon gem is intentionally not a dependency.
