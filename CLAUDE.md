# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A single landing page for **PixelForge**, a retro gaming review site. The visual direction is retro-gaming / pixel-game inspired.

There is no build system, package manager, linter, or test suite. Open `index.html` directly in a browser, or serve the directory with `python3 -m http.server`.

## Structure

- `index.html` — the whole page. Currently just an empty `<main>` linking `style.css`.
- `style.css` — the single stylesheet.

## Conventions

- **No third-party libraries or frameworks.** Plain HTML and CSS only. The one external dependency is the Inter font, loaded via the Google Fonts `@import` at the top of `style.css`.
- **Semantic HTML.** Use the tag that fits (`header`, `nav`, `main`, `section`, `article`, `footer`, etc.) and keep the markup clean and shallow.
- **Use classes sparingly.** Prefer styling through element and structural selectors. When a class is needed, give it a semantic name describing what the element *is* (e.g. `.review-card`), not how it looks (e.g. `.red-box`).
- **Colors come from the `:root` variables** in `style.css` (`--color-bg`, `--color-surface`, `--color-surface-raised`, `--color-primary`, `--color-secondary`, `--color-accent`, `--color-success`, `--color-warning`, `--color-danger`, `--color-text`, `--color-text-muted`, `--color-border`). Do not hard-code colors; the theme is dark.
- A global `* { margin: 0; padding: 0 }` reset is in effect, so spacing must be set explicitly.
