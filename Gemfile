source "https://rubygems.org"

gem "minimal-mistakes-jekyll"
gem "github-pages", group: :jekyll_plugins
gem "jekyll-include-cache", group: :jekyll_plugins

# Ruby 3.0 dropped webrick from the default gems, and Jekyll 3.9's
# `serve` command still requires it. Local preview only -- GitHub Pages
# builds server-side and does not read this Gemfile.
gem "webrick", "~> 1.8"