# Frank Jamison — 2015 Portfolio Site (Static)

This repository contains a static portfolio website built with plain HTML, CSS, and JavaScript.

- **Entry point:** `index.html`
- **Assets:** `css/`, `js/`, `images/`, `fonts/`
- **No build step required:** open locally or serve as static files

## What’s in this project

- A single-page (or single entry) portfolio layout driven by `index.html`
- Styling composed of a main stylesheet plus theme color variants
- Front-end behavior powered by jQuery and Bootstrap

## Project structure

- `index.html` — Main page markup and section layout.
- `css/`
  - `style.css` — Primary site styling.
  - `bootstrap.min.css` — Bootstrap CSS.
  - `font-awesome.min.css`, `linecons.css` — Icon/font styles.
  - `normalize.css` — Cross-browser normalization.
  - `colors/` — Alternate color themes (for example `blue.css`, `green.css`, etc.).
- `js/`
  - `jquery.min.js` — jQuery runtime.
  - `bootstrap.min.js` — Bootstrap JS.
  - `main.js`, `layout.js`, `default.js`, `watch.js` — Site-specific scripts.
- `images/` — Images used by the site.
  - `portfolio/` — Portfolio images/assets.
  - `team/` — Team-related images/assets.
  - `gmaps/` — Map-related assets (if used by the page).
- `fonts/` — Icon font files and related assets.
- `Frank Jamison.vcf` — vCard contact file.

## Getting started (local)

Because this is a static site, you can use any static file server. Serving files (rather than opening `index.html` directly) is recommended to avoid browser restrictions around local file access.

### Option A: Python (simple)

From the project folder:

- Python 3:
  - `python -m http.server 8000`

Then open:

- `http://127.0.0.1:8000/`

### Option B: Node.js `serve`

If you have Node.js installed:

- `npx serve .`

It will print the URL it’s serving on.

### Option C: VS Code Live Server

If you use VS Code, the “Live Server” extension is a convenient way to preview static sites.

## Editing content

Most content changes happen in `index.html`.

Common edits:

- **Text / sections:** Update headings, paragraphs, and lists in `index.html`.
- **Images:** Place new images under `images/` (often `images/portfolio/`) and update the corresponding `<img>` `src` attributes.
- **Contact / vCard:** Update `Frank Jamison.vcf` if contact details change.

## Styling and themes

### Main styling

- Primary styling lives in `css/style.css`.

### Color themes

- Theme color styles are in `css/colors/`.
- If the page links to a specific color file (for example `css/colors/blue.css`), switching themes usually means changing that linked stylesheet in `index.html`.

## JavaScript behavior

Scripts are in `js/`. In general:

- `jquery.min.js` and `bootstrap.min.js` provide the baseline library behavior.
- `main.js`, `layout.js`, `default.js`, and `watch.js` contain site-specific interactions.

If you change script loading order, keep jQuery loaded before scripts that depend on it.

## Deployment

This site can be deployed to any static hosting provider:

- Traditional web hosting (upload the folder contents)
- Static hosting platforms (drag-and-drop or Git-based deployments)
- A web server (IIS/Apache/Nginx) configured to serve `index.html` as the default document

Deployment checklist:

- Ensure `index.html` is at the site root.
- Keep relative paths intact (`css/`, `js/`, `images/`, `fonts/`).
- Verify images and fonts load correctly after deployment.

## Browser support

The site uses common front-end libraries and should work in modern browsers. If you need to support older browsers, test thoroughly—especially around CSS features and any JavaScript-driven layout behavior.