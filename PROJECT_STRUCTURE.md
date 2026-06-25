Project: Damone Washington Portfolio (Jekyll / GitHub Pages)
Date: 2026-06-25

Purpose
-------
This document summarizes the current repository structure, Jekyll configuration, layout system, and restart instructions for future portfolio development.

Current Site Architecture
-------------------------
- `_config.yml` - Jekyll config using `theme: jekyll-theme-tactile`, explicit SEO/sitemap plugins, and the `projects` collection.
- `index.md` - Main landing page with valid front matter, hero section, skills grid, featured projects, and contact section.
- `about.md` - About page with education, research, coursework, and internship goals.
- `projects.md` - Projects index page available at `/projects/`.
- `_projects/` - Project collection items using `layout: project`.
- `_layouts/default.html` - Main Tactile-compatible site shell. It keeps the Tactile container/header/content structure and delegates shared header/footer markup to includes.
- `_layouts/project.html` - Individual project page layout.
- `_includes/header.html` - Shared site title, description, and primary navigation buttons.
- `_includes/footer.html` - Shared footer.
- `assets/css/styles.scss` - Custom CSS overrides layered on top of the Tactile theme stylesheet.
- `assets/js/main.js` - Reserved for future interaction scripts.
- `assets/images/` - Profile images used by the homepage.
- `.github/workflows/deploy.yml` - GitHub Pages build and deploy workflow.
- `_site/` - Generated site output. It is ignored by git and should not be edited directly.

Portfolio Content Focus
-----------------------
- Target roles: software engineering internships, entry-level full-stack web development, and data operations.
- Core areas: data structures, AI/ML system security, backend utility automation, REST API integrations, graph theory, NLP, semantic embeddings, and computer vision security.
- Highlighted work: MCU knowledge graph tooling, scientific concept knowledge graph visualization, and adversarial AI defense research.

Local Development
-----------------
Install dependencies:

```bash
bundle install
```

Serve locally:

```bash
bundle exec jekyll serve --livereload
```

Build locally:

```bash
bundle exec jekyll build
```

Notes
-----
- The `/projects/` route is backed by `projects.md`; individual project pages are generated from `_projects/`.
- Keep navigation links in `_includes/header.html` so the layout stays maintainable.
- Keep theme-level structure in `_layouts/default.html`; add portfolio-specific visual changes in `assets/css/styles.scss`.
- The old misplaced workflow path `.github/-/workflows/deploy.yml` has been removed. GitHub recognizes workflows under `.github/workflows/`.
- If local builds fail with a missing `github-pages` gem, run `bundle install` before serving or building.
