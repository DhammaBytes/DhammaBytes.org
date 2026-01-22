# DhammaBytes Website

Static website for DhammaBytes, a group creating free apps for studying the Buddha's Dhamma.

## Structure

- `index.html` - Home page listing all apps
- `pali-practice/` - Landing page for Pāli Practice app
- `pali-practice/privacy-policy/` - Privacy policy for Pāli Practice
- `css/common.css` - Shared styles
- `img/` - App icons and images

## Design System

### Color Palette

Light mode:
- Background: `#fdfcfa`
- Text: `#3a3632`
- Headings: `#5c4a2a`
- Links: `#8b5a2b` (hover: `#a0522d`)
- Borders: `#d4c8b8`
- Subtle backgrounds: `#f5f0e8`
- Muted text: `#7a6b5a`

Dark mode:
- Background: `#1a1815`
- Text: `#d4cdc4`
- Headings: `#c9a86c`
- Links: `#d4a574` (hover: `#e0b584`)
- Borders: `#3a332a`
- Subtle backgrounds: `#2a2520`
- Muted text: `#a89878`

### Typography

- Font: Georgia, serif
- Base size: 1.05rem
- Line height: 1.6
- Max width: 42rem (centered)

### Components

**Store links**: Use `.store-link` class with inline SVG icons (16x16). Background changes on hover.

**Icons**: Inline SVGs with `class="icon"`, `aria-hidden="true"`, `viewBox="0 0 24 24"`. Use `fill: currentColor` for solid icons, `stroke: currentColor` for outlined.

**Blockquotes**: Use `.sutta-quote` class for Dhamma quotes (italic, left border accent).

## Coding Rules

- Use 4-space indentation
- Always include dark mode styles via `@media (prefers-color-scheme: dark)`
- External links get `target="_blank" rel="noopener"`
- Include meta tags: charset, viewport, theme-color, description, canonical, og:*
- App icons: 80x80 on home page, 128x128 on landing pages
- Each page has `<header>`, `<main>`, `<footer>`
- Use semantic HTML: `<article>` for app entries, proper heading hierarchy

## Accessibility

- Always include `lang="en"` on `<html>`
- Use `aria-labelledby` to label `<main>` sections when there's a heading
- Decorative icons get `aria-hidden="true"`
- Use `<abbr>` with `title` attribute for Pāli terms or abbreviations on first use
- All sizing in rem, never px (respects user font preferences)
- Aim for WCAG AA compliance
- Focus states must be visible (already in common.css)

## Performance

- Keep page weight minimal; inline page-specific CSS in `<style>` tags
- Common styles go in `css/common.css`
- Use SVG for icons (scalable, small, no extra requests when inlined)
- No JavaScript unless absolutely necessary

