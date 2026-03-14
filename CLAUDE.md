# Nosura — Project Conventions

## Overview
This is a Shopify 2.0 theme based on Prestige v10.11.1, configured for nosura.com — a general online store.

## Critical Rules

### Security (NEVER violate)
- **NO external domain links** in any theme file (`.liquid`, `.js`, `.css`)
- Only allowed external domains: `cdn.shopify.com`, `fonts.shopifycdn.com`, `schema.org`, `fonts.gstatic.com`, `www.gstatic.com`
- Video embeds (`youtube.com`, `vimeo.com`) are allowed only in iframe `src` attributes
- **NO `eval()`**, `atob()`, `btoa()`, `new Function()`, or `document.write()` in any JS
- **NO external CDN** for libraries - self-host all JS/CSS in `assets/`
- Never add tracking pixels, beacons, or analytics scripts without explicit approval

### Google Merchant Centre Compliance
- All `<img>` tags MUST have `alt` attributes
- All product pages MUST output valid JSON-LD structured data (`@type: Product`)
- All pages MUST have `<link rel="canonical" href="{{ canonical_url }}" />`
- All pages MUST have proper `<title>` and `<meta name="description">`
- Use semantic HTML5
- No hidden text, cloaking, or deceptive redirects
- No hardcoded store URLs - use `{{ shop.url }}` or relative paths

### Design System
- **Color scheme**: Neutral mono (black/white/gold #FBBF24)
- **Heading font**: Instrument Sans, uppercase, 18% letter-spacing
- **Body font**: Nunito, 14px
- **Buttons**: 0px border radius (sharp corners), uppercase

### File Structure
- `layout/` - Master layout (theme.liquid)
- `sections/` - Theme sections (64 sections)
- `snippets/` - Reusable components (43 snippets)
- `blocks/` - Theme blocks (27 blocks)
- `assets/` - CSS, JS, SVG
- `config/` - Theme settings schema and data
- `locales/` - Translation files (27 languages)
- `templates/` - Page templates (JSON format)
