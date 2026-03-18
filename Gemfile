# frozen_string_literal: true

source "https://rubygems.org"

# This gem ensures your local environment matches GitHub Pages exactly
gem "github-pages", group: :jekyll_plugins

# Windows and JRuby support
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Keep this if you have a .gemspec file in your folder
gemspec
