# frozen_string_literal: true

source "https://rubygems.org"

gem "rake", "~> 13.0"

group :development do
  gem "launchy", "~> 2.3"
  gem "pry"

  gem "pry-byebug" unless RUBY_ENGINE == "jruby"
end

#


#

group :test_legacy do
  gem "test-unit" if RUBY_PLATFORM =~ %r!cygwin!

  gem "minitest"
  gem "minitest-profile"
  gem "minitest-reporters"
  gem "shoulda"
  gem "simplecov"
end

#

group :benchmark do
  if ENV["BENCHMARK"]
    gem "benchmark-ips"
    gem "rbtrace"
    gem "ruby-prof"
    gem "stackprof"
  end
end

#

group :jekyll_optional_dependencies do
  gem "jekyll-coffeescript"
  gem "jekyll-docs", :path => "../docs" if Dir.exist?("../docs") && ENV["JEKYLL_VERSION"]
  gem "jekyll-feed", "~> 0.9"
  gem "jekyll-gist"
  gem "jekyll-paginate"
  gem "jekyll-redirect-from"
  gem "kramdown-syntax-coderay"
  gem "mime-types", "~> 3.0"
  gem "rdoc", "~> 6.0"
  gem "tomlrb"

  platforms :ruby, :mswin, :mingw, :x64_mingw do
    gem "classifier-reborn", "~> 2.2"
    gem "liquid-c", "~> 4.0"
    gem "yajl-ruby", "~> 1.4"
  end

  # Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
  # and associated library
  platforms :jruby, :mswin, :mingw, :x64_mingw do
    gem "tzinfo", "~> 1.2"
    gem "tzinfo-data"
  end
end

#

group :site do
  gem "html-proofer", "~> 3.4" if ENV["PROOF"]

  gem "jekyll-avatar"
  gem "jekyll-mentions"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
  gem "jemoji"
end

gem "webrick"
