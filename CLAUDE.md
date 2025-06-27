# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a Jekyll-based personal blog using the Tale theme, hosted on GitHub Pages. The blog is primarily written in Korean and focuses on mobile marketing, technology, and personal thoughts.

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install

# Run the site locally with live reload
jekyll serve --watch
# or
bundle exec jekyll serve --watch

# Access at http://localhost:4000
```

### Build Commands
```bash
# Build the site for production
jekyll build
# or
bundle exec jekyll build
```

## Architecture

### Site Structure
- **_posts/**: Blog posts in Markdown format with YAML front matter
- **_layouts/**: HTML templates (default.html, post.html, page.html)
- **_includes/**: Reusable HTML components (head.html, analytics.html)
- **_sass/**: SCSS stylesheets for theming
- **css/**: Compiled CSS and external libraries
- **js/**: JavaScript files including jQuery and Bigfoot footnotes
- **images/**: Static assets and blog post images

### Key Configuration
- Site configuration in `_config.yml`
- Uses Jekyll pagination (15 posts per page)
- Permalink structure: `/:year-:month-:day/:title`
- SASS compilation with compressed output

### Blog Features
- Korean language navigation and content
- Responsive design with Tale theme
- Syntax highlighting with Pygments
- Footnotes support via Bigfoot.js
- Facebook integration
- Google Analytics (production only)
- RSS feed via jekyll-feed plugin

### Content Guidelines
- Blog posts use Korean titles and content
- Post filenames follow format: `YYYY-MM-DD-title.md`
- Posts require YAML front matter with layout, title, and date
- Images stored in `/images/` directory

### Development Notes
- Ruby-based Jekyll site with Bundler for dependency management
- GitHub Pages compatible configuration
- Uses Jekyll 4.3.2 with required plugins for sitemap, feed, and pagination
- Production analytics only activated via `jekyll.environment == 'production'`