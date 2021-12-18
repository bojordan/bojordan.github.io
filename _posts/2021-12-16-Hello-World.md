---
layout: post
title: Hello world
---

I spare moments I've stumbling through getting a quick blogging solution, and - HELLO WORLD - I have one.

GitHub is a wonderful resource, and I already use it. Further, [GitHub Pages](https://docs.github.com/en/pages) is a wonderful *free* resource for all users of GitHub, both free and paid. Add the ability fork someone else's getting-started work (of course this is a core tenent of what GitHub is), is amazing.

## The steps
1. Get a GitHub account, if you don't already have one.
1. Fork [Barry Clark's jekyll-now repo](https://github.com/barryclark/jekyll-now).
1. Rename your fork's repository to `<yourgithubname>.github.io`.
1. Done!

<!--more-->

What you end up with is a static site. This basically means there is no database needed to run things. GitHub provides Jekyll (the code that generates the static pages) as a service. All of my content are [Markdown](https://daringfireball.net/projects/markdown/) text files, which are versioned with Git.

If you are intersted in the same, please check out Barry Clark's extremely helpful repo and explanations:

* <https://github.com/barryclark/jekyll-now>
* <https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/>

## What's next?
* **Private repo**: I don't believe you can take a forked repo private, so may do a tiny amount of work to make this blog's repo private. (Note, I believe GitHub Pages is only supported in private repos wih paid GitHub accounts.) I may prefer the repo to remain public.
* **Style**: I'd like to style things a little. I've already added an excerpt separator to the site's `_config.yml`, but I haven't bothered to look at themes.
* **Custom domain**: I am using a custom domain for this site. Getting this to work was mostly simple, but I had more hiccups than I expected.
* **Run Jekyll locally**: I need to run the site locally.
* **Drafts**: I need a drafts strategy, which is [probably this](http://seanlaw.github.io/2015/03/14/jekyll-drafts/).

## What's long-term?
* **DasBlog Core**: I have no interest in working on the Jekyll back-end of this solution. If I find things are limiting in any way (not likely), I'm interested in looking into a .NET-centric static site-generating solution like [DasBlog Core](https://github.com/poppastring/dasblog-core). [Scott Hanselman has a great post about his implementation.](https://www.hanselman.com/blog/migrating-this-blog-to-azure-its-done-now-the-work-begins)