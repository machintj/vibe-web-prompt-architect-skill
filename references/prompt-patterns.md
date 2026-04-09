# Prompt Patterns

本文件提供可直接复用的网页 Prompt 模式。根据任务类型选一个最贴近的模板，再做轻量改写。

## 1. Hero Only

适用于：
- 首屏展示
- 品牌首页头图
- 单一强叙事页面

模板：

```md
Create a premium hero section for "[brand_name]" using React + Vite + TypeScript + Tailwind CSS.

Creative Direction
- Aesthetic: [editorial / cinematic / minimal / glassmorphism / luxury]
- Mood: [premium / calm / futuristic / poetic / bold]
- Avoid: [generic SaaS look / extra UI libraries / random gradients]

Design System
- Display font: [font]
- Body font: [font]
- Accent font: [font]
- Background: [color]
- Foreground: [color]
- Primary: [color]
- Muted: [color]

Layout
- Full viewport height
- Relative wrapper with overflow-hidden
- Background layer z-0
- Overlay layer z-10
- Content layer z-20
- Max width: [value]
- Padding: [value]

Navbar
- Logo: [text/icon]
- Links: [items]
- CTA: [label]

Hero Content
- Badge: [text]
- Headline: "[headline]"
- Subtitle: "[subcopy]"
- Primary CTA: [text]
- Secondary CTA: [text]

Motion
- Badge: [animation]
- Heading: [animation]
- Subtitle: [animation]
- CTA group: [animation]

Responsive
- Collapse navbar on mobile
- Reduce heading size on smaller screens
- Keep CTA readable and wrapped if needed

Output
- Provide complete component code and required CSS.
```

## 2. SaaS Landing

适用于：
- AI 产品
- 工具型产品
- B2B 官网

模板：

```md
Build a modern SaaS landing page for "[brand_name]" using React + TypeScript + Tailwind CSS.

The visual system should feel [clean / premium / dark / futuristic / sharp], with a restrained and product-focused hierarchy.

Sections
- Navbar
- Hero
- Social proof
- Feature highlights
- CTA footer

Design System
- Fonts: [display/body]
- Tokens: [HSL or hex]
- Accent color: [color]
- Border style: [soft / crisp / glass]

Hero
- Headline: "[headline]"
- Subtitle: "[subcopy]"
- CTA buttons: [primary/secondary]
- Proof row: [logos / ratings / metrics]

Feature Section
- Use 3-4 tightly designed feature blocks
- Avoid generic repeated cards unless they have a clear visual rhythm
- Add one signature visual element: [glow / panel / dashboard crop / floating badge]

Motion
- Subtle fade-up and staggered reveal
- Hover polish on CTAs and cards
- Keep animations product-grade, not playful

Negative Constraints
- No template-like icon-card overload
- No random gradients
- No visual clutter above the fold
```

## 3. Portfolio / Agency

适用于：
- 创意工作室
- 设计师作品集
- 视频/品牌 Agency

模板：

```md
Create a portfolio-style landing page for "[brand_name]" using React + TypeScript + Tailwind CSS.

Creative Direction
- Aesthetic: [editorial / cinematic / artistic / luxury minimal]
- Typography should be the hero of the page.
- The page must feel authored, not corporate.

Fonts
- Display: [serif / experimental font]
- Body: [neutral sans]
- Accent: [italic serif / script]

Structure
- Minimal navbar
- Statement-driven hero
- Short positioning paragraph
- Selected work / credibility strip
- CTA

Visual Rules
- Strong whitespace
- Tight color discipline
- One signature motif: [video / grain / marquee / glass badge / oversized typography]
- Avoid feature-grid SaaS language

Motion
- Slow, elegant, restrained
- Fade, rise, drift, or staggered text only
- No bouncy interactions
```

## 4. Glassmorphism / Liquid Glass

适用于：
- 高感知“高级感”
- 浮层、玻璃 UI、卡片层次

模板：

```md
Build a high-end landing page with a liquid glass aesthetic using React + Tailwind CSS.

Glass System
- Define a reusable `.liquid-glass` class
- Use subtle transparency, backdrop blur, inner highlight, and refined border treatment
- Keep glass usage selective: navbar, badge, floating card, key panel

Background
- Dark or tinted base
- Add one glow source or ambient media layer
- Ensure readability with gradients or contrast zones

Rules
- Do not overuse glass on every component
- Use glass only where depth or emphasis is needed
- Keep typography crisp to balance soft surfaces
```

## 5. Video Background Hero

适用于：
- 情绪化首屏
- 电影感产品页
- 高沉浸品牌页面

模板：

```md
Create a fullscreen hero section with a looping background video.

Video Requirements
- Source: [URL]
- Behavior: autoplay, muted, loop, playsInline
- Object fit: cover
- Layer behind all content
- Add [none / bottom fade / left gradient / dark overlay] depending on readability needs

If using custom loop behavior
- Monitor currentTime and duration
- Fade in at start
- Fade out before the end
- Reset and replay cleanly
- Clean up listeners and animation frames on unmount

Foreground
- Keep text and CTA in a strong contrast zone
- Use minimal but intentional overlays
```

## 6. Monochrome Minimal

适用于：
- 极简品牌
- 内容平台
- 高端产品展示

模板：

```md
Create a monochrome landing page using only black, white, and grayscale values.

Rules
- No accent colors unless explicitly specified
- Typography hierarchy must carry the design
- Use spacing, contrast, and motion instead of decorative color
- Keep the interface minimal but not empty

Components
- Minimal navbar
- One dominant headline
- One supporting paragraph
- One strong CTA
- One subtle trust element

Motion
- Fade-up
- Blur-in
- Soft stagger
- No flashy effects
```

## 7. Quick Compression Formula

当用户输入非常模糊时，用这条公式先补全：

`品牌气质 + 设计系统 + 页面骨架 + 背景层 + 关键组件 + 动效协议 + 工程边界 + 禁止项`

例子：

```md
Create a cinematic dark hero for "[brand]" using React + TypeScript + Tailwind CSS.

Use [display font] for headlines and [body font] for interface copy.
The page should have a fullscreen video background, a transparent navbar, one strong headline, one subtitle, one primary CTA, and one proof element.
Define exact colors, spacing, z-index layers, and motion timing.
Avoid generic startup UI patterns and unnecessary sections.
Provide full runnable code.
```
