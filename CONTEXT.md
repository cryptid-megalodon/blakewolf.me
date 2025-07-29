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

## Current Status
- The home page and about page have been customized with Blake's professional information
- Both pages use the same content and portrait image
- Demo blog posts and projects are still present
- Contact form is configured but form action is empty
- Pagination has been removed from the site

## Future Considerations
- Add link to substack for blog posts.
- Remove or replace demo blog posts and projects with real content
- Configure contact form with proper form handler
- Add real projects to showcase
- Consider differentiating home and about pages or removing redundancy
- Consider adding recent blog posts about machine learning journey
- Fix deprecated Sass warnings in theme stylesheets (optional)