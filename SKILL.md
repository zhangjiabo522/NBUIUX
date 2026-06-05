---
name: nbuiux
description: Premium UI/UX design with cinematic quality - no cheap AI gradients, only professional-grade visuals with advanced effects and sophisticated color palettes
license: MIT
compatibility: opencode
metadata:
  audience: senior frontend developers
  workflow: premium-ui-design
---

## What I do

I create **premium-grade** UI/UX designs that look like they cost $50k+ to build. Every design is cinematic, sophisticated, and absolutely stunning. No cheap AI-looking gradients or amateur effects.

## ⚠️ CRITICAL DESIGN RULES

### ❌ NEVER DO THESE (AI-looking cheap effects):
- Simple linear-gradient with 2-3 colors
- Bright neon colors (#00ff00, #ff00ff, etc.)
- Rainbow gradients
- Overly saturated colors
- Generic "tech" blue/purple gradients
- Flat, lifeless backgrounds
- Basic box shadows
- Cookie-cutter layouts

### ✅ ALWAYS DO THESE (Premium quality):
- **Complex color systems** with 5-10+ carefully curated colors
- **Sophisticated gradients** with multiple stops, opacity variations
- **Texture overlays** (noise, grain, subtle patterns)
- **Depth and layers** (parallax, glassmorphism, shadows)
- **Micro-interactions** (hover states, scroll animations, cursor effects)
- **Typography hierarchy** with contrast and rhythm
- **White space** - generous, intentional spacing
- **Motion design** - smooth, purposeful animations

## 🎨 COLOR SYSTEM RULES

### Rule 1: Use Sophisticated Palettes
```css
/* ❌ BAD - AI-looking */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* ✅ GOOD - Premium */
:root {
  --bg-primary: #0a0a0a;
  --bg-secondary: #111111;
  --bg-tertiary: #1a1a1a;
  --surface: #141414;
  --surface-hover: #1f1f1f;
  --border: rgba(255, 255, 255, 0.06);
  --border-hover: rgba(255, 255, 255, 0.12);
  --text-primary: #f5f5f5;
  --text-secondary: #a0a0a0;
  --text-tertiary: #666666;
  --accent: #e8e8e8;
  --accent-subtle: rgba(255, 255, 255, 0.08);
}
```

### Rule 2: Dark Themes - Go DEEP
```css
/* Premium dark palette */
--bg-void: #000000;
--bg-deep: #050505;
--bg-base: #0a0a0a;
--bg-elevated: #0f0f0f;
--bg-surface: #141414;
--bg-surface-hover: #1a1a1a;
--bg-muted: #222222;

/* Sophisticated grays */
--gray-50: #fafafa;
--gray-100: #f5f5f5;
--gray-200: #e5e5e5;
--gray-300: #d4d4d4;
--gray-400: #a3a3a3;
--gray-500: #737373;
--gray-600: #525252;
--gray-700: #404040;
--gray-800: #262626;
--gray-900: #171717;
--gray-950: #0a0a0a;
```

### Rule 3: Accent Colors - Be Intentional
```css
/* Subtle, sophisticated accents */
--accent-warm: #c8a882;
--accent-cool: #8ba4b8;
--accent-neutral: #a0a0a0;
--accent-highlight: #ffffff;

/* NEVER use these */
/* --neon-green: #00ff00;  ❌ */
/* --cyber-blue: #00d4ff;  ❌ */
/* --matrix-purple: #bf00ff;  ❌ */
```

### Rule 4: Gradients - Complex & Subtle
```css
/* ❌ BAD - Simple and cheap */
background: linear-gradient(135deg, #667eea, #764ba2);

/* ✅ GOOD - Complex and sophisticated */
background: 
  radial-gradient(ellipse at 20% 50%, rgba(120, 119, 198, 0.15) 0%, transparent 50%),
  radial-gradient(ellipse at 80% 20%, rgba(255, 255, 255, 0.03) 0%, transparent 40%),
  radial-gradient(ellipse at 50% 80%, rgba(120, 119, 198, 0.08) 0%, transparent 50%),
  linear-gradient(180deg, #0a0a0a 0%, #111111 100%);

/* Or use layered backgrounds */
background: 
  url("data:image/svg+xml,...") /* noise texture */,
  radial-gradient(...),
  linear-gradient(...);
```

## 🎬 VIDEO BACKGROUND RULES

### Always Add Depth Layers
```jsx
<div className="relative min-h-screen">
  {/* Video layer */}
  <video className="absolute inset-0 w-full h-full object-cover" />
  
  {/* Gradient overlays for depth */}
  <div className="absolute inset-0 bg-gradient-to-b from-black/80 via-black/20 to-black/80" />
  <div className="absolute inset-0 bg-gradient-to-r from-black/40 via-transparent to-black/40" />
  
  {/* Noise texture for film grain */}
  <div className="absolute inset-0 opacity-[0.03] mix-blend-overlay" 
    style={{ backgroundImage: 'url("data:image/svg+xml,...")' }} />
  
  {/* Vignette effect */}
  <div className="absolute inset-0" 
    style={{ background: 'radial-gradient(ellipse at center, transparent 50%, rgba(0,0,0,0.5) 100%)' }} />
  
  {/* Content */}
  <div className="relative z-10">...</div>
</div>
```

## ✨ ANIMATION RULES

### Rule 1: Smooth Easing
```js
// ❌ BAD - Linear or basic easing
transition: { ease: "easeOut" }

// ✅ GOOD - Custom cubic-bezier
transition: { 
  duration: 0.8, 
  ease: [0.16, 1, 0.3, 1] // Expo ease out
}
```

### Rule 2: Stagger Everything
```js
const container = {
  hidden: { opacity: 0 },
  show: {
    opacity: 1,
    transition: {
      staggerChildren: 0.1,
      delayChildren: 0.3,
    }
  }
};

const item = {
  hidden: { opacity: 0, y: 20 },
  show: { 
    opacity: 1, 
    y: 0,
    transition: { duration: 0.5, ease: [0.16, 1, 0.3, 1] }
  }
};
```

### Rule 3: Scroll-Driven Animations
```js
const { scrollYProgress } = useScroll();
const opacity = useTransform(scrollYProgress, [0, 0.2], [0, 1]);
const y = useTransform(scrollYProgress, [0, 0.2], [100, 0]);
const scale = useTransform(scrollYProgress, [0, 0.2], [0.8, 1]);
```

## 🖼️ LIQUID GLASS EFFECT (Premium Version)

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

/* Add inner glow */
.liquid-glass::after {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  background: radial-gradient(
    ellipse at 50% 0%,
    rgba(255, 255, 255, 0.1) 0%,
    transparent 60%
  );
  pointer-events: none;
}
```

## 📐 LAYOUT RULES

### Rule 1: Generous Spacing
```css
/* ❌ BAD - Cramped */
padding: 1rem;
gap: 0.5rem;

/* ✅ GOOD - Spacious */
padding: 2rem 3rem;
gap: 1.5rem;

/* Desktop */
@media (min-width: 1024px) {
  padding: 4rem 6rem;
  gap: 3rem;
}
```

### Rule 2: Typography Scale
```css
/* Use a proper type scale */
--text-xs: clamp(0.75rem, 0.7rem + 0.25vw, 0.875rem);
--text-sm: clamp(0.875rem, 0.8rem + 0.375vw, 1rem);
--text-base: clamp(1rem, 0.9rem + 0.5vw, 1.125rem);
--text-lg: clamp(1.125rem, 1rem + 0.625vw, 1.25rem);
--text-xl: clamp(1.25rem, 1.1rem + 0.75vw, 1.5rem);
--text-2xl: clamp(1.5rem, 1.3rem + 1vw, 2rem);
--text-3xl: clamp(1.875rem, 1.5rem + 1.875vw, 2.5rem);
--text-4xl: clamp(2.25rem, 1.8rem + 2.25vw, 3rem);
--text-5xl: clamp(3rem, 2.4rem + 3vw, 4rem);
--text-6xl: clamp(3.75rem, 3rem + 3.75vw, 5rem);
--text-7xl: clamp(4.5rem, 3.6rem + 4.5vw, 6rem);
--text-8xl: clamp(6rem, 4.8rem + 6vw, 8rem);
--text-9xl: clamp(8rem, 6.4rem + 8vw, 10rem);
```

## 🎯 TEMPLATE CATEGORIES

### 1. Cinematic & Premium (Templates 2, 3, 6, 7, 14, 15, 20, 21)
- Full-screen video backgrounds
- Liquid glass navigation
- Smooth scroll animations
- **For:** Luxury brands, entertainment, premium products

### 2. Creative Portfolio (Templates 1, 10, 25)
- Unique layouts
- Interactive elements
- Show-stopping animations
- **For:** Designers, artists, agencies

### 3. SaaS & Tech (Templates 5, 16, 27, 30)
- Clean, modern design
- Clear value proposition
- Professional aesthetics
- **For:** Startups, software companies

### 4. Web3 & NFT (Templates 18, 24)
- Dark, immersive themes
- Video showcases
- Futuristic feel
- **For:** Blockchain, crypto projects

### 5. Agency & Studio (Templates 11, 12, 22, 25)
- Bold typography
- Case study layouts
- Team showcases
- **For:** Creative agencies, consultancies

## 📦 TECH STACK

- **React 18** + TypeScript + Vite
- **Tailwind CSS 3.4+** (with custom config)
- **Framer Motion** (for animations)
- **GSAP** (for complex scroll animations)
- **Lucide React** (for icons)
- **HLS.js** (for video streaming)

## 🚀 USAGE EXAMPLES

```
User: "I need a premium landing page for my AI startup"
→ Use Template 16 with deep blacks, subtle glows, and smooth animations

User: "Create a luxury brand website"
→ Use Template 20 with cinematic video, elegant typography, and refined palette

User: "Build a creative portfolio"
→ Use Template 1 with unique layout, interactive elements, and bold design

User: "Design an NFT marketplace"
→ Use Template 18 with dark theme, video showcases, and futuristic feel
```

## 🎨 COLOR PALETTE EXAMPLES

### Ultra Dark (Cinematic)
```css
--bg: #000000;
--surface: #0a0a0a;
--elevated: #111111;
--border: rgba(255, 255, 255, 0.06);
--text: #f5f5f5;
--text-muted: #666666;
```

### Warm Dark (Sophisticated)
```css
--bg: #0c0a09;
--surface: #1c1917;
--elevated: #292524;
--border: rgba(255, 255, 255, 0.08);
--text: #fafaf9;
--text-muted: #a8a29e;
--accent: #c8a882;
```

### Cool Dark (Technical)
```css
--bg: #0a0a0f;
--surface: #12121a;
--elevated: #1a1a25;
--border: rgba(255, 255, 255, 0.06);
--text: #f0f0f5;
--text-muted: #8888aa;
--accent: #8ba4b8;
```

## Remember

**Every pixel matters.** Every color choice, every spacing decision, every animation curve should be intentional and sophisticated. We're building premium experiences, not templates.
