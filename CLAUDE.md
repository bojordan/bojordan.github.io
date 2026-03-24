# Claude Code Instructions

## Project Overview

Personal blog and project site built with Jekyll, hosted on GitHub Pages.

## Local Development

```sh
# Start server (kills any existing Jekyll process first)
kill $(pgrep -f jekyll) 2>/dev/null; /opt/homebrew/opt/ruby/bin/bundle exec jekyll serve --detach
```

Site available at http://127.0.0.1:4000. Auto-regeneration is disabled in detached mode — restart the server after making changes.

## Key Conventions

- **Layouts**: `_layouts/default.html` is the base layout. `_layouts/spectrum.html` extends it for the spectrum analyzer tutorial. `_layouts/tutorial.html` extends it for the Minecraft tutorial.
- **Theming**: The site supports dark/light modes via CSS custom properties defined in `_sass/main.scss` (`:root` for light, `[data-theme="dark"]` for dark). All colors should use `var(--...)` tokens, not hardcoded hex values.
- **Spectrum tutorial**: Lives at `projects/spectrum-analyzer/tutorial/`. This is the **canonical source** for all tutorial content — the standalone HTML version in `~/src/claude-experiments/tutorial/` is archived and should not be edited.

## Related Repository

The spectrum analyzer app code lives in `~/src/claude-experiments/VUMeter/`. See that repo's CLAUDE.md for details. When working on the tutorial, you may need to reference the app source code there.
