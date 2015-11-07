source 'https://rubygems.org'

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem 'github-pages', versions['github-pages']

gem 'octopress', '~> 3.0.0.rc.12'
gem 'rouge'

group :development do
  gem 'guard-jekyll-plus'
  gem 'guard-livereload'
  gem 'guard-bundler', require: false
end

