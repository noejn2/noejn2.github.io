# Copilot Instructions for noejn2.github.io

## Project Overview

This is a **Jekyll-based personal academic website** using a customized `plainwhite` theme. It serves as a portfolio for an economist, showcasing research projects, working papers, and professional information.

## Architecture

### Content Structure
- **`index.md`** — Homepage with "About me" content using `layout: home`
- **`project-descriptions/`** — Research project pages (Markdown with `layout: page`)
- **`blog/blog.md`** — Working papers page listing academic research
- **`_posts/`** — Blog posts (date-prefixed Markdown, `layout: post`)
- **`project-assets/`** — PDFs and assets linked from project descriptions
- **`cv/`** — LaTeX CV source files (PDF served at `/cv/cv_nava.pdf`)

### Layout Hierarchy
```
default.html  ← Base layout with sidebar navigation
├── home.html   ← For index.md (About page)
├── page.html   ← For standalone pages (project descriptions)
└── post.html   ← For blog posts with date/categories
```

### Configuration
- **`_config.yml`** — Site metadata, navigation links, social links, and theme settings
- Navigation is defined under `plainwhite.navigation[]` — each entry needs `title` and `url`

## Key Conventions

### Adding New Content

**New project description:**
```markdown
---
layout: page
title: "Project Title"
---
# Content here...
```
Place in `project-descriptions/` and add navigation link in `_config.yml`.

**New blog post:**
```markdown
---
layout: post
title: "Post Title"
categories: [category1, category2]
---
```
Name file as `YYYY-MM-DD-slug.markdown` in `_posts/`.

### Styling
- SCSS in `_sass/plain.scss` — imports from `_sass/ext/` (fonts, normalize)
- Variables: `$linkColor`, `$mobileW` (768px), `$smallMobileW` (480px)
- Fonts: Raleway (body), Merriweather (headings) via Google Fonts

### Navigation Pattern
Navigation links in `_config.yml` can be:
- Internal pages: `/project-descriptions/gravityGE`
- External URLs: `https://noejnava2.shinyapps.io/...`
- PDF files: `/cv/cv_nava.pdf`
- Spacers: use `title: " "` with `url: "#"`

## Development Workflow

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

Site builds to `_site/` (gitignored). Deployed via GitHub Pages.

## Important Notes

- The theme is a local gem (`plainwhite.gemspec`) — not installed from RubyGems
- Social icons use Fontello (`assets/font/fontello-config.json`)
- SEO handled by `jekyll-seo-tag` plugin — set metadata in front matter
- Profile image: `assets/jm_cropped.jpg`
