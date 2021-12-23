---
layout: post
title: Jekyll is fun
---

So, with some free holiday hours, I've found playing with Jekyll to be more fun than expected. I guess I shouldn't be surprised.

I wanted to do one of two things: Either start competely from scratch with a bare-bones GitHub Pages blog repo, or fork from [Barry Clark's jekyll-now repo](https://github.com/barryclark/jekyll-now). I tried both.

With the bare-bones repo, with *no prior knowledge of Jekyll at all*, it was very straightforward how to get a page to be served, but not how to create a blog of many files, all in a time series.

<!--
With the forked repo, the structure of what Jekyll needs to serve up a blog is present. However, what is required by plug-ins and what is required by the default theme were not completely clear to me (remember, *no prior knowledge of Jekyll at all*). So, trying to change the theme via the GitHub Pages settings panel (which apparently just puts a `theme:` entry into `_config.yml`) doesn't immediately work. Further, if you aren't running Jekyll locally, there is little insight into how things are working when the site is published.
-->

While the forked repo strategy was extremely simple to get started, I did not find it to be tinker-friendly without any knowledge of Jekyll. I can't keep away from tinkering at least a little bit with a theme.

<!--
So, on to reading the [Jekyll themes](https://jekyllrb.com/docs/themes/) documentation. It seems like gem-based themes are what I want, since I want the platform to do as much for me as possible. However, it appears that's what the GitHub Pages settings panel tried to do, with no result in my forked repo.
-->

Eventually, it became apparent to me I should just learn what Jekyll is doing, and it turns out there is a wonderful [Step by Step tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/) on the Jekyll site. There are ten steps, but they are pretty simple, and they each explain the logic of the components of Jekyll. I followed the tutorial on Windows, and pretty much ended up with a complete (albeit unstyled) site, running locally. Grab some existing CSS from a few blogs, and a tiny bit of tinkering later I have something a little closer to what I want.