# BashSnippets — Cursor Project Context

## Stack
- Static HTML, GitHub Pages, NO build tools, NO npm, NO bundler
- All HTML files are self-contained (styles + scripts inline or CDN)
- Never introduce React, Vue, Webpack, or any framework

## Brand
- bg: #0d1117 | green: #39d353 | amber: #e3b341 | blue: #58a6ff | muted: #8b949e
- Fonts: IBM Plex Mono (body/code), Syne (headings) — Google Fonts CDN only
- CSS vars already defined in every file: --bg, --green, --amber, --blue, --muted

## Scripts That Must Survive Every Edit
- GA4: G-6B01TGE8XS
- AdSense: ca-pub-5399156622542127
- DigitalOcean affiliate: refcode 7a196437764c

## Three.js CDN (use ONLY this version/URL)
https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js

## 3D Hero Visual Direction
- Layer 1: Matrix particle field — tiny bash character glyphs (#,$,>,~) drifting downward
- Layer 2: Wireframe vortex tunnel behind particles — slow Z rotation, glitch energy
- Layer 3: Cursor gravity — particle field breathes toward mouse position
- Glitch pulse every 4-7s: random particle scatter + scanline sweep

## Performance Rules
- Low-end detection: hardwareConcurrency <= 2 OR window.innerWidth < 768
- Low-end: reduce to 700 particles, disable cursor gravity
- Pause loop when document.hidden, resume on visibilitychange
- Debounce resize handler 50ms
- setPixelRatio capped at 2

## Hero Canvas Rules
- canvas#hero-canvas: position absolute, full hero width/height, z-index 0, pointer-events none
- All hero text: position relative, z-index 2
- .hero: position relative, overflow hidden, min-height 92vh, flexbox centered

## What To Never Touch
- Any file in /snippets/
- sitemap.xml
- Nav and footer HTML
- Any existing GA4, AdSense, or affiliate code