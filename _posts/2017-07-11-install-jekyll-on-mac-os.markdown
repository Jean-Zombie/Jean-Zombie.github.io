---
layout: post
title: "setup a blog on github with Jekyll (mac os sierra)"
date: "2017-07-11 11:43:34 +0200"
---

What could be a better topic for a first blogpost then a how-to about setting up the blog itself? I read a lot about the combination of github (hosting) and Jekyll (serving) for a personal blog. But it wasn't as easy as it first seemed. I started off with this [tutorial](http://www.abstractclass.org/tutorial/blog/2015/05/19/tutorial-personal-blog-with-github.html) which covers the basics of setting up a github repo designated for blogging.

Problems began when I tried using Jekyll. Jekyll needs a Ruby version higher then 2.1 but my built-in ruby is only 2.0. Homebrew to the rescue.

* Install Ruby with homebrew: https://goo.gl/rXYZsT
* Install Jekyll: `sudo gem install Jekyll`

Problems didn't stop here though. I wanted to use [Hyde](https://goo.gl/XQRkY7) as a theme which has some dependencies that weren't met. Also it's config file was outdated. Solutions:

In the *_config.yml*:
* change "gem" to "plugins"
* add "[jekyll-paginate, jekyll-gist]" as plugins
* comment out "relative_permalinks" or set it to "false"
* add "paginate_path: 'page:num'"
* remove the whole "markdown" line
* change "highlighter" value to "rouge", since github doesn't use "pygments"


You probably also need to install said plugins:
* gem install jekyll-paginate
* gem install jekyll-gist

Then head over to the location of your local git repo and fire up the server with `jekyll serve`. Did it for me.
