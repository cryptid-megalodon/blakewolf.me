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
- `/projects/` - Automatically generated project portfolio from GitHub repos.
- `/contact` - Contact page with direct links (no form)
- `/blog/` - Link out to Substack blog (https://cryptidmegalodon1.substack.com/)

## Key Files
- `_config.yml` - Main Jekyll configuration
- `_data/settings.yml` - Site settings (colors, fonts, menus, social links)
- `index.md` - Home page with Blake's professional information
- `_pages/` - Static pages (projects.md, contact.md)
- `_layouts/page.html` - Page layout template

## Current Status
- Automated GitHub projects system implemented with daily updates
- Projects page automatically displays GitHub repos with About sections
- Contact page has been updated to display email, GitHub, and LinkedIn links
- Pagination has been removed from the site
- Substack blog link added to main navigation and social icons (https://cryptidmegalodon1.substack.com/)

## Automated Projects System
- **GitHub Actions Workflow**: `.github/workflows/update-projects.yml` runs daily at 6 AM UTC
- **Data Source**: Fetches all public repos from cryptid-megalodon GitHub account via GitHub API
- **Filtering**: Only includes repositories with populated About/description sections
- **Output**: Creates `_data/github_projects.yml` with alphabetized project list
- **Display**: `/projects/` page automatically renders bulleted list with repo names, descriptions, and GitHub links
- **Manual Trigger**: Workflow can be manually triggered via GitHub Actions web interface at https://github.com/cryptid-megalodon/blakewolf.me/actions
- **Status**: Workflow committed and deployed, ready for manual or scheduled execution
- **Testing**: GitHub API connectivity verified, workflow logic confirmed functional

## Future Considerations
- Consider adding solar farm project as a manual entry since it may not have a GitHub repo

## Technical Notes

### Sass Deprecation Warnings
**Remaining (@import warnings):**
The remaining 12 @import deprecation warnings are intentionally left in place because:
- Jekyll themes with templating variables require global variable scoping
- Converting to @use would break variable access across partials due to different scoping rules
- These are deprecation warnings (not errors) that won't break functionality until Dart Sass 3.0.0
- Theme compatibility and stability take priority over eliminating non-critical warnings