# Gemfile
source "https://rubygems.org"

# Core Jekyll
gem "jekyll", "~> 4.1"

# Theme deps from your gemspec (pinned same as spec)
gem "jekyll-sitemap",         "~> 1.4.0"
gem "jekyll-mentions",        "~> 1.6.0"
gem "jekyll-paginate",        "~> 1.1.0"
gem "jekyll-seo-tag",         "~> 2.7.1"
gem "jekyll-redirect-from",   "~> 0.16"
gem "jekyll-feed",            "~> 0.15"
gem "jekyll-commonmark",      "~> 1.3.1"
gem "jekyll-include-cache",   "~> 0.2"
gem "jemoji",                 "~> 0.12"

# ✅ Dart Sass pipeline (modern, fixes global-builtin deprecation complaints in practice)
# jekyll-sass-converter v3 switches Jekyll to Dart Sass via sass-embedded
gem "jekyll-sass-converter",  "~> 3.0"
gem "sass-embedded",          ">= 1.77"   # keep current; Dart Sass engine

# Optional dev niceties
group :development do
  gem "webrick", "~> 1.8"   # Ruby 3 compatibility for `bundle exec jekyll serve`
end
