# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static personal portfolio website for Lauren Angela Macalinao, showcasing her work in Data Science and Front-End Development. The site is built with vanilla HTML, CSS, and JavaScript with no build process or dependencies.

## Structure

The project has a simple three-file architecture:

- `index.html` - Single-page application containing all content sections
- `css/style.css` - All styling using CSS custom properties (CSS variables)
- `js/main.js` - Client-side interactivity and animations

## Development

Since this is a static site with no build process:

- Open `index.html` directly in a browser to view the site
- No installation, build, or compilation steps required
- Changes to HTML/CSS/JS are immediately reflected on page refresh

## Architecture & Design Patterns

### CSS Architecture
- Uses CSS custom properties (`:root` variables) for theming in `css/style.css:3-19`
- Color scheme: Deep charcoal backgrounds with sage green accents and gold highlights
- Font stack: 'Outfit' for headings, 'Inter' for body text
- All transitions use a consistent `--transition: all 0.3s ease-in-out` variable

### JavaScript Features (js/main.js)
- **Mobile Navigation**: Hamburger menu toggle for responsive design (lines 5-21)
- **Smooth Scrolling**: Custom anchor link scrolling with 80px offset for fixed navbar (lines 23-45)
- **Scroll Reveal Animations**: Intersection Observer API for on-scroll element reveals (lines 47-66)
  - Elements get `.hidden` class initially, then `.revealed` when scrolling into view
  - Animates section titles, text blocks, skills, timeline items, projects, and gallery items

### HTML Structure
The page follows a single-page application pattern with these sections:
1. Fixed navbar with smooth-scroll navigation
2. Hero section with CTA buttons
3. About section with education details
4. Skills section (3 categories: Technical, Data Science, Design & Other)
5. Experience timeline (2 positions)
6. Projects grid (3 projects with placeholder gradients)
7. Interests section with travel animation (globe + orbiting plane)
8. Contact section with form and social links
9. Footer

### Key Implementation Details
- **Fixed Navbar**: Positioned at top with `backdrop-filter: blur(10px)` for glassmorphism effect
- **Responsive Design**: Hamburger menu for mobile (CSS media queries handle visibility)
- **Travel Animation**: CSS-animated globe with orbiting plane icon in interests section
- **Project Cards**: Use inline gradient backgrounds as placeholders for project images
- **Form**: Contact form present but has no backend handler (submit functionality not implemented)

## Common Modifications

### Updating Content
- Portfolio sections are in `index.html` with semantic section IDs (#about, #skills, #projects, etc.)
- Social links are placeholder `#` anchors in contact section (index.html:265-268)
- Contact form has no action handler - submissions are not processed

### Styling Changes
- Modify color scheme by updating CSS variables in `css/style.css:3-19`
- Section spacing controlled by `.section` class padding (css/style.css:90-92)

### Adding Interactivity
- Extend `js/main.js` DOMContentLoaded handler for new features
- Intersection Observer pattern already set up for scroll animations (js/main.js:47-66)

## External Dependencies

- Font Awesome 6.4.0 (CDN) for icons
- Google Fonts: Inter and Outfit font families

## Notes

- The site includes a resume PDF: `Macalinao_LaurenAngela_Resume.pdf`
- There's a typo in the skills section: "Coogle Colab" should be "Google Colab" (index.html:94)
- Project card links and social media links are placeholders pointing to `#`
