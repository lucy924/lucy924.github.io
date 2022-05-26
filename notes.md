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
- I never got this working in the end.

To use the Not-Pure-Poole theme:
- https://jamstackthemes.dev/theme/not-pure-poole/
- https://github.com/benbalter/jekyll-remote-theme
- ended up copying a lot of the directories/docs from this repo into the corresponding places in my repo
- https://vszhub.github.io/not-pure-poole/2020/09/29/welcome-to-not-pure-poole/#

To rebuild and test locally:
delete Gemfile.lock
`cd [path/to/docs/location]` 
`chruby 3.1.2`
`jekyll build`
`bundle install`
`bundle update`
`bundle exec jekyll serve`

To start testing after computer restart:
`cd [path/to/docs/location]` 
`chruby 3.1.2`
`bundle update`
`bundle exec jekyll serve`

Testing help:
https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll

