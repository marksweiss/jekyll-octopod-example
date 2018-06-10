source "https://rubygems.org"

# Hello! This is where you manage which Jekyll version is used to run.
# When you want to use a different version, change it below, save the
# file and run `bundle install`. Run Jekyll with `bundle exec`, like so:
#
#     bundle exec jekyll serve
#
# Fork of jekyll 3.7.3 that suppresses a build warning caused by pages having a 'post_type'
# property. This properyt is used by feed.xml to support creating separate podcast and blog
# RSS feeds. It is also available to any template to support conditional rendering logic.
# NOTE: jekyll 3.7.3 is the correct version to run with jekyll-octopod, and this fork is
# 3.7.3 with the sole change being a conditionl check to suppress logging of a deprecation message
# when the 'post_type' attribute is detected in a Jekyll::Document type.
gem "jekyll", :git => "https://github.com/marksweiss/jekyll.git", :branch => "3.7-stable_support_podcast_and_blog_feeds"

# This is the default theme for new Jekyll sites. You may change this to anything you like.
gem "jekyll-theme-hydejack", "~> 7.5"
gem "jekyll-theme-awesome"
gem "minima", "~> 2.0"

# If you want to use GitHub Pages, remove the "gem "jekyll"" above and
# uncomment the line below. To upgrade, run `bundle update github-pages`.
# gem "github-pages", group: :jekyll_plugins

# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.6"
end

# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.0" if Gem.win_platform?

# Fork of jekyll-octopod 0.9.4 that supports separate blog and podcast feeds
gem "jekyll-octopod", :git => "https://github.com/marksweiss/jekyll-octopod.git", :branch => "support_podcast_and_blog_feeds"
gem "jekyll-serve"
