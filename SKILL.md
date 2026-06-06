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

### Color Palette (NO warm/yellow tones!)

```css
/* Pure Black & White */
:root {
  --bg: #000000;
  --bg-surface: #0a0a0a;
  --bg-elevated: #111111;
  --bg-card: #141414;
  --border: rgba(255,255,255,0.06);
  --border-hover: rgba(255,255,255,0.12);
  --text: #ffffff;
  --text-secondary: #a0a0a0;
  --text-muted: #666666;
}

/* Cool Blue Accent */
:root {
  --accent: #3b82f6;
  --accent-hover: #60a5fa;
  --accent-muted: rgba(59,130,246,0.15);
}

/* Cool Purple Accent */
:root {
  --accent: #8b5cf6;
  --accent-hover: #a78bfa;
  --accent-muted: rgba(139,92,246,0.15);
}

/* Cool Cyan Accent */
:root {
  --accent: #06b6d4;
  --accent-hover: #22d3ee;
  --accent-muted: rgba(6,182,212,0.15);
}

/* Neutral Gray (no color) */
:root {
  --accent: #e5e5e5;
  --accent-hover: #f5f5f5;
  --accent-muted: rgba(229,229,229,0.1);
}
```

### ❌ BANNED Colors
- #c8a882 (屎黄色)
- #f59e0b (amber)
- #fbbf24 (yellow)
- #fcd34d (gold)
- Any warm/yellow/orange tones
- Neon colors
- Rainbow gradients

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
