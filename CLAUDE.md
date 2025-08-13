# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal website built with Hugo static site generator using the Anatole theme. It's a minimalist two-column Hugo theme that showcases personal projects, writing, and other content.

## Technology Stack

- **Static Site Generator**: Hugo
- **Theme**: Anatole (https://github.com/lxndrblz/anatole.git) - installed as git submodule
- **Configuration**: TOML format in config.toml
- **Content**: Markdown files in content/ directory
- **Deployment**: Static files generated to public/ directory

## Common Development Commands

### Hugo Commands (from root directory)
- `hugo serve` - Start development server (default: http://localhost:1313)
- `hugo serve -D` - Start development server including draft content
- `hugo` - Build static site to public/ directory
- `hugo --buildDrafts` - Build including draft content

### Theme Development (from themes/anatole/)
- `npm run dev` - Development server for theme
- `npm run build` - Build theme resources
- `npm run prettier` - Format code with Prettier

## Site Structure

### Content Organization
- `content/about/` - About page content
- `content/projects/` - Project pages and listing
- `content/writing/` - Writing/blog content
- `content/other/` - Additional content section

### Key Configuration Files
- `config.toml` - Main Hugo configuration with menu, params, and social icons
- `layouts/index.html` - Custom homepage layout with project display
- `static/` - Static assets (images, videos, favicons)

### Theme Integration
- Theme installed as git submodule in `themes/anatole/`
- Custom layouts in `layouts/` directory override theme defaults
- Homepage uses custom layout to display projects from content/projects/

## Development Notes

### Content Creation
- New content files should include Hugo front matter (title, date, draft status)
- Projects support `external_url` parameter for linking to external resources
- The homepage automatically displays all content from the projects section

### Styling
- Custom CSS is embedded in layouts/index.html for homepage styling
- Theme supports dark/light mode with CSS custom properties
- Responsive design with mobile breakpoints

### Menu Configuration
Navigation menu is defined in config.toml with weighted ordering:
1. Projects (home page)
2. Writing
3. About  
4. Other