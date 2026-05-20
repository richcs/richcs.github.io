# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Deployment

This is a GitHub Pages site — pushing to `main` deploys automatically to `https://richcs.github.io`. There is no build step, bundler, or package manager. Edit files and push.

## Architecture

Three files, no dependencies:

- **`index.html`** — single-page layout with sections: `#hero`, `#about`, `#projects`, `#skills`, `#contact`. All content is hard-coded here.
- **`style.css`** — all styling. Uses CSS custom properties defined in `:root` for the color palette (dark theme, `--accent`/`--accent-2` are the purple brand colors). The `.fade-in` / `.fade-in.visible` pair is driven by JS.
- **`main.js`** — two behaviours: navbar scroll-shadow via `.scrolled` class, and `IntersectionObserver` fade-ins on cards and sections.

## Updating content

- **Projects** — add or edit `.project-card` blocks in `index.html`. The `.featured` modifier adds a purple tint and is used for the top project.
- **Skills** — edit the `.skill-group` lists in the skills section. Language dot colors (`.lang-dot.<name>`) are defined in `style.css`.
- **Colors / theme** — all tokens are CSS variables in `:root`; change there to retheme globally.
