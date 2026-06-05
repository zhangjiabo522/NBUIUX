---
name: nbuiux
description: Premium landing page design system - 35 cinematic templates with liquid glass, 3D effects, video backgrounds
license: MIT
compatibility: opencode
metadata:
  author: zhangjiabo522
  version: 4.0.0
  templates: 35
---

# NBUIUX - Premium Landing Page Generator

## Workflow

When user requests a landing page:

1. **Ask requirements** - What type? What style? Any specific features?
2. **Select template** - Use table below to find best match
3. **Read prompt** - Open `prompts.md`, find the template number
4. **Generate code** - Follow the prompt, apply design rules

## Template Selection

| # | Name | Type | For | Features |
|---|------|------|-----|----------|
| 1 | Jack 3D | Portfolio | 3D creators | Magnetic mouse, scroll animations |
| 2-3 | Prisma | Studio | Agencies | Liquid glass, video bg |
| 4 | TOONHUB | Carousel | Toy brands | 3D carousel |
| 5 | Space Travel | Cinematic | Travel | Dual video, liquid glass |
| 6 | Cinematic Hero | Cinematic | Entertainment | Video fade loop |
| 7 | VEX Brand | Cinematic | Luxury | Video + glass nav |
| 8 | Mental Health | SaaS | Health apps | Search pill |
| 9 | SkyElite | Luxury | Aviation | Overlapping titles |
| 10 | Mainframe | Agency | Creative | Mouse scrub video |
| 11-12 | Axion | Agency | Studios | Shader bg |
| 13 | Typewriter | SaaS | Services | Service pills |
| 14 | Asme Newsletter | Content | Newsletter | Email capture |
| 15 | Asme Full | Content | Platforms | 5 sections |
| 16 | Asme HLS | SaaS | Tech | HLS + typewriter |
| 17 | Michael Smith | Portfolio | Designers | GSAP parallax |
| 18 | Orbis NFT | Web3 | NFT | Space theme, glass cards |
| 19 | VaultShield | SaaS | Security | Icon titles |
| 20 | Movie Hero | Cinematic | Streaming | Blur mask |
| 21 | Simple Hero | Minimal | Any | Minimal video |
| 22 | LinkFlow | SaaS | Tech | Boomerang video |
| 23 | Mindloop | Content | Platforms | Scroll text |
| 24 | RIVR DeFi | Web3 | DeFi | Custom font |
| 25 | Viktor Oddy | Agency | Studios | Mouse trail |
| 26 | CodeNest | Education | Bootcamps | Grid lines |
| 27 | Power AI | SaaS | AI | Large title |
| 28 | Bloom | SaaS | AI tools | Dual panel |
| 29 | MicroVisuals | Portfolio | Designers | Frame capture |
| 30 | HLS Background | Minimal | Any | HLS video |
| 31 | Fearless Vision | Agency | Creative | Stacked title |
| 32 | Wanderful | Travel | Travel | GSAP parallax |
| 33 | SENTINEL AI | Enterprise | Security | Spline 3D |
| 34 | DesignPro | Education | Courses | ShinyText |
| 35 | Prosthetics | E-commerce | Medical | Minimal hero |

## Quick Match

| User Says | Use Template |
|-----------|--------------|
| "AI startup landing page" | 16, 27 |
| "NFT marketplace" | 18, 24 |
| "Creative portfolio" | 1, 10, 17, 25 |
| "Design agency" | 2, 3, 11, 12, 22 |
| "Luxury brand" | 5, 6, 7, 20 |
| "SaaS product" | 16, 26, 27, 30 |
| "Newsletter/content" | 8, 14, 23 |
| "Travel brand" | 5, 32 |
| "Security company" | 19, 33 |
| "Education/course" | 26, 34 |
| "Minimal/clean" | 21, 30, 35 |

## Design Rules

### Color
- Deep dark: #000000 → #141414
- No neon, no rainbow, no cheap gradients
- Use 5-10+ curated colors

### Glass Effect
```css
.glass {
  background: rgba(255,255,255,0.02);
  backdrop-filter: blur(20px) saturate(180%);
  border: 1px solid rgba(255,255,255,0.08);
  box-shadow: 0 0 0 1px rgba(255,255,255,0.05) inset, 0 20px 40px -20px rgba(0,0,0,0.5);
}
```

### Animation
```js
// FadeUp
{ opacity: 0, y: 20 } → { opacity: 1, y: 0 }
// Easing: [0.16, 1, 0.3, 1]
```

### Video Layers
1. Video (object-cover)
2. Gradient overlay (depth)
3. Noise texture (grain)
4. Vignette (edges)
5. Content (z-10)

## Tech Stack
- React 18 + TypeScript + Vite
- Tailwind CSS 3.4+
- Framer Motion / GSAP
- Lucide React
- HLS.js

## Files
- `SKILL.md` - This file
- `prompts.md` - 35 detailed prompts
- `README.md` - Documentation
