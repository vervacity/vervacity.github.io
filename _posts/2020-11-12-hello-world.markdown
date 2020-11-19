---
layout: post
title:  "hello world"
date:   2020-11-12 20:06:46 -0800
categories: tutorial
excerpt_separator: <!--more-->
---

Today let's talk about how to set up a github-pages website. I did not find it as straightforward as I might have hoped, so am leaving my notes here in case it helps someone else down the line.

# setup

The following instructions are intended for a MacOS user who wants to build a github pages based website but also run locally to test before pushing to github pages.

Starting install docs of use:

- Jekyll and Github pages instructions [here](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll)
- Jekyll install instructions [here](https://jekyllrb.com/docs/installation/)
- Follow macOS version instructions [here](https://jekyllrb.com/docs/installation/macos/)

# installing ruby/jekyll

Notes on installing ruby:

- Jekyll will require `ruby >= 2.5`
- I installed with `homebrew` first, but then used `rbenv` for the final working set up locally. Unsure if you need both or not, but would recommend definitely using `rbenv` setup.

Notes on installing gems

- Follow the jekyll install instructions for user install.
- Note that your ruby version may be slightly different from the gem ruby version folder. Ie, ruby verion can be `2.7.1` while the folder will be `2.7.0`.

My final bash profile was modified with the following:

```
export PATH="/usr/local/opt/ruby/bin:$PATH"
export PATH="$HOME/.gem/ruby/2.7.0/bin:$PATH"
export GEM_HOME=$HOME/gems
export PATH=$HOME/gems/bin:$PATH

eval "$(rbenv init -)"
```

# setting up for github-pages

First, build a github repo as described in the jekyll/github-pages instructions. Then, run `jekyll new .` in the root folder. Voila, a jekyll website!

# testing locally

To run locally, directions [here](https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/testing-your-github-pages-site-locally-with-jekyll), run `bundle exec jekyll serve` to get it running on your local computer. Of note, the Gemfile says you want to uncomment the github-pages line in the Gemfile to make it work with github-pages, but I didn't do that and it seems to be running fine online...

# themes

Next to play with: themes. Github pages supports [these themes](https://pages.github.com/themes/) Most of them do not look great, I think I'll be looking to customize another way.

--

*How 'accurate' is this post: 7/10. How 'precise' is this post: 3/10.*
