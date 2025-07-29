# Blake Wolf Professional Landing Page - Project Context

## Overview
This is Blake Wolf's professional landing page hosted at https://blakewolf.me. The website serves as a personal portfolio and professional presence online.

## Technical Stack
- **Framework**: Jekyll static site generator (v4.3.4)
- **Ruby Version**: 3.2.3
- **Theme**: Journal (from Jekyll Themes)
- **Hosting**: GitHub Pages
- **Domain**: blakewolf.me

## Site Owner Information
- **Name**: Blake Wolf
- **Email**: blake@blakewolf.me
- **GitHub**: https://github.com/cryptid-megalodon
- **LinkedIn**: https://www.linkedin.com/in/blake-w-192382222/
- **Portrait Image**: `/images/blake_bw2.webp`

## Professional Background
- Former Senior Software Engineer at Google
- Led the YouTube Music Event Tickets Team
- Worked on data center infrastructure and TensorFlow model analysis tools
- Co-founded a solar farm development company
- Currently focused on machine learning through self-study and personal projects

## Site Structure
- `/` - Home/landing page with about content (index.md)
- `/projects/` - Portfolio/projects showcase
- `/contact` - Contact form page
- `/blog/` - Blog posts section (pagination enabled)

## Key Files
- `_config.yml` - Main Jekyll configuration
- `_data/settings.yml` - Site settings (colors, fonts, menus, social links)
- `index.md` - Home page with Blake's professional information
- `_pages/` - Static pages (about.md, contact.md, thanks.md)
- `_posts/` - Blog posts (currently has demo content)
- `_projects/` - Project portfolio items (currently has demo content)
- `_layouts/page.html` - Page layout template (fixed to use {{ content }} instead of {{ page.content }})

## Recent Changes
- Upgraded Jekyll from 3.8.5 to 4.3.4 for Ruby 3.2 compatibility
- Renamed index.html to index.md to enable Markdown processing
- Fixed page layout template to properly render Markdown content
- Updated about page and home page with Blake's portrait image
- Both home and about pages now display identical professional content
- Menu updated to show "About" instead of "Latest" for the home page
- Removed pagination configuration and jekyll-paginate plugin
- Contact page replaced form with direct contact links (email, GitHub, LinkedIn)
- Removed unused contact form dependencies (includes, CSS, JavaScript, settings)
- Fixed critical Sass deprecation warnings (color functions and math operations)
- Added Substack link to navigation menu and social icons

## Current Status
- The home page and about page have been customized with Blake's professional information
- Both pages use the same content and portrait image
- Demo blog posts and projects have been removed
- Automated GitHub projects system implemented with daily updates
- Projects page automatically displays GitHub repos with About sections
- Contact page has been updated to display email, GitHub, and LinkedIn links (no form)
- Pagination has been removed from the site
- Critical Sass deprecation warnings have been resolved (color functions, math operations)
- Remaining @import deprecation warnings are intentionally left in place for Jekyll theme compatibility
- Substack blog link added to main navigation and social icons (https://cryptidmegalodon1.substack.com/)

## Automated Projects System
- **GitHub Actions Workflow**: `.github/workflows/update-projects.yml` runs daily at 6 AM UTC
- **Data Source**: Fetches all public repos from cryptid-megalodon GitHub account
- **Filtering**: Only includes repositories with populated About/description sections
- **Output**: Creates `_data/github_projects.yml` with alphabetized project list
- **Display**: `/projects/` page automatically renders bulleted list with repo names, descriptions, and GitHub links
- **Manual Trigger**: Workflow can be manually triggered via GitHub Actions interface

## Future Considerations
- Consider adding solar farm project as a manual entry since it may not have a GitHub repo
- Consider differentiating home and about pages or removing redundancy
- Consider adding recent blog posts about machine learning journey

## Technical Notes

### Sass Deprecation Warnings
**Fixed (Critical):**
- Replaced `adjust-hue()` with `color.adjust()` using proper `$hue: 15deg` syntax
- Replaced slash division (`/`) with `math.div()` function
- Added `@use "sass:color"` and `@use "sass:math"` modules

**Remaining (@import warnings):**
The remaining 12 @import deprecation warnings are intentionally left in place because:
- Jekyll themes with templating variables require global variable scoping
- Converting to @use would break variable access across partials due to different scoping rules
- These are deprecation warnings (not errors) that won't break functionality until Dart Sass 3.0.0
- Theme compatibility and stability take priority over eliminating non-critical warnings