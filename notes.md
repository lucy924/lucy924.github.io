install ruby following these instructions: https://stackoverflow.com/a/54873916
- brew install chruby ruby-install
- ruby-install ruby
    - Successfully installed ruby 3.1.2 into /Users/lucy/.rubies/ruby-3.1.2
- when you want to use ruby: 
    - chruby 3.1.2

To use the Architect theme:
https://stackoverflow.com/questions/44010385/jekyll-architect-theme-not-working-on-github-page
- deleted Gemfile.lock to use updated bundler
- bundle update
- bundle install (creates a new Gemfile.lock)

To use the Not-Pure-Poole theme:
- https://jamstackthemes.dev/theme/not-pure-poole/
- https://github.com/benbalter/jekyll-remote-theme
- ended up copying a lot of the directories/docs from this repo into the corresponding places in my repo

To rebuild and test locally:
delete Gemfile.lock
run `jekyll build`
run `bundle install`
run `bundle exec jekyll serve`
