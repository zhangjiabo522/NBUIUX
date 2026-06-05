# NBUIUX - Premium UI/UX Design Skill

<div align="center">

![NBUIUX Banner](https://img.shields.io/badge/NBUIUX-Premium%20UI%2FUX-000000?style=for-the-badge&logoColor=white)
![Version](https://img.shields.io/badge/version-1.0.0-000000?style=for-the-badge&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-000000?style=for-the-badge&logoColor=white)

**Create stunning, cinematic UI/UX designs that look like they cost $50k+ to build.**

No cheap AI-looking gradients. No amateur effects. Only premium-grade visuals.

</div>

---

## What is NBUIUX?

NBUIUX is an OpenCode skill that helps you create **premium-grade** UI/UX designs. Every design is cinematic, sophisticated, and absolutely stunning.

### Key Features

- **35+ Premium Templates** - From cinematic hero sections to creative portfolios
- **Liquid Glass Effects** - Multi-layer blur, subtle borders, and inner glows
- **3D Interactions** - Perspective transforms, parallax, and mouse tracking
- **Sophisticated Color Systems** - No cheap AI gradients, only curated palettes
- **Micro-interactions** - Hover states, scroll animations, cursor effects
- **Typography Hierarchy** - Proper type scale with contrast and rhythm
- **Texture Overlays** - Noise, grain, and subtle patterns for depth

---

## Installation

### Prerequisites

- [OpenCode](https://opencode.ai) installed
- Node.js 18+ (for running generated projects)

### Install the Skill

```bash
# Clone to your OpenCode skills directory
git clone git@github.com:zhangjiabo522/NBUIUX.git ~/.config/opencode/skills/nbuiux
```

Or copy the `SKILL.md` file to your skills directory:

```bash
# Create skills directory if it doesn't exist
mkdir -p ~/.config/opencode/skills/nbuiux

# Copy the skill file
cp SKILL.md ~/.config/opencode/skills/nbuiux/
```

---

## Usage

### Load the Skill

```
skill({ name: "nbuiux" })
```

### Describe Your Project

Tell me about your project, and I'll select the best template:

```
"I need a premium landing page for my AI startup"
"Create a luxury brand website"
"Build a creative portfolio"
"Design an NFT marketplace"
```

### Get the Code

I'll generate complete React + Tailwind CSS code with:
- Premium animations (Framer Motion / GSAP)
- Liquid glass effects
- Video backgrounds
- 3D interactions
- Responsive design

---

## Template Categories

### 1. Cinematic & Premium (Templates 2, 3, 6, 7, 14, 15, 20, 21)
- Full-screen video backgrounds
- Liquid glass navigation
- Smooth scroll animations
- **Best for:** Luxury brands, entertainment, premium products

### 2. Creative Portfolio (Templates 1, 10, 25)
- Unique layouts
- Interactive elements
- Show-stopping animations
- **Best for:** Designers, artists, agencies

### 3. SaaS & Tech (Templates 5, 16, 27, 30)
- Clean, modern design
- Clear value proposition
- Professional aesthetics
- **Best for:** Startups, software companies

### 4. Web3 & NFT (Templates 18, 24)
- Dark, immersive themes
- Video showcases
- Futuristic feel
- **Best for:** Blockchain, crypto projects

### 5. Agency & Studio (Templates 11, 12, 22, 25)
- Bold typography
- Case study layouts
- Team showcases
- **Best for:** Creative agencies, consultancies

---

## Design Rules

### ❌ NEVER DO (AI-looking cheap effects):
- Simple linear-gradient with 2-3 colors
- Bright neon colors (#00ff00, #ff00ff, etc.)
- Rainbow gradients
- Overly saturated colors
- Generic "tech" blue/purple gradients
- Flat, lifeless backgrounds
- Basic box shadows
- Cookie-cutter layouts

### ✅ ALWAYS DO (Premium quality):
- Complex color systems with 5-10+ carefully curated colors
- Sophisticated gradients with multiple stops, opacity variations
- Texture overlays (noise, grain, subtle patterns)
- Depth and layers (parallax, glassmorphism, shadows)
- Micro-interactions (hover states, scroll animations, cursor effects)
- Typography hierarchy with contrast and rhythm
- White space - generous, intentional spacing
- Motion design - smooth, purposeful animations

---

## Color System

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

---

## Liquid Glass Effect

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

---

## Tech Stack

- **Framework:** React 18 + TypeScript + Vite
- **Styling:** Tailwind CSS 3.4+
- **Animations:** Framer Motion, GSAP
- **Icons:** Lucide React
- **Video:** HLS.js for streaming
- **3D:** Spline for 3D scenes

---

## Animation Patterns

### FadeUp
```js
hidden: { opacity: 0, y: 20 }
visible: { opacity: 1, y: 0 }
```

### BlurFadeUp
```js
hidden: { opacity: 0, filter: 'blur(20px)', y: 40 }
visible: { opacity: 1, filter: 'blur(0)', y: 0 }
```

### SlideReveal
```js
hidden: { translateY: '110%' }
visible: { translateY: '0' }
```

### Custom Easing
```js
transition: { 
  duration: 0.8, 
  ease: [0.16, 1, 0.3, 1] // Expo ease out
}
```

---

## Examples

### AI Startup Landing Page
```
User: "I need a premium landing page for my AI startup"
→ Deep blacks, subtle glows, smooth animations
→ Template 16 with liquid glass navbar
```

### Luxury Brand Website
```
User: "Create a luxury brand website"
→ Cinematic video, elegant typography, refined palette
→ Template 20 with video background
```

### Creative Portfolio
```
User: "Build a creative portfolio"
→ Unique layout, interactive elements, bold design
→ Template 1 with 3D effects
```

### NFT Marketplace
```
User: "Design an NFT marketplace"
→ Dark theme, video showcases, futuristic feel
→ Template 18 with glass morphism
```

---

## Project Structure

```
nbuiux/
├── SKILL.md          # Main skill file
├── README.md         # This file
└── examples/         # Example projects (coming soon)
```

---

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- Inspired by premium design studios and agencies
- Built for developers who demand the best
- Created with ❤️ for the design community

---

<div align="center">

**[GitHub](https://github.com/zhangjiabo522/NBUIUX)** • **[Issues](https://github.com/zhangjiabo522/NBUIUX/issues)** • **[Discussions](https://github.com/zhangjiabo522/NBUIUX/discussions)**

</div>
