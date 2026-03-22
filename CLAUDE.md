# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **single-file static portfolio website** for Sam KIM, a Logistics Warehouse Automation Expert. The entire site is contained in `index.html` with no build tools, no dependencies to install, and no compilation step. Open the file directly in a browser to view.

## Architecture

### Single-File Structure
- **`index.html`** — contains all HTML, CSS (inline `<style>`), and JavaScript (inline `<script>`)
- No external build tooling (Webpack, Vite, etc.)
- No package manager or `node_modules`
- No separate source directories

### Technology Stack
- **HTML5 / CSS3** — semantic markup and custom CSS animations
- **Tailwind CSS** (via CDN) — utility-first styling for layout, spacing, colors, and responsive design
- **Google Fonts: Noto Sans KR** (via CDN) — Korean web font for Korean-language content
- **Vanilla JavaScript** (inline) — three main behaviors:
  - Navbar opacity toggle on scroll
  - Mobile hamburger menu toggle
  - Scroll-reveal fade-in animations via `IntersectionObserver` API

### Page Structure
The site is organized into 5 sections via anchor navigation:
- `#home` — Hero banner with gradient background and CTA
- `#about` — About Me section with 4 info cards (experience, location, education, interests)
- `#skills` — Core Competencies with 5 skill cards
- `#projects` — Major Projects with 5 project cards
- `#contact` — Contact section with email link

### Key Custom Features
- `.hero-gradient` — linear gradient background for hero section
- `fadeInUp` keyframes — CSS animation for scroll-reveal effect
- `max-height` transition on mobile menu — smooth hamburger open/close
- Card hover effects — subtle scaling and shadow on skill/project cards

## Development

### No Build Step Required
Simply open `index.html` directly in a browser, or serve it locally:

```bash
# Option 1: Windows - open directly in default browser
start index.html

# Option 2: Use a local HTTP server (requires Node.js)
npx serve .

# Option 3: Python built-in server
python -m http.server 8000
```

### No Commands for Lint / Test
This is a static site with no toolchain. Validation is manual:
- Preview in a browser
- Test responsive behavior (resize browser, check mobile menu on small screens)
- Verify all 5 sections render and animations play smoothly
- Check that anchor navigation (#home, #about, etc.) works

### Editing the Site
1. Edit `index.html` directly in any text editor
2. Refresh the browser to see changes
3. Keep all CSS and JS inline — do not extract or refactor into separate files

## Key Considerations

- **Korean Language**: Content is in Korean with English section headings. Maintain the existing language split and font setup.
- **No Dependencies**: Do not introduce build tools, package managers, or external dependencies. Keep it simple and static.
- **Light Theme**: The site uses a light color palette (white backgrounds, gray text, colored accents). Maintain consistency with existing colors.
- **Responsive Design**: Heavy use of Tailwind's responsive utilities (`sm:`, `md:`, `lg:`). Test on mobile, tablet, and desktop.
- **Accessibility**: Ensure semantic HTML, proper heading hierarchy, and sufficient color contrast.

## Files

- `index.html` — Main site file (all HTML, CSS, JS combined)
- `index(최초).html` — Archived original version (do not modify)
- `참고이미지.jpeg` — Reference image (design/content reference)
- `.gitignore` — Git ignore rules
- `.claude/settings.local.json` — Claude Code local settings (do not modify)
