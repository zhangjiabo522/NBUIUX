# NBUIUX - 高端UI/UX设计技能

<div align="center">

![NBUIUX Banner](https://img.shields.io/badge/NBUIUX-Premium%20UI%2FUX-000000?style=for-the-badge&logoColor=white)
![Version](https://img.shields.io/badge/version-5.0.0-000000?style=for-the-badge&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-000000?style=for-the-badge&logoColor=white)

**创建看起来价值5万美元以上的高端UI/UX设计**

拒绝廉价AI风格渐变，只做专业级视觉效果

[English](#english-version) | [中文文档](#中文版本)

</div>

---

## 📖 中文版本

### 🎯 什么是NBUIUX？

NBUIUX是一个OpenCode/Claude技能，帮助你创建**高端级**UI/UX设计。每个设计都是电影级别的、精致的、绝对惊艳的。

### ✨ 核心特性

| 特性 | 描述 |
|------|------|
| 🎬 **35+高端模板** | 从电影级Hero区域到创意作品集 |
| 💎 **液态玻璃效果** | 多层模糊、微妙边框、内发光 |
| 🎮 **3D交互** | 透视变换、视差效果、鼠标跟踪 |
| 🎨 **精致配色系统** | 拒绝廉价AI渐变，只用精心策划的配色 |
| ✨ **微交互** | 悬停状态、滚动动画、光标效果 |
| 📝 **字体层次** | 正确的字体比例和对比度 |
| 🖼️ **纹理叠加** | 噪点、颗粒、微妙图案增加深度 |

---

### 📦 安装方法

#### 方法一：OpenCode安装（推荐）

```bash
# 克隆到OpenCode技能目录
git clone git@github.com:zhangjiabo522/NBUIUX.git ~/.config/opencode/skills/nbuiux
```

#### 方法二：Claude Desktop安装

```bash
# 1. 找到Claude Desktop的技能目录
# macOS:
mkdir -p ~/Library/Application\ Support/Claude/skills/nbuiux

# Windows:
mkdir -p %APPDATA%\Claude\skills\nbuiux

# Linux:
mkdir -p ~/.config/claude/skills/nbuiux

# 2. 克隆仓库
git clone git@github.com:zhangjiabo522/NBUIUX.git ~/Library/Application\ Support/Claude/skills/nbuiux

# 3. 或者手动复制SKILL.md文件到上述目录
```

#### 方法三：手动安装

```bash
# 1. 创建技能目录
mkdir -p ~/.config/opencode/skills/nbuiux

# 2. 下载SKILL.md文件
curl -o ~/.config/opencode/skills/nbuiux/SKILL.md https://raw.githubusercontent.com/zhangjiabo522/NBUIUX/main/SKILL.md

# 3. 下载README.md文件（可选）
curl -o ~/.config/opencode/skills/nbuiux/README.md https://raw.githubusercontent.com/zhangjiabo522/NBUIUX/main/README.md
```

---

### 🚀 使用方法

#### 在OpenCode中使用

```
# 加载技能
skill({ name: "nbuiux" })

# 然后描述你的项目
"我需要一个AI创业公司的高端landing page"
"创建一个奢侈品牌网站"
"设计一个NFT市场"
```

#### 在Claude Desktop中使用

1. 将SKILL.md文件复制到Claude Desktop的技能目录
2. 重启Claude Desktop
3. 在对话中告诉Claude你的项目需求

---

### 🎨 模板分类

#### 1. 电影级 & 高端 (模板 2, 3, 6, 7, 14, 15, 20, 21)
- 全屏视频背景
- 液态玻璃导航
- 平滑滚动动画
- **适用：** 奢侈品牌、娱乐、高端产品

#### 2. 创意作品集 (模板 1, 10, 25)
- 独特布局
- 交互元素
- 惊艳动画
- **适用：** 设计师、艺术家、代理机构

#### 3. SaaS & 科技 (模板 5, 16, 27, 30)
- 简洁现代设计
- 清晰价值主张
- 专业美学
- **适用：** 创业公司、软件公司

#### 4. Web3 & NFT (模板 18, 24)
- 深色沉浸主题
- 视频展示
- 未来感
- **适用：** 区块链、加密项目

#### 5. 代理机构 & 工作室 (模板 11, 12, 22, 25)
- 大胆字体
- 案例研究布局
- 团队展示
- **适用：** 创意代理机构、咨询公司

---

### 🚫 设计规则

#### ❌ 绝对不要做（AI廉价效果）：

- 简单的2-3色线性渐变
- 高亮霓虹色 (#00ff00, #ff00ff等)
- 彩虹渐变
- 过度饱和的颜色
- 通用的"科技"蓝紫渐变
- 扁平、无生气的背景
- 基础阴影
- 千篇一律的布局

#### ✅ 必须做（高端品质）：

- 5-10+精心策划的复杂配色系统
- 多停止点、透明度变化的精致渐变
- 纹理叠加（噪点、颗粒、微妙图案）
- 深度和层次（视差、毛玻璃、阴影）
- 微交互（悬停状态、滚动动画、光标效果）
- 有对比度和节奏的字体层次
- 慷慨、有意的白色空间
- 流畅、有目的的动画设计

---

### 🎨 配色系统

#### 超级深色（电影级）
```css
:root {
  --bg: #000000;
  --surface: #0a0a0a;
  --elevated: #111111;
  --border: rgba(255, 255, 255, 0.06);
  --text: #f5f5f5;
  --text-muted: #666666;
}
```

#### 暖色深色（精致）
```css
:root {
  --bg: #0c0a09;
  --surface: #1c1917;
  --elevated: #292524;
  --border: rgba(255, 255, 255, 0.08);
  --text: #fafaf9;
  --text-muted: #a8a29e;
  --accent: #c8a882;
}
```

#### 冷色深色（技术感）
```css
:root {
  --bg: #0a0a0f;
  --surface: #12121a;
  --elevated: #1a1a25;
  --border: rgba(255, 255, 255, 0.06);
  --text: #f0f0f5;
  --text-muted: #8888aa;
  --accent: #8ba4b8;
}
```

---

### 💎 液态玻璃效果

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

### 📦 技术栈

| 技术 | 用途 |
|------|------|
| React 18 | 框架 |
| TypeScript | 类型安全 |
| Vite | 构建工具 |
| Tailwind CSS 3.4+ | 样式 |
| Framer Motion | 动画 |
| GSAP | 复杂滚动动画 |
| Lucide React | 图标 |
| HLS.js | 视频流 |
| Spline | 3D场景 |

---

### ✨ 动画模式

#### FadeUp（淡入上移）
```js
const fadeUp = {
  hidden: { opacity: 0, y: 20 },
  visible: { opacity: 1, y: 0 }
}
```

#### BlurFadeUp（模糊淡入）
```js
const blurFadeUp = {
  hidden: { opacity: 0, filter: 'blur(20px)', y: 40 },
  visible: { opacity: 1, filter: 'blur(0)', y: 0 }
}
```

#### SlideReveal（滑动揭示）
```js
const slideReveal = {
  hidden: { translateY: '110%' },
  visible: { translateY: '0' }
}
```

#### 自定义缓动
```js
transition: { 
  duration: 0.8, 
  ease: [0.16, 1, 0.3, 1] // Expo ease out
}
```

---

### 📁 项目结构

```
nbuiux/
├── SKILL.md          # 主技能文件
├── README.md         # 本文件
└── examples/         # 示例项目（即将推出）
```

---

### 🤝 贡献指南

欢迎贡献！请随时提交Pull Request。

1. Fork仓库
2. 创建特性分支 (`git checkout -b feature/amazing-feature`)
3. 提交更改 (`git commit -m 'Add amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 开启Pull Request

---

### 📄 许可证

本项目采用MIT许可证 - 详见[LICENSE](LICENSE)文件

---

### 🙏 致谢

- 受高端设计工作室和代理机构启发
- 为追求最佳的开发者而生
- 用❤️为设计社区而建

---

<div align="center">

**[GitHub](https://github.com/zhangjiabo522/NBUIUX)** • **[Issues](https://github.com/zhangjiabo522/NBUIUX/issues)** • **[Discussions](https://github.com/zhangjiabo522/NBUIUX/discussions)**

</div>

---

<a name="english-version"></a>

## 📖 English Version

### 🎯 What is NBUIUX?

NBUIUX is an OpenCode/Claude skill that helps you create **premium-grade** UI/UX designs. Every design is cinematic, sophisticated, and absolutely stunning.

### ✨ Key Features

| Feature | Description |
|---------|-------------|
| 🎬 **35+ Premium Templates** | From cinematic hero sections to creative portfolios |
| 💎 **Liquid Glass Effects** | Multi-layer blur, subtle borders, inner glows |
| 🎮 **3D Interactions** | Perspective transforms, parallax, mouse tracking |
| 🎨 **Sophisticated Color Systems** | No cheap AI gradients, only curated palettes |
| ✨ **Micro-interactions** | Hover states, scroll animations, cursor effects |
| 📝 **Typography Hierarchy** | Proper type scale with contrast and rhythm |
| 🖼️ **Texture Overlays** | Noise, grain, subtle patterns for depth |

---

### 📦 Installation

#### Method 1: OpenCode (Recommended)

```bash
# Clone to OpenCode skills directory
git clone git@github.com:zhangjiabo522/NBUIUX.git ~/.config/opencode/skills/nbuiux
```

#### Method 2: Claude Desktop

```bash
# 1. Find Claude Desktop skills directory
# macOS:
mkdir -p ~/Library/Application\ Support/Claude/skills/nbuiux

# Windows:
mkdir -p %APPDATA%\Claude\skills\nbuiux

# Linux:
mkdir -p ~/.config/claude/skills/nbuiux

# 2. Clone repository
git clone git@github.com:zhangjiabo522/NBUIUX.git ~/Library/Application\ Support/Claude/skills/nbuiux

# 3. Or manually copy SKILL.md to the directory above
```

#### Method 3: Manual Installation

```bash
# 1. Create skills directory
mkdir -p ~/.config/opencode/skills/nbuiux

# 2. Download SKILL.md
curl -o ~/.config/opencode/skills/nbuiux/SKILL.md https://raw.githubusercontent.com/zhangjiabo522/NBUIUX/main/SKILL.md

# 3. Download README.md (optional)
curl -o ~/.config/opencode/skills/nbuiux/README.md https://raw.githubusercontent.com/zhangjiabo522/NBUIUX/main/README.md
```

---

### 🚀 Usage

#### In OpenCode

```
# Load the skill
skill({ name: "nbuiux" })

# Then describe your project
"I need a premium landing page for my AI startup"
"Create a luxury brand website"
"Design an NFT marketplace"
```

#### In Claude Desktop

1. Copy SKILL.md to Claude Desktop skills directory
2. Restart Claude Desktop
3. Tell Claude about your project in the conversation

---

### 🎨 Template Categories

#### 1. Cinematic & Premium (Templates 2, 3, 6, 7, 14, 15, 20, 21)
- Full-screen video backgrounds
- Liquid glass navigation
- Smooth scroll animations
- **Best for:** Luxury brands, entertainment, premium products

#### 2. Creative Portfolio (Templates 1, 10, 25)
- Unique layouts
- Interactive elements
- Show-stopping animations
- **Best for:** Designers, artists, agencies

#### 3. SaaS & Tech (Templates 5, 16, 27, 30)
- Clean, modern design
- Clear value proposition
- Professional aesthetics
- **Best for:** Startups, software companies

#### 4. Web3 & NFT (Templates 18, 24)
- Dark, immersive themes
- Video showcases
- Futuristic feel
- **Best for:** Blockchain, crypto projects

#### 5. Agency & Studio (Templates 11, 12, 22, 25)
- Bold typography
- Case study layouts
- Team showcases
- **Best for:** Creative agencies, consultancies

---

### 🚫 Design Rules

#### ❌ NEVER DO (AI-looking cheap effects):
- Simple linear-gradient with 2-3 colors
- Bright neon colors (#00ff00, #ff00ff, etc.)
- Rainbow gradients
- Overly saturated colors
- Generic "tech" blue/purple gradients
- Flat, lifeless backgrounds
- Basic box shadows
- Cookie-cutter layouts

#### ✅ ALWAYS DO (Premium quality):
- Complex color systems with 5-10+ carefully curated colors
- Sophisticated gradients with multiple stops, opacity variations
- Texture overlays (noise, grain, subtle patterns)
- Depth and layers (parallax, glassmorphism, shadows)
- Micro-interactions (hover states, scroll animations, cursor effects)
- Typography hierarchy with contrast and rhythm
- White space - generous, intentional spacing
- Motion design - smooth, purposeful animations

---

### 🎨 Color System

#### Ultra Dark (Cinematic)
```css
:root {
  --bg: #000000;
  --surface: #0a0a0a;
  --elevated: #111111;
  --border: rgba(255, 255, 255, 0.06);
  --text: #f5f5f5;
  --text-muted: #666666;
}
```

#### Warm Dark (Sophisticated)
```css
:root {
  --bg: #0c0a09;
  --surface: #1c1917;
  --elevated: #292524;
  --border: rgba(255, 255, 255, 0.08);
  --text: #fafaf9;
  --text-muted: #a8a29e;
  --accent: #c8a882;
}
```

#### Cool Dark (Technical)
```css
:root {
  --bg: #0a0a0f;
  --surface: #12121a;
  --elevated: #1a1a25;
  --border: rgba(255, 255, 255, 0.06);
  --text: #f0f0f5;
  --text-muted: #8888aa;
  --accent: #8ba4b8;
}
```

---

### 💎 Liquid Glass Effect

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

### 📦 Tech Stack

| Technology | Purpose |
|------------|---------|
| React 18 | Framework |
| TypeScript | Type safety |
| Vite | Build tool |
| Tailwind CSS 3.4+ | Styling |
| Framer Motion | Animations |
| GSAP | Complex scroll animations |
| Lucide React | Icons |
| HLS.js | Video streaming |
| Spline | 3D scenes |

---

### ✨ Animation Patterns

#### FadeUp
```js
const fadeUp = {
  hidden: { opacity: 0, y: 20 },
  visible: { opacity: 1, y: 0 }
}
```

#### BlurFadeUp
```js
const blurFadeUp = {
  hidden: { opacity: 0, filter: 'blur(20px)', y: 40 },
  visible: { opacity: 1, filter: 'blur(0)', y: 0 }
}
```

#### SlideReveal
```js
const slideReveal = {
  hidden: { translateY: '110%' },
  visible: { translateY: '0' }
}
```

#### Custom Easing
```js
transition: { 
  duration: 0.8, 
  ease: [0.16, 1, 0.3, 1] // Expo ease out
}
```

---

### 📁 Project Structure

```
nbuiux/
├── SKILL.md          # Main skill file
├── README.md         # This file
└── examples/         # Example projects (coming soon)
```

---

### 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

### 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### 🙏 Acknowledgments

- Inspired by premium design studios and agencies
- Built for developers who demand the best
- Created with ❤️ for the design community

---

<div align="center">

**[GitHub](https://github.com/zhangjiabo522/NBUIUX)** • **[Issues](https://github.com/zhangjiabo522/NBUIUX/issues)** • **[Discussions](https://github.com/zhangjiabo522/NBUIUX/discussions)**

</div>
