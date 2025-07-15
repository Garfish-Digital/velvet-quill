# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Velvet Quill is a sophisticated Astro-based demo site for an erotic/romance writers' collective and literary salon. The project showcases elegant design, advanced interactive components, and atmospheric effects suitable for a literary community.

## Development Commands

### Essential Commands
- `npm run dev` - Start development server (localhost:4321)
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm install` - Install dependencies

### Dependencies Management
- Core: Astro v5.11.0 with static site generation
- Styling: Sass for advanced CSS preprocessing
- Optional: Tailwind CSS available but primary styling uses custom SCSS

## Architecture

### Directory Structure
```
src/
├── layouts/
│   └── BaseLayout.astro          # Main layout with SEO, accessibility
├── components/
│   ├── TypewriterReveal.astro    # Animated typewriter text effect
│   ├── InkTransition.astro       # Ink bleed section transitions
│   ├── SecretContent.astro       # Hover-reveal hidden content
│   └── AuthorCard.astro          # Author profile cards with excerpts
├── styles/
│   ├── global.scss               # Main stylesheet with design system
│   ├── _variables.scss           # Color palette and design tokens
│   └── _textures.scss            # Texture mixins and effects
└── pages/
    └── index.astro               # Homepage with all sections
```

### Design System
**Color Palette:**
- Primary: Deep velvet (#4A0E4E), Midnight black (#0A0A0A)
- Secondary: Blush rose (#D4A5A5), Cream (#FFF8E7)
- Accent: Gold ink (#FFD700), Deep crimson (#8B0000)

**Typography:**
- Serif: Crimson Text (headings, literary content)
- Sans: Inter (UI elements, forms)

### Key Components

#### TypewriterReveal
- Animated text that appears as if being typed
- Configurable speed, delay, cursor display
- Intersection Observer for scroll-triggered animations

#### InkTransition  
- Section transition effects with ink bleed animations
- Multiple directions (up, down, left, right, radial)
- Multiple colors and intensity levels
- Trigger options: scroll, hover, click, load

#### SecretContent
- Hover/click/scroll revealed hidden content
- Multiple mask styles: blur, fade, ink, veil
- Accessibility features with ARIA labels
- Touch device support

#### AuthorCard
- Professional author profile cards
- Hover effects with image scaling and overlays
- Integrated SecretContent for excerpt reveals
- Social media links and book information
- Page curl and candlelight hover effects

### Styling Architecture

**SCSS Organization:**
- `_variables.scss`: Design tokens, colors, spacing, breakpoints
- `_textures.scss`: Mixins for paper grain, velvet overlays, ink effects
- `global.scss`: Base styles, typography, utility classes, responsive grid

**Key Features:**
- Custom CSS properties for dynamic theming
- Sophisticated hover and animation effects
- Mobile-first responsive design
- Accessibility considerations (reduced motion, focus states)
- Paper texture and velvet overlay effects

### Interactive Features

1. **Typewriter Text**: Hero section and content reveals
2. **Ink Bleed Transitions**: Between major sections
3. **Secret Content Reveals**: Reading room excerpts, form submissions
4. **Candlelight Ambiance**: Subtle flicker animations
5. **Page Curl Effects**: Author cards and excerpts
6. **Smooth Scrolling**: Navigation and anchor links

### Content Structure

**Sections:**
1. Hero - Typewriter intro with elegant tagline
2. Featured Authors - Interactive author cards with hidden excerpts
3. Upcoming Salons - Event calendar with dates and details
4. Reading Room - Hidden excerpt previews with different reveal styles
5. Join the Collective - Application form with secret reveal

### Development Notes

- Components use Intersection Observer for performance-optimized scroll animations
- All interactive elements include keyboard navigation support
- Custom CSS properties enable easy theme adjustments
- SCSS mixins provide reusable texture and effect patterns
- Mobile-responsive with progressive enhancement
- Semantic HTML structure for accessibility

### Performance Considerations

- Lazy loading for images and heavy animations
- CSS-based animations preferred over JavaScript
- Intersection Observer reduces unnecessary scroll event listeners
- Efficient component state management
- Optimized asset loading and bundling through Astro