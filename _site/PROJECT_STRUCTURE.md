Project: My Portfolio (Jekyll / GitHub Pages)
Date: 2026-06-18

Purpose
-------
This document summarizes the repository structure, important Jekyll configuration, known issues, and quick restart instructions so this chat session (or another assistant) can resume work quickly.

Top-level tree (important files and folders)
-------------------------------------------
- `_config.yml` — Jekyll config (site title, `url`, `theme: minima`, `collections: projects`).
- `index.md` — Home page (has malformed front matter; missing leading `---`).
- `_layouts/defaults.html` — Primary layout used by pages; includes header/footer and links CSS/JS.
- `_includes/header.html` — Site header / navigation.
- `_includes/footer.html` — Footer.
- `_projects/` — Collection of project markdown files (e.g., `example-project.md`) with `layout: project`.
- `assets/css/styles.scss` — Source SASS/CSS.
- `assets/js/main.js` — Site JS.
- `_site/` — Generated site output (built site). Usually not committed.

Notes & Known Issues
--------------------
- `index.md` currently renders the front matter as content because the opening `---` is missing. Fix: add `---` as the first line.
- There is no `_layouts/project.html` while project items request `layout: project`. Either add `_layouts/project.html` or change project files to `layout: defaults`/`default`.
- Stylesheet path inconsistency: `_layouts/defaults.html` links `/assets/css/styles.css` but the built page references `/assets/main.css`. Use the compiled path consistently and prefer Liquid: `{{ '/assets/main.css' | relative_url }}`.
- Images should be placed under `assets/images/` and referenced via `{{ '/assets/images/NAME' | relative_url }}`.
- `_site/` is present: consider adding `_site/` to `.gitignore` and not committing generated files to source repo.

Quick local build commands
--------------------------
Install dependencies (already run in this workspace):

```bash
bundle install
```

Serve locally:

```bash
bundle exec jekyll serve --livereload
```

Files to check first when resuming
---------------------------------
- [`_config.yml`]( _config.yml ) — verify `url`, `baseurl`, theme, and collections.
- [`index.md`]( index.md ) — fix front matter.
- [`_layouts/defaults.html`]( _layouts/defaults.html ) — update stylesheet link and ensure includes are correct.
- [`_projects/` folder]( _projects/ ) — ensure `layout: project` matches a real layout.

How to use this file to restart the chat
---------------------------------------
1. Open this repository in the editor.
2. Open this file: [`PROJECT_STRUCTURE.md`]( PROJECT_STRUCTURE.md ).
3. In a new chat, paste this file's path and ask the assistant to "resume analysis from PROJECT_STRUCTURE.md" or "continue fixing index front matter and add project layout" — the assistant can pick up the exact next steps listed in "Files to check first".

If you want, I can now apply the three quick fixes mentioned above (fix `index.md` front matter, add a minimal `_layouts/project.html`, and update the stylesheet link). Reply with `apply fixes` to proceed.
