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
_drafts/              # Unpublished post drafts
_layouts/             # HTML layout templates
_posts/               # Published blog posts
_sass/                # Sass stylesheets
assets/               # CSS, images, and other static files
assets_unpublished/   # Font files and other assets tracked in git but excluded from the site build
projects/             # Project pages
```

## Fonts

The site uses [Berkeley Mono](https://berkeleygraphics.com/typefaces/berkeley-mono/) by U.S. Graphics Company as its monospace typeface for the site title, code blocks, and other monospace elements. The Regular weight is self-hosted as a web font from `assets/fonts/`. The full font family (all 20 weights) is stored in `assets_unpublished/fonts/` — see [assets_unpublished/fonts/README.txt](assets_unpublished/fonts/README.txt) for license and build details.

## Deployment

Push to `main` — GitHub Pages builds and deploys automatically.
