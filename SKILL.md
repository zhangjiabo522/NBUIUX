---
name: nbuiux
description: Premium landing page design system - 35 cinematic templates with liquid glass, 3D effects, video backgrounds
license: MIT
compatibility: opencode
metadata:
  author: zhangjiabo522
  version: 5.0.0
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

### 3D Effects

#### Perspective Container
```css
.perspective-container {
  perspective: 1000px;
  perspective-origin: 50% 50%;
}
```

#### 3D Card Tilt (Mouse Follow)
```js
// Framer Motion
const [rotateX, setRotateX] = useState(0);
const [rotateY, setRotateY] = useState(0);

const handleMouseMove = (e) => {
  const rect = e.currentTarget.getBoundingClientRect();
  const x = e.clientX - rect.left;
  const y = e.clientY - rect.top;
  const centerX = rect.width / 2;
  const centerY = rect.height / 2;
  setRotateX((y - centerY) / 20);
  setRotateY((centerX - x) / 20);
};

// In JSX
<motion.div
  animate={{ rotateX, rotateY }}
  transition={{ type: "spring", stiffness: 300, damping: 30 }}
  style={{ transformStyle: "preserve-3d" }}
>
  <div style={{ transform: "translateZ(50px)" }}>Content</div>
</motion.div>
```

#### 3D Floating Elements
```css
@keyframes float3d {
  0%, 100% { transform: translateZ(0) rotateX(0) rotateY(0); }
  25% { transform: translateZ(20px) rotateX(5deg) rotateY(5deg); }
  50% { transform: translateZ(40px) rotateX(0) rotateY(10deg); }
  75% { transform: translateZ(20px) rotateX(-5deg) rotateY(5deg); }
}

.float-3d {
  animation: float3d 6s ease-in-out infinite;
  transform-style: preserve-3d;
}
```

### Mouse Particle Effects

#### Particle Trail
```js
const ParticleTrail = () => {
  const canvasRef = useRef(null);
  const particles = useRef([]);
  const mouse = useRef({ x: 0, y: 0 });

  useEffect(() => {
    const canvas = canvasRef.current;
    const ctx = canvas.getContext('2d');
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    const addParticle = (x, y) => {
      particles.current.push({
        x, y,
        vx: (Math.random() - 0.5) * 2,
        vy: (Math.random() - 0.5) * 2,
        life: 1,
        size: Math.random() * 3 + 1,
        color: `hsla(${210 + Math.random() * 30}, 80%, 60%, `
      });
    };

    const animate = () => {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      
      particles.current.forEach((p, i) => {
        p.x += p.vx;
        p.y += p.vy;
        p.life -= 0.02;
        
        if (p.life <= 0) {
          particles.current.splice(i, 1);
          return;
        }

        ctx.beginPath();
        ctx.arc(p.x, p.y, p.size * p.life, 0, Math.PI * 2);
        ctx.fillStyle = p.color + p.life + ')';
        ctx.fill();
      });

      requestAnimationFrame(animate);
    };

    const handleMouseMove = (e) => {
      mouse.current = { x: e.clientX, y: e.clientY };
      if (Math.random() > 0.5) addParticle(e.clientX, e.clientY);
    };

    window.addEventListener('mousemove', handleMouseMove);
    animate();

    return () => window.removeEventListener('mousemove', handleMouseMove);
  }, []);

  return <canvas ref={canvasRef} className="fixed inset-0 pointer-events-none z-50" />;
};
```

#### Glowing Cursor
```js
const GlowingCursor = () => {
  const [position, setPosition] = useState({ x: 0, y: 0 });
  const [isHovering, setIsHovering] = useState(false);

  useEffect(() => {
    const handleMouseMove = (e) => {
      setPosition({ x: e.clientX, y: e.clientY });
    };
    window.addEventListener('mousemove', handleMouseMove);
    return () => window.removeEventListener('mousemove', handleMouseMove);
  }, []);

  return (
    <motion.div
      className="fixed pointer-events-none z-50"
      animate={{
        x: position.x - 20,
        y: position.y - 20,
        scale: isHovering ? 1.5 : 1,
      }}
      transition={{ type: "spring", stiffness: 500, damping: 28 }}
    >
      <div className="w-10 h-10 rounded-full bg-gradient-to-r from-blue-500/30 to-purple-500/30 blur-xl" />
    </motion.div>
  );
};
```

### Gravity Effects

#### Falling Elements
```js
const GravityElement = ({ children }) => {
  const [position, setPosition] = useState({ x: 0, y: 0 });
  const [velocity, setVelocity] = useState({ x: 0, y: 0 });
  const gravity = 0.5;
  const friction = 0.99;

  useEffect(() => {
    const handleMouseMove = (e) => {
      const rect = e.currentTarget.getBoundingClientRect();
      const centerX = rect.left + rect.width / 2;
      const centerY = rect.top + rect.height / 2;
      const dx = e.clientX - centerX;
      const dy = e.clientY - centerY;
      const distance = Math.sqrt(dx * dx + dy * dy);
      
      if (distance < 200) {
        setVelocity(prev => ({
          x: prev.x - (dx / distance) * 2,
          y: prev.y - (dy / distance) * 2
        }));
      }
    };

    const animate = () => {
      setVelocity(prev => ({
        x: prev.x * friction,
        y: prev.y * friction + gravity
      }));
      
      setPosition(prev => ({
        x: prev.x + velocity.x,
        y: prev.y + velocity.y
      }));

      requestAnimationFrame(animate);
    };

    animate();
  }, []);

  return (
    <motion.div
      animate={{ x: position.x, y: position.y }}
      transition={{ type: "spring", stiffness: 100, damping: 10 }}
    >
      {children}
    </motion.div>
  );
};
```

#### Magnetic Hover Effect
```js
const MagneticElement = ({ children, strength = 0.3 }) => {
  const ref = useRef(null);
  const [position, setPosition] = useState({ x: 0, y: 0 });

  const handleMouseMove = (e) => {
    const rect = ref.current.getBoundingClientRect();
    const centerX = rect.left + rect.width / 2;
    const centerY = rect.top + rect.height / 2;
    const dx = e.clientX - centerX;
    const dy = e.clientY - centerY;
    
    setPosition({
      x: dx * strength,
      y: dy * strength
    });
  };

  const handleMouseLeave = () => {
    setPosition({ x: 0, y: 0 });
  };

  return (
    <motion.div
      ref={ref}
      animate={{ x: position.x, y: position.y }}
      transition={{ type: "spring", stiffness: 200, damping: 15 }}
      onMouseMove={handleMouseMove}
      onMouseLeave={handleMouseLeave}
    >
      {children}
    </motion.div>
  );
};
```

### Scroll Animations

#### Parallax Layer
```js
const ParallaxLayer = ({ children, speed = 0.5 }) => {
  const [scrollY, setScrollY] = useState(0);

  useEffect(() => {
    const handleScroll = () => setScrollY(window.scrollY);
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  }, []);

  return (
    <motion.div
      style={{ y: scrollY * speed }}
    >
      {children}
    </motion.div>
  );
};
```

#### Scroll-Triggered Reveal
```js
const ScrollReveal = ({ children, delay = 0 }) => {
  const ref = useRef(null);
  const isInView = useInView(ref, { once: true, margin: "-100px" });

  return (
    <motion.div
      ref={ref}
      initial={{ opacity: 0, y: 50, filter: "blur(10px)" }}
      animate={isInView ? { opacity: 1, y: 0, filter: "blur(0px)" } : {}}
      transition={{ duration: 0.8, delay, ease: [0.16, 1, 0.3, 1] }}
    >
      {children}
    </motion.div>
  );
};
```

### Text Animations

#### Character Reveal
```js
const CharReveal = ({ text }) => {
  return (
    <motion.div>
      {text.split('').map((char, i) => (
        <motion.span
          key={i}
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ delay: i * 0.03, duration: 0.5 }}
        >
          {char}
        </motion.span>
      ))}
    </motion.div>
  );
};
```

#### Gradient Text Sweep
```js
const GradientText = ({ children }) => {
  return (
    <motion.span
      className="bg-gradient-to-r from-white via-blue-200 to-white bg-clip-text text-transparent"
      animate={{
        backgroundPosition: ["0% 50%", "100% 50%", "0% 50%"],
      }}
      transition={{ duration: 3, repeat: Infinity, ease: "linear" }}
      style={{ backgroundSize: "200% 200%" }}
    >
      {children}
    </motion.span>
  );
};
```

### Hover Effects

#### Scale & Glow
```js
const HoverCard = ({ children }) => {
  return (
    <motion.div
      whileHover={{ 
        scale: 1.05,
        boxShadow: "0 0 30px rgba(59, 130, 246, 0.3)"
      }}
      transition={{ type: "spring", stiffness: 300, damping: 20 }}
    >
      {children}
    </motion.div>
  );
};
```

#### Border Gradient on Hover
```css
.hover-border {
  position: relative;
  background: #0a0a0a;
  border: 1px solid rgba(255,255,255,0.06);
  transition: all 0.3s ease;
}

.hover-border::before {
  content: "";
  position: absolute;
  inset: -1px;
  border-radius: inherit;
  padding: 1px;
  background: linear-gradient(135deg, #3b82f6, #8b5cf6, #06b6d4);
  -webkit-mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.hover-border:hover::before {
  opacity: 1;
}
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
