---
name: nbuiux
description: Premium UI/UX design system - 35 cinematic landing page templates with liquid glass, 3D effects, video backgrounds
license: MIT
compatibility: opencode
metadata:
  author: zhangjiabo522
  version: 3.0.0
  templates: 35
---

# NBUIUX - Premium Landing Page Generator

## How to Use This Skill

When user requests a landing page, follow these steps:

### Step 1: Ask User Requirements
Ask user:
1. What type of project? (SaaS, portfolio, NFT, agency, etc.)
2. What style? (cinematic, minimal, creative, etc.)
3. Any specific features? (video background, 3D effects, animations, etc.)

### Step 2: Select Template
Based on user requirements, select template from the list below:

| Template | Name | Type | Best For | Key Features |
|----------|------|------|----------|--------------|
| 1 | Jack 3D | Portfolio | 3D creators, artists | Magnetic mouse, scroll animations, 3D images |
| 2 | Prisma v1 | Studio | Creative agencies | Liquid glass, video bg, bold typography |
| 3 | Prisma v2 | Studio | Design firms | Same as v2 with variations |
| 4 | TOONHUB | Carousel | Character/toy brands | 3D carousel, interactive cards |
| 5 | Space Travel | Cinematic | Travel, luxury | Dual video loop, liquid glass |
| 6 | Cinematic Hero | Cinematic | Entertainment | Video fade in/out loop |
| 7 | VEX Brand | Cinematic | Premium brands | Video + liquid glass nav |
| 8 | Mental Health | SaaS | Health apps | Search pill component |
| 9 | SkyElite | Luxury | Aviation, luxury | Hamburger menu, overlapping titles |
| 10 | Mainframe | Agency | Creative agencies | Mouse scrub video, typewriter |
| 11 | Axion v1 | Agency | Studios | Shader background, effects |
| 12 | Axion v2 | Agency | Studios | Same with variations |
| 13 | Mainframe Typewriter | SaaS | Service platforms | Service pills, conditional feedback |
| 14 | Asme Newsletter | Content | Newsletters | Video fade + email capture |
| 15 | Asme Full Page | Content | Content platforms | 5 sections: about, video, services |
| 16 | Asme HLS | SaaS | Tech products | HLS video, email, typewriter |
| 17 | Michael Smith | Portfolio | Designers | Loading screen, GSAP, parallax gallery |
| 18 | Orbis NFT | Web3 | NFT marketplaces | Space theme, liquid glass cards |
| 19 | VaultShield | SaaS | Security products | Icon inline titles, mobile drawer |
| 20 | Movie Hero | Cinematic | Streaming, entertainment | Bottom blur mask, mobile menu |
| 21 | Simple Hero | Minimal | Any project | Minimal video background |
| 22 | LinkFlow | SaaS | Tech products | Boomerang video, mobile menu |
| 23 | Mindloop | Content | Content platforms | HLS video, scroll-driven text |
| 24 | RIVR DeFi | Web3 | DeFi dashboards | Custom font, bottom cards |
| 25 | Viktor Oddy | Agency | Design studios | Infinite scroll, mouse trail, carousel |
| 26 | CodeNest | Education | Coding bootcamps | HLS, grid lines, liquid glass cards |
| 27 | Power AI | SaaS | AI products | Large title gradient, logo marquee |
| 28 | Bloom | SaaS | AI/creative tools | Dual panel, liquid glass layers |
| 29 | MicroVisuals | Portfolio | Designers | Frame capture boomerang, parallax mouse |
| 30 | HLS Background | Minimal | Any project | Minimal HLS video |
| 31 | Fearless Vision | Agency | Creative agencies | Stacked title, fold menu |
| 32 | Wanderful | Travel | Travel brands | GSAP parallax, boomerang video |
| 33 | SENTINEL AI | Enterprise | Security companies | Spline 3D background, shadcn |
| 34 | DesignPro | Education | Design courses | ShinyText gradient sweep |
| 35 | Prosthetics | E-commerce | Medical products | Minimal hero, dual pill nav |

### Step 3: Read Template Prompt
After selecting template, read the corresponding prompt from `prompts.md` file.

The `prompts.md` file contains detailed prompts for each template numbered 1-35.

### Step 4: Generate Code
Generate complete React + Tailwind CSS code based on the prompt, applying these rules:

## Design Rules (MUST FOLLOW)

### ❌ NEVER DO
- Simple 2-3 color gradients
- Bright neon colors (#00ff00, #ff00ff)
- Rainbow gradients
- Generic blue/purple tech gradients
- Flat lifeless backgrounds
- Basic box shadows

### ✅ ALWAYS DO
- Deep dark backgrounds (#000000 → #141414)
- Complex color systems (5-10+ colors)
- Liquid glass effects (blur + border + shadow)
- Texture overlays (noise, grain)
- Smooth animations (cubic-bezier easing)
- Responsive design (mobile-first)

## Liquid Glass CSS
```css
.liquid-glass {
  background: rgba(255, 255, 255, 0.02);
  backdrop-filter: blur(20px) saturate(180%);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 0 0 0 1px rgba(255, 255, 255, 0.05) inset, 0 20px 40px -20px rgba(0, 0, 0, 0.5);
}
.liquid-glass::before {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  padding: 1px;
  background: linear-gradient(180deg, rgba(255,255,255,0.15) 0%, rgba(255,255,255,0.05) 50%, transparent 100%);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  pointer-events: none;
}
```

## Color Palettes
```css
/* Ultra Dark */
--bg: #000000; --surface: #0a0a0a; --text: #f5f5f5; --text-muted: #666666;

/* Warm Dark */
--bg: #0c0a09; --surface: #1c1917; --text: #fafaf9; --accent: #c8a882;

/* Cool Dark */
--bg: #0a0a0f; --surface: #12121a; --text: #f0f0f5; --accent: #8ba4b8;
```

## Animation Pattern
```js
// FadeUp
hidden: { opacity: 0, y: 20 }
visible: { opacity: 1, y: 0, transition: { duration: 0.5, ease: [0.16, 1, 0.3, 1] } }

// Stagger
transition: { staggerChildren: 0.1, delayChildren: 0.3 }
```

## Tech Stack
- React 18 + TypeScript + Vite
- Tailwind CSS 3.4+
- Framer Motion
- Lucide React
- HLS.js (for video)

## Example Workflow

User: "我要一个AI创业公司的landing page"

1. Select Template: 16 (Asme HLS) or 27 (Power AI)
2. Read prompts.md for template 16 or 27
3. Generate code with:
   - Dark background
   - Video background
   - Liquid glass navbar
   - Smooth animations
   - Responsive design
