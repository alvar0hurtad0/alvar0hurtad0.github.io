# alvar0hurtad0 presonal website

Created from https://github.com/wowthemesnet/mediumish-theme-jekyll

## Install
gem install bundler
bundle install
bundle exec jekyll serve --watch

## Create microblog post.
cat templates/microblog > _microblog/$(date +%s).md
