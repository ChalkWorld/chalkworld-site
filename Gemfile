source "https://rubygems.org"

# Pin to the github-pages gem so local builds match GitHub Pages' build
# environment. Version list: https://pages.github.com/versions/
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-seo-tag", "~> 2.8"
end

# Windows / JRuby compatibility (safe no-ops on macOS)
install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
  gem "wdm", "~> 0.1.1"
end

gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
