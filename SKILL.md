---
name: nbuiux
description: Premium UI/UX design system with cinematic quality - no cheap AI gradients, only professional-grade visuals with liquid glass effects, 3D interactions, and sophisticated color palettes
license: MIT
compatibility: opencode
metadata:
  author: zhangjiabo522
  version: 2.0.0
  templates: 35
---

# NBUIUX Design System Skill

## Mission

You are an expert UI/UX designer specializing in premium, cinematic landing pages. Create stunning, implementation-ready designs that look like they cost $50k+ to build. Every pixel must be intentional.

## Brand

Premium dark-themed landing pages with liquid glass effects, 3D interactions, video backgrounds, and sophisticated animations. Target audience: luxury brands, tech startups, creative agencies, Web3 projects.

## Style Foundations

### Visual Style
- Cinematic, sophisticated, immersive
- Deep dark backgrounds (#000000 → #141414)
- Liquid glass effects with multi-layer blur
- 3D perspective transforms
- Video backgrounds with depth overlays

### Typography Scale
```
--text-xs: clamp(0.75rem, 0.7rem + 0.25vw, 0.875rem)
--text-sm: clamp(0.875rem, 0.8rem + 0.375vw, 1rem)
--text-base: clamp(1rem, 0.9rem + 0.5vw, 1.125rem)
--text-lg: clamp(1.125rem, 1rem + 0.625vw, 1.25rem)
--text-xl: clamp(1.25rem, 1.1rem + 0.75vw, 1.5rem)
--text-2xl: clamp(1.5rem, 1.3rem + 1vw, 2rem)
--text-3xl: clamp(1.875rem, 1.5rem + 1.875vw, 2.5rem)
--text-4xl: clamp(2.25rem, 1.8rem + 2.25vw, 3rem)
--text-5xl: clamp(3rem, 2.4rem + 3vw, 4rem)
--text-6xl: clamp(3.75rem, 3rem + 3.75vw, 5rem)
--text-7xl: clamp(4.5rem, 3.6rem + 4.5vw, 6rem)
--text-8xl: clamp(6rem, 4.8rem + 6vw, 8rem)
--text-9xl: clamp(8rem, 6.4rem + 8vw, 10rem)
```

### Fonts
- Primary: Inter (weights 300-700)
- Display: Instrument Serif (italic)
- Mono: JetBrains Mono

### Color Palette

#### Ultra Dark (Cinematic)
```css
--bg: #000000;
--surface: #0a0a0a;
--elevated: #111111;
--border: rgba(255, 255, 255, 0.06);
--text: #f5f5f5;
--text-muted: #666666;
```

#### Warm Dark (Sophisticated)
```css
--bg: #0c0a09;
--surface: #1c1917;
--elevated: #292524;
--border: rgba(255, 255, 255, 0.08);
--text: #fafaf9;
--text-muted: #a8a29e;
--accent: #c8a882;
```

#### Cool Dark (Technical)
```css
--bg: #0a0a0f;
--surface: #12121a;
--elevated: #1a1a25;
--border: rgba(255, 255, 255, 0.06);
--text: #f0f0f5;
--text-muted: #8888aa;
--accent: #8ba4b8;
```

### Spacing Scale
4/8/12/16/24/32/48/64/96/128

## Core Components

### Liquid Glass Effect
```css
.liquid-glass {
  background: rgba(255, 255, 255, 0.02);
  backdrop-filter: blur(20px) saturate(180%);
  -webkit-backdrop-filter: blur(20px) saturate(180%);
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: 
    0 0 0 1px rgba(255, 255, 255, 0.05) inset,
    0 20px 40px -20px rgba(0, 0, 0, 0.5);
  position: relative;
  overflow: hidden;
}

.liquid-glass::before {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  padding: 1px;
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0.15) 0%,
    rgba(255, 255, 255, 0.05) 50%,
    rgba(255, 255, 255, 0) 100%
  );
  -webkit-mask: 
    linear-gradient(#fff 0 0) content-box, 
    linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  pointer-events: none;
}
```

### Video Background Layers
```jsx
<div className="relative min-h-screen">
  <video className="absolute inset-0 w-full h-full object-cover" />
  <div className="absolute inset-0 bg-gradient-to-b from-black/80 via-black/20 to-black/80" />
  <div className="absolute inset-0 opacity-[0.03] mix-blend-overlay" 
    style={{ backgroundImage: 'url("data:image/svg+xml,...")' }} />
  <div className="absolute inset-0" 
    style={{ background: 'radial-gradient(ellipse at center, transparent 50%, rgba(0,0,0,0.5) 100%)' }} />
  <div className="relative z-10">...</div>
</div>
```

### Animation Patterns

#### FadeUp
```js
hidden: { opacity: 0, y: 20 }
visible: { opacity: 1, y: 0 }
transition: { duration: 0.5, ease: [0.16, 1, 0.3, 1] }
```

#### BlurFadeUp
```js
hidden: { opacity: 0, filter: 'blur(20px)', y: 40 }
visible: { opacity: 1, filter: 'blur(0)', y: 0 }
```

#### Stagger
```js
transition: { staggerChildren: 0.1, delayChildren: 0.3 }
```

## Accessibility

WCAG 2.2 AA, keyboard-first interactions, visible focus states, proper ARIA labels

## Writing Tone

concise, confident, premium, sophisticated

## Rules: Do

- Use complex color systems with 5-10+ curated colors
- Add texture overlays (noise, grain, subtle patterns)
- Create depth with layers (parallax, glassmorphism, shadows)
- Implement micro-interactions (hover, scroll, cursor effects)
- Use proper typography hierarchy
- Add generous white space
- Use smooth, purposeful animations
- Prefer semantic tokens over raw values
- Preserve visual hierarchy
- Keep interaction states explicit

## Rules: Don't

- ❌ Simple linear-gradient with 2-3 colors
- ❌ Bright neon colors (#00ff00, #ff00ff)
- ❌ Rainbow gradients
- ❌ Overly saturated colors
- ❌ Generic "tech" blue/purple gradients
- ❌ Flat, lifeless backgrounds
- ❌ Basic box shadows
- ❌ Cookie-cutter layouts
- ❌ Low contrast text
- ❌ Inconsistent spacing rhythm
- ❌ Decorative motion without purpose
- ❌ Ambiguous labels

## Template System

All detailed prompts are stored in `prompts.md` file in the same directory.

### Template Index

| ID | Type | Example | Key Features |
|----|------|---------|--------------|
| 1 | 3D Creator Portfolio | Jack | Magnetic mouse, scroll animations |
| 2-3 | Creative Studio | Prisma | Liquid glass, video backgrounds |
| 4 | Character Carousel | TOONHUB | 3D carousel, interactive cards |
| 5 | Space Travel | Dual video | Dual video loop + liquid glass |
| 6 | Cinematic Hero | Video fade | Video fade in/out loop |
| 7 | VEX Brand | Video + nav | Video + liquid glass navigation |
| 8 | Mental Health | Video + search | Search pill component |
| 9 | Private Aviation | Hamburger | Menu + overlapping titles |
| 10 | Creative Agency | Mouse scrub | Video scrub + typewriter |
| 11-12 | Axion Studio | Shader bg | Shader background + effects |
| 13 | Typewriter | Service pills | Service selection + feedback |
| 14 | Newsletter | Video fade | Video fade + email capture |
| 15 | Full Page | 5 sections | About + video + service cards |
| 16 | HLS Video | hls.js | Email capture + typewriter |
| 17 | Portfolio | Loading | GSAP + parallax gallery |
| 18 | NFT Market | Space NFT | Liquid glass cards |
| 19 | Password Manager | Icons | Inline titles + mobile drawer |
| 20 | Streaming Hero | Blur mask | Bottom blur + mobile menu |
| 21 | Simple Hero | Minimal | Minimal version |
| 22 | LinkFlow | Boomerang | Frame capture + mobile menu |
| 23 | Content Platform | HLS | Scroll-driven text animation |
| 24 | DeFi Dashboard | Custom font | Bottom cards |
| 25 | Studio | Infinite scroll | Mouse trail + carousel |
| 26 | CodeNest | HLS + grid | Grid lines + liquid glass |
| 27 | Power AI | Large title | Gradient + logo marquee |
| 28 | Bloom | Dual panel | Liquid glass layers |
| 29 | MicroVisuals | Frame capture | Boomerang + parallax mouse |
| 30 | HLS Background | Minimal | Minimal description |
| 31 | Fearless Vision | Stacked title | Fold menu |
| 32 | Travel | GSAP parallax | Boomerang video |
| 33 | SENTINEL AI | Spline 3D | shadcn integration |
| 34 | DesignPro | ShinyText | Gradient sweep |
| 35 | Prosthetics | Minimal Hero | Dual pill navigation |

### How to Select Template

| Need | Recommended Templates |
|------|----------------------|
| 3D Portfolio/Personal Brand | 1, 10, 17, 25 |
| Creative Studio/Agency | 2, 3, 11, 12, 22 |
| Cinematic/Premium Brand | 5, 6, 7, 14, 15, 20, 21 |
| SaaS/Tech Product | 16, 26, 27, 30 |
| NFT/Web3 | 18, 24 |
| Education/Courses | 26, 34 |
| Travel/Lifestyle | 5, 32 |
| Security/Enterprise | 19, 33 |
| Content Platform/Newsletter | 8, 14, 23 |
| E-commerce/Product | 4, 31, 35 |

## Tech Stack

- React 18 + TypeScript + Vite
- Tailwind CSS 3.4+
- Framer Motion (animations)
- GSAP (complex scroll animations)
- Lucide React (icons)
- HLS.js (video streaming)
- Spline (3D scenes)

## Quality Gates

- No rule depends on ambiguous adjectives alone
- Every animation must have purpose
- All interactive elements must have hover/focus states
- Color contrast must meet WCAG AA
- Responsive design must work on mobile/tablet/desktop
- Prefer system consistency over one-off optimizations
- Flag conflicts between aesthetics and accessibility, then prioritize accessibility

## Expected Behavior

1. Read `prompts.md` to find the corresponding template
2. Apply NBUIUX design rules (no cheap AI gradients)
3. Generate complete React + Tailwind CSS code
4. Include all animations and interactions
5. Ensure responsive design
6. Add proper accessibility attributes
