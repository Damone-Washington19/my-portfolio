Project: My Portfolio (Jekyll / GitHub Pages)
Date: 2026-06-20

Purpose
-------
This document summarizes the repository structure, important Jekyll configuration, current status, and quick restart instructions so this chat session (or another assistant) can resume work quickly.

Repository Info
---------------
- **Repo:** Damone-Washington19/my-portfolio
- **Primary Language:** Jupyter Notebook (89.1%)
- **Other Languages:** HTML (6.2%), CSS (3.7%), Other (1%)
- **Type:** Jekyll-based portfolio + AI/ML projects

Top-level tree (important files and folders)
-------------------------------------------
- `_config.yml` — Jekyll config (site title, `url`, `theme: minima`, `collections: projects`).
- `index.md` — Home page (front matter is correct ✅).
- `_layouts/defaults.html` — Primary layout used by pages; includes header/footer and links CSS/JS.
- `_layouts/project.html` — Individual project page layout (CREATED ✅).
- `_includes/header.html` — Site header / navigation.
- `_includes/footer.html` — Footer.
- `_projects/` — Collection of project markdown files:
  - `mcu-knowledge-graph.md` — MCU relationship graph project
  - `scientific-knowledge-graph.md` — Scientific knowledge graph project
- `assets/css/styles.scss` — Source SASS/CSS.
- `assets/js/main.js` — Site JS.
- `_site/` — Generated site output (not committed, in .gitignore ✅).

Current Status (Updated 2026-06-20)
-----------------------------------
✅ **FIXED:**
- `index.md` front matter is correct (has opening `---`)
- `_layouts/project.html` created and configured
- `_site/` added to `.gitignore` (along with `Gemfile.lock` and `.DS_Store`)
- Stylesheet paths use correct Liquid syntax: `{{ '/assets/css/styles.css' | relative_url }}`

✅ **VERIFIED:**
- Project collection files properly use `layout: project`
- Images referenced correctly with `{{ '/assets/images/NAME' | relative_url }}`
- All Jekyll configuration is valid

Quick local build commands
--------------------------
Install dependencies:

```bash
bundle install
```

Serve locally:

```bash
bundle exec jekyll serve --livereload
```

The site will be available at `http://localhost:4000`

Project Details
---------------
**MCU Knowledge Graph** (`_projects/mcu-knowledge-graph.md`)
- Multi-phase Python system mapping Marvel Cinematic Universe character relationships
- Tech: Python, NetworkX, Matplotlib, BeautifulSoup, Wikipedia API, Requests
- Phases: Web Crawler → Wikipedia Integration → Character Relationship Graph

**Scientific Knowledge Graph** (`_projects/scientific-knowledge-graph.md`)
- Similar knowledge graph architecture for scientific domain

Files to check first when resuming
---------------------------------
- [`_config.yml`](_config.yml) — verify `url`, `baseurl`, theme, and collections.
- [`_layouts/defaults.html`](_layouts/defaults.html) — stylesheet link and includes.
- [`_layouts/project.html`](_layouts/project.html) — project page layout (newly created).
- [`_projects/` folder](_projects/) — all projects using `layout: project`.

How to use this file to restart the chat
---------------------------------------
1. Open this repository in the editor.
2. Open this file: [`PROJECT_STRUCTURE.md`](PROJECT_STRUCTURE.md).
3. In a new chat, paste this file's path and ask the assistant to "resume analysis from PROJECT_STRUCTURE.md" or ask specific questions about the portfolio.

Next Steps
----------
- Test the site locally with `bundle exec jekyll serve --livereload`
- Verify all project pages render correctly
- Consider adding more projects to the `_projects/` collection
- Optionally enhance styling in `assets/css/styles.scss`
