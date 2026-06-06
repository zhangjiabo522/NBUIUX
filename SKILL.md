---
name: nbuiux
description: Premium landing page design system - 35 cinematic templates with liquid glass, 3D effects, video backgrounds
license: MIT
compatibility: opencode
metadata:
  author: zhangjiabo522
  version: 7.0.0
  templates: 35
---

# NBUIUX - Premium Landing Page Generator

## Workflow

When user requests a landing page:

1. **Ask requirements** - What type? What style? Any specific features?
2. **Select category** - Use category table below
3. **Read prompt** - Open `prompts/template-X.md` (X = template number)
4. **Generate code** - Follow the prompt, apply design rules

## Template Categories

### 🎨 Portfolio & Personal Brand
| # | Name | Features | File |
|---|------|----------|------|
| 1 | Jack 3D | Magnetic mouse, scroll animations | `prompts/template-1.md` |
| 10 | Mainframe | Mouse scrub video, typewriter | `prompts/template-10.md` |
| 17 | Michael Smith | Loading screen, GSAP parallax | `prompts/template-17.md` |
| 25 | Viktor Oddy | Infinite scroll, mouse trail | `prompts/template-25.md` |
| 29 | MicroVisuals | Frame capture boomerang | `prompts/template-29.md` |

### 🎬 Cinematic & Premium
| # | Name | Features | File |
|---|------|----------|------|
| 5 | Space Travel | Dual video, liquid glass | `prompts/template-5.md` |
| 6 | Cinematic Hero | Video fade loop | `prompts/template-6.md` |
| 7 | VEX Brand | Video + glass nav | `prompts/template-7.md` |
| 14 | Asme Newsletter | Video fade + email | `prompts/template-14.md` |
| 15 | Asme Full | 5 sections | `prompts/template-15.md` |
| 20 | Movie Hero | Blur mask | `prompts/template-20.md` |
| 21 | Simple Hero | Minimal video | `prompts/template-21.md` |

### 🏢 Agency & Studio
| # | Name | Features | File |
|---|------|----------|------|
| 2 | Prisma v1 | Liquid glass, video bg | `prompts/template-2.md` |
| 3 | Prisma v2 | Same with variations | `prompts/template-3.md` |
| 11 | Axion v1 | Shader bg | `prompts/template-11.md` |
| 12 | Axion v2 | Shader bg variations | `prompts/template-12.md` |
| 22 | LinkFlow | Boomerang video | `prompts/template-22.md` |
| 25 | Viktor Oddy | Mouse trail, carousel | `prompts/template-25.md` |
| 31 | Fearless Vision | Stacked title | `prompts/template-31.md` |

### 💻 SaaS & Tech
| # | Name | Features | File |
|---|------|----------|------|
| 8 | Mental Health | Search pill | `prompts/template-8.md` |
| 13 | Typewriter | Service pills | `prompts/template-13.md` |
| 16 | Asme HLS | HLS + typewriter | `prompts/template-16.md` |
| 22 | LinkFlow | Boomerang video | `prompts/template-22.md` |
| 26 | CodeNest | Grid lines, glass cards | `prompts/template-26.md` |
| 27 | Power AI | Large title gradient | `prompts/template-27.md` |
| 28 | Bloom | Dual panel | `prompts/template-28.md` |
| 30 | HLS Background | Minimal HLS | `prompts/template-30.md` |

### 🔗 Web3 & NFT
| # | Name | Features | File |
|---|------|----------|------|
| 18 | Orbis NFT | Space theme, glass cards | `prompts/template-18.md` |
| 24 | RIVR DeFi | Custom font, bottom cards | `prompts/template-24.md` |

### 📰 Content & Newsletter
| # | Name | Features | File |
|---|------|----------|------|
| 8 | Mental Health | Search pill | `prompts/template-8.md` |
| 14 | Asme Newsletter | Video fade + email | `prompts/template-14.md` |
| 15 | Asme Full | 5 sections | `prompts/template-15.md` |
| 23 | Mindloop | Scroll text animation | `prompts/template-23.md` |

### ✈️ Travel & Lifestyle
| # | Name | Features | File |
|---|------|----------|------|
| 5 | Space Travel | Dual video, liquid glass | `prompts/template-5.md` |
| 9 | SkyElite | Overlapping titles | `prompts/template-9.md` |
| 32 | Wanderful | GSAP parallax | `prompts/template-32.md` |

### 🔒 Security & Enterprise
| # | Name | Features | File |
|---|------|----------|------|
| 19 | VaultShield | Icon titles, mobile drawer | `prompts/template-19.md` |
| 33 | SENTINEL AI | Spline 3D, shadcn | `prompts/template-33.md` |

### 📚 Education & Courses
| # | Name | Features | File |
|---|------|----------|------|
| 26 | CodeNest | Grid lines, glass cards | `prompts/template-26.md` |
| 34 | DesignPro | ShinyText gradient | `prompts/template-34.md` |

### 🛒 E-commerce & Product
| # | Name | Features | File |
|---|------|----------|------|
| 4 | TOONHUB | 3D carousel | `prompts/template-4.md` |
| 35 | Prosthetics | Minimal hero | `prompts/template-35.md` |

## Quick Match

| User Says | Category | Templates |
|-----------|----------|-----------|
| "AI startup" | SaaS | 16, 27 |
| "NFT marketplace" | Web3 | 18, 24 |
| "Creative portfolio" | Portfolio | 1, 10, 17, 25 |
| "Design agency" | Agency | 2, 3, 11, 12 |
| "Luxury brand" | Cinematic | 5, 6, 7, 20 |
| "SaaS product" | SaaS | 16, 26, 27, 30 |
| "Newsletter" | Content | 8, 14, 23 |
| "Travel brand" | Travel | 5, 9, 32 |
| "Security company" | Security | 19, 33 |
| "Education" | Education | 26, 34 |
| "E-commerce" | E-commerce | 4, 35 |

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
```

### ❌ BANNED Colors
- #c8a882 (warm yellow)
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

### 3D Effects
```css
.perspective-container {
  perspective: 1000px;
  perspective-origin: 50% 50%;
}

@keyframes float3d {
  0%, 100% { transform: translateZ(0) rotateX(0) rotateY(0); }
  25% { transform: translateZ(20px) rotateX(5deg) rotateY(5deg); }
  50% { transform: translateZ(40px) rotateX(0) rotateY(10deg); }
  75% { transform: translateZ(20px) rotateX(-5deg) rotateY(5deg); }
}
```

### Animation (Anime.js)
```js
// FadeUp
anime({
  targets: '.element',
  opacity: [0, 1],
  translateY: [20, 0],
  duration: 800,
  easing: 'easeOutExpo'
});

// Stagger
anime({
  targets: '.element',
  opacity: [0, 1],
  translateY: [20, 0],
  duration: 800,
  delay: anime.stagger(100, {start: 300}),
  easing: 'easeOutExpo'
});

// Scroll-Triggered
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      anime({
        targets: entry.target,
        opacity: [0, 1],
        translateY: [50, 0],
        duration: 1000,
        easing: 'easeOutExpo'
      });
    }
  });
});
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
- **Anime.js** (primary animation library)
- GSAP (complex scroll animations)
- Lucide React
- HLS.js

## Files
- `SKILL.md` - This file
- `prompts/` - 35 template prompts
  - `template-1.md` to `template-35.md`
- `README.md` - Documentation
