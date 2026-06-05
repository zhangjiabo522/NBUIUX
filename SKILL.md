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

## 🎯 TEMPLATE CATEGORIES & PROMPT SYSTEM

### 📁 Prompt File Location
All detailed prompts are stored in `prompts.md` file in the same directory as this SKILL.md file.

**To use:** Read the `prompts.md` file and find the corresponding template number based on user requirements.

---

### 📋 Template Index

| 编号 | 类型 | 示例 | 关键特性 |
|------|------|------|----------|
| 1 | 3D 创作者作品集 | Jack — 3D Creator | 磁性鼠标跟随、滚动驱动动画 |
| 2-3 | 创意工作室 | Prisma（两个版本） | 液态玻璃、视频背景 |
| 4 | 角色手办轮播 | TOONHUB | 3D轮播、交互式卡片 |
| 5 | 太空旅行落地页 | 双视频循环 | 双视频循环 + 液态玻璃 |
| 6 | 电影级 Hero | 视频淡入淡出循环 | 视频淡入淡出循环 |
| 7 | VEX 品牌落地页 | 视频 + 液态玻璃导航 | 视频 + 液态玻璃导航 |
| 8 | mėntality 心理健康 | 视频 + 搜索药丸组件 | 搜索药丸组件 |
| 9 | SkyElite 私人飞机 | 汉堡菜单 + 重叠标题 | 汉堡菜单 + 重叠标题 |
| 10 | Mainframe 创意机构 | 鼠标擦洗视频 + 打字机 | 鼠标擦洗视频 + 打字机 |
| 11-12 | Axion Studio | shader 背景 + 特效 | shader 背景 + 特效 |
| 13 | Mainframe 打字机 | 服务选择药丸 + 条件反馈 | 服务选择药丸 + 条件反馈 |
| 14 | Asme 新闻通讯 | 视频淡入淡出循环 + 邮箱捕获 | 视频淡入淡出循环 + 邮箱捕获 |
| 15 | Asme 完整 5 节页面 | 关于 + 特色视频 + 服务卡片 | 关于 + 特色视频 + 服务卡片 |
| 16 | Asme HLS 视频 | hls.js + 邮箱捕获 + 打字机占位符 | hls.js + 邮箱捕获 + 打字机占位符 |
| 17 | Michael Smith 作品集 | 加载屏幕 + GSAP + 视差画廊 | 加载屏幕 + GSAP + 视差画廊 |
| 18 | Orbis.Nft | 太空 NFT 市场 + 液态玻璃卡片 | 太空 NFT 市场 + 液态玻璃卡片 |
| 19 | VaultShield 密码管理器 | 图标内联标题 + 移动端抽屉 | 图标内联标题 + 移动端抽屉 |
| 20 | 电影/流媒体 Hero | 底部模糊遮罩 + 移动端菜单 | 底部模糊遮罩 + 移动端菜单 |
| 21 | 简单的视频 Hero | 最小版本 | 最小版本 |
| 22 | LinkFlow | 回旋镖视频帧捕获 + 移动端菜单 | 回旋镖视频帧捕获 + 移动端菜单 |
| 23 | Mindloop 内容平台 | HLS 视频 + 滚动驱动文字动画 | HLS 视频 + 滚动驱动文字动画 |
| 24 | RIVR DeFi 仪表盘 | 自定义字体 + 底部卡片 | 自定义字体 + 底部卡片 |
| 25 | Viktor Oddy 工作室 | 无限滚动 + 鼠标轨迹 + 轮播 | 无限滚动 + 鼠标轨迹 + 轮播 |
| 26 | CodeNest | HLS + 网格线 + 液态玻璃卡片 | HLS + 网格线 + 液态玻璃卡片 |
| 27 | Power AI | 大标题渐变 + Logo 跑马灯 | 大标题渐变 + Logo 跑马灯 |
| 28 | Bloom | 双面板 + 液态玻璃层级 | 双面板 + 液态玻璃层级 |
| 29 | MicroVisuals | 帧捕获回旋镖 + 视差鼠标 | 帧捕获回旋镖 + 视差鼠标 |
| 30 | HLS 视频背景（简略） | 最小说明 | 最小说明 |
| 31 | Fearless Vision | 堆叠标题 + 折叠菜单 | 堆叠标题 + 折叠菜单 |
| 32 | Wanderful 旅行 | GSAP 视差 + 回旋镖视频 | GSAP 视差 + 回旋镖视频 |
| 33 | SENTINEL AI | Spline 3D 背景 + shadcn | Spline 3D 背景 + shadcn |
| 34 | DesignPro | ShinyText 渐变扫光 | ShinyText 渐变扫光 |
| 35 | 假肢品牌 | 最小 Hero + 双药丸导航 | 最小 Hero + 双药丸导航 |

---

### 🔍 How to Select Template

**Step 1: Identify the category**

| 需求类型 | 推荐模板 |
|----------|----------|
| 3D作品集/个人品牌 | 1, 10, 17, 25 |
| 创意工作室/代理机构 | 2, 3, 11, 12, 22 |
| 电影级/高端品牌 | 5, 6, 7, 14, 15, 20, 21 |
| SaaS/科技产品 | 16, 26, 27, 30 |
| NFT/Web3 | 18, 24 |
| 教育/课程 | 26, 34 |
| 旅行/生活方式 | 5, 32 |
| 安全/企业 | 19, 33 |
| 内容平台/新闻通讯 | 8, 14, 23 |
| 电商/产品展示 | 4, 31, 35 |

**Step 2: Read the corresponding prompt**

```
Read prompts.md and find template number [X]
```

**Step 3: Generate code based on the prompt**

Apply NBUIUX design rules (no cheap AI gradients, premium quality only)

---

### 🎨 Category Details

#### 1. 创意作品集 (Templates 1, 10, 17, 25)
- 独特布局
- 交互元素
- 惊艳动画
- **适用：** 设计师、艺术家、代理机构

#### 2. 创意工作室 (Templates 2, 3, 11, 12, 22)
- 大胆字体
- 案例研究布局
- 团队展示
- **适用：** 创意代理机构、咨询公司

#### 3. 电影级 & 高端 (Templates 5, 6, 7, 14, 15, 20, 21)
- 全屏视频背景
- 液态玻璃导航
- 平滑滚动动画
- **适用：** 奢侈品牌、娱乐、高端产品

#### 4. SaaS & 科技 (Templates 16, 26, 27, 30)
- 简洁现代设计
- 清晰价值主张
- 专业美学
- **适用：** 创业公司、软件公司

#### 5. Web3 & NFT (Templates 18, 24)
- 深色沉浸主题
- 视频展示
- 未来感
- **适用：** 区块链、加密项目

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
