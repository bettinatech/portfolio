# Bettina's Portfolio

A responsive, botanical, book-style data analytics portfolio with a bilingual profile, two SQL/Power BI dashboard projects, an HR Analytics gallery, completed courses and contact links.

## Technologies

HTML, CSS, vanilla JavaScript and SVG. Images are embedded as data URLs in `index.html`; no image files are missing. DM Sans is loaded from Google Fonts, with local font fallbacks. Dashboard galleries display screenshots, not a live Power BI service connection.

## Install

Use Node.js 18 or newer and npm:

```sh
npm ci
```

There are no third-party npm dependencies.

## Develop / run

```sh
npm run dev
```

Open http://127.0.0.1:3000. Edit `index.html` directly and refresh the browser. The development server is local-only. Alternatively, any static web server can serve this folder.

## Validate / build

```sh
npm run check
npm run build
```

This is a source-first static site: no compilation or generated dist/build directory is needed. The build command validates the existing source. Checks cover inline JavaScript syntax, unique HTML IDs, required sections, local-path references and common secret signatures. They do not replace visual/browser testing or a complete security audit.

## Structure

```text
index.html          Complete editable site: markup, CSS, JavaScript, embedded images
scripts/serve.cjs   Local development server using Node built-ins
scripts/validate.cjs Source validation using Node built-ins
package.json        Development and validation commands
package-lock.json   Dependency lockfile (no third-party packages)
.nojekyll           GitHub Pages static hosting marker
.gitignore         Local/dependency/secret exclusions
README.md           This guide
```

## GitHub Pages

Upload these files to the repository root. In Settings → Pages select “Deploy from a branch”, your main branch and the root folder. No server runtime or credentials are required on GitHub Pages. The local Node server is only a development convenience.

## Editing and behavior

The project galleries and botanical artwork are embedded in `index.html`; preserve the data URLs when editing. Desktop shows book spreads, while mobile shows separate project leaves. Long HR text uses internal scrolling so the compact mobile page and bottom navigation stay fixed. English and Hungarian HR leaves belong to one project, not duplicate projects.

The public LinkedIn/GitHub links and contact email are intentional portfolio content. Do not add credentials, raw databases, .env files or confidential data to the repository. Screenshots should only show information intended for public display.
