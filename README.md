# bojordan.github.io

Personal site built with [Jekyll](https://jekyllrb.com/) and hosted on GitHub Pages.

## Prerequisites

- Ruby (installed via Homebrew: `/opt/homebrew/opt/ruby/bin/ruby`)
- Bundler (`gem install bundler`)

## Setup

Install dependencies:

```sh
/opt/homebrew/opt/ruby/bin/bundle install
```

## Local development

Start the local server:

```sh
kill $(pgrep -f jekyll); /opt/homebrew/opt/ruby/bin/bundle exec jekyll serve --detach
```

I prefer to run it in watch mode:
```sh
/opt/homebrew/opt/ruby/bin/bundle exec jekyll serve --detach
```

This kills any existing Jekyll process and starts a new one in the background. The site will be available at http://127.0.0.1:4000.

To stop the server:

```sh
pkill -f jekyll
```

## Project structure

```
_drafts/     # Unpublished post drafts
_layouts/    # HTML layout templates
_posts/      # Published blog posts
_sass/       # Sass stylesheets
assets/      # CSS, images, and other static files
projects/    # Project pages
```

## Deployment

Push to `main` — GitHub Pages builds and deploys automatically.
