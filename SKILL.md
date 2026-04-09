---
name: vibe-web-prompt-architect
description: 将模糊的网页创意、Hero 区块或 Landing Page 需求，转写为高质量、低歧义、可直接生成 React/TypeScript/Tailwind 页面代码的结构化 Prompt。适用于品牌首屏、SaaS 官网、作品集、Agency 页面、AI 产品页、视频背景页面、glassmorphism 页面等场景。触发于用户要求“做一个高级网页”“生成高质量网页 Prompt”“提炼 vibe coding 网页方法论”“写 Hero/Landing Page 提示词模板”等任务。
---

# Vibe Web Prompt Architect

把“想做一个高级网页”的模糊需求，转成一份前端生成模型可以稳定执行的结构化 Prompt。

## 何时使用

在以下任务中使用本 Skill：

- 用户要生成网页、Hero、Landing Page、Portfolio、Agency 页面
- 用户只有风格方向，没有完整规格
- 用户想沉淀网页类 vibe coding 提示词方法论
- 用户要求页面更高级、更有设计感、更少模板味
- 用户想要一套可复用的网页 Prompt 模板

以下情况不要优先使用本 Skill：

- 用户已经给了完整 Figma 和精确标注
- 用户只是在修现有组件 bug
- 用户只需要改一段文案
- 用户明确要求只做工程实现，不需要 Prompt 抽象

## 核心目标

输出一份结构化网页 Prompt，使生成结果具备：

- 明确的品牌气质
- 一致的设计系统
- 稳定的页面骨架
- 清晰的视觉分层
- 有节奏的动效
- 明确的工程边界
- 较低的跑偏概率
- 较强的可落地性

## 工作原则

### 1. 先定气质，再定页面

不要直接开始写按钮、卡片、导航。

先用一句话定义：

- 页面类型
- 品牌名
- aesthetic
- mood
- density

例如：

`Create a cinematic, premium single-page hero for "Aethera" with an editorial tone and airy composition.`

### 2. 抽象审美必须翻译成工程约束

像“高级”“未来感”“玻璃质感”“品牌化”这类词，必须落到可执行字段：

- 字体
- 颜色
- token
- 布局
- z-index
- 背景媒体
- overlay
- 动画
- 依赖库
- 文件位置
- 响应式规则

### 3. 只精确关键节点

重点约束这些部分：

- Hero headline
- 背景层
- CTA
- Navbar
- badge / floating card / proof row / marquee
- 关键光效、玻璃、边框、噪点、阴影

其他区域保持适度自由，不要把整个页面写成像素级规格书。

### 4. 必须包含负约束

高质量 Prompt 不只定义“要什么”，还要定义“不要什么”。

常见负约束：

- 不要默认 SaaS 模板感
- 不要无意义 feature card 堆砌
- 不要随机渐变
- 不要未指定 UI 库
- 不要过度装饰
- 不要 placeholder 破坏真实感
- 不要色彩漂移

### 5. 高级感来自“层”，不是“组件数量”

优先定义层级：

- Background media layer
- Overlay / readability layer
- Main content layer
- Floating emphasis layer

并明确各层职责。

## 快速执行协议

收到网页生成类任务后，按以下顺序构造输出：

1. 一句话重写创意方向
2. 建立设计系统
3. 定义页面骨架
4. 定义背景与分层
5. 定义关键组件
6. 定义动效协议
7. 定义响应式行为
8. 定义工程约束
9. 加入负约束
10. 输出最终 Prompt

如果用户需要多个方向，再输出 2-3 个变体 Prompt。

## 标准执行流程

### Step 1. 识别页面类型

先判断属于哪类：

- Hero only
- Single-page landing
- Multi-section marketing page
- Portfolio
- Agency
- SaaS landing
- Brand campaign
- Interactive section

如果用户没有明确指定，默认从以下结构开始：

- Navbar
- Hero
- One supporting module
- CTA ending

### Step 2. 写一句创意总述

格式：

`Create a [page type] for [brand] with a [aesthetic] aesthetic, [mood] tone, and [density] composition.`

### Step 3. 建立设计系统

至少明确：

#### Typography
- Display font
- Body font
- Accent font
- 字体导入位置
- 字体用途分工

#### Color System
- Background
- Foreground
- Primary
- Secondary
- Muted
- Border
- Accent
- 是否使用 HSL token / CSS variables / Tailwind theme

#### Style Rules
- 圆角风格：sharp / soft / pill / mixed
- 边框风格：none / subtle / crisp / glass edge
- 阴影风格：soft ambient / hard elevation / none
- 是否允许 glow / gradients / blur / glass

### Step 4. 定义页面骨架

必须明确页面有哪些模块。

最常见骨架：

- Navbar
- Hero content
- CTA group
- Badge / proof / stats / floating card
- Optional feature strip / about / footer CTA

如果是单屏首屏，明确：

- 100vh
- no scroll
- hero-only

### Step 5. 定义背景与分层

必须明确：

- 背景类型：video / image / 3D / gradients / glow / solid
- 来源：URL / asset / generated effect
- 行为：loop / autoplay / muted / HLS / static
- object-fit：cover / contain
- 是否需要 overlay
- 是否需要可读性渐变
- 是否需要顶部/底部 fade
- 是否需要中心 glow 或环境 blur

推荐层级：

- Background media: z-0
- Overlay / glow / gradients: z-10
- Main UI and content: z-20
- Floating emphasis details: z-30

### Step 6. 定义关键组件

至少单独定义以下内容。

#### Navbar
- Logo 形式
- Nav links
- CTA
- 是否固定 / 浮动 / 透明
- 移动端行为

#### Badge / Eyebrow
- 文案
- 结构
- 是否 glass / outline / filled
- 是否有 icon

#### Headline
- 文案
- 分行方式
- 强调词
- 字号区间
- 行高
- tracking
- 字重
- 颜色层级

#### Subtitle
- 文案
- max-width
- 字号
- 行高
- 透明度 / 颜色

#### CTA Group
- primary button
- secondary button
- icon
- hover 行为
- 间距与排列方式

#### Supporting Details
根据页面类型补充：
- review pill
- social proof row
- logo marquee
- floating card
- metric chips
- glass panel
- calculator area
- split media block

### Step 7. 定义动效协议

必须回答：

- 用什么：motion/react / framer-motion / GSAP / CSS keyframes
- 谁会动：badge / headline / subtitle / CTA / cards / logos
- 怎么动：fade-up / blur-in / split-text / scale / drift / parallax
- 时间：duration / delay / stagger
- hover：opacity / scale / translate / shadow
- 如果有背景视频，如何 loop 和 cleanup

### Step 8. 定义响应式行为

必须明确：

- navbar 在移动端如何处理
- 标题在移动端如何缩放
- split layout 是否 stack
- CTA 是否 wrap
- 哪些装饰元素只在 desktop 显示
- padding 与 spacing 如何收缩

### Step 9. 定义工程约束

可选约束包括：

- Framework: React + Vite / Next.js
- Language: TypeScript strict
- Styling: Tailwind CSS
- Animation: motion/react / framer-motion / CSS only
- Icons: lucide-react
- Video: native video / hls.js
- UI: shadcn/ui allowed or forbidden
- 文件位置：fonts.css / index.css / theme.css
- 是否允许第三方 UI 库
- 是否要求 production-ready
- 是否要求 no `any`

### Step 10. 定义负约束

常用模板：

- Do not make it look like a generic startup template.
- Avoid repetitive feature-card grids above the fold.
- Do not introduce colors outside the specified palette.
- Do not use extra UI libraries unless explicitly requested.
- Avoid overly playful motion unless the brand calls for it.
- Do not clutter the hero with unnecessary decorative elements.

### Step 11. 定义输出要求

明确模型要输出什么：

- 完整代码
- 必要依赖
- 必要 CSS
- 主题 token
- 不要伪代码
- 保持可运行
- 保持严格类型

## 输出格式

默认按以下格式输出结果：

### 1. 规律摘要
提炼任务对应的核心设计规律，3-6 条即可。

### 2. 结构化拆解
- Creative Direction
- Design System
- Page Structure
- Layering
- Motion System
- Responsive Rules
- Engineering Constraints
- Negative Constraints

### 3. Final Prompt
给出一份可以直接复制使用的完整 Prompt。

### 4. Optional Variants
如果用户需要，再补：
- Variant A: 更极简
- Variant B: 更品牌化
- Variant C: 更产品化

## Prompt 组装公式

`品牌气质 + 技术栈 + 设计系统 + 页面骨架 + 背景与分层 + 关键组件约束 + 动效协议 + 响应式规则 + 工程边界 + 负约束 + 输出要求`

## 基础模板

```md
Create a high-quality [page_type] for "[brand_name]" using [tech_stack].

Creative Direction
- Aesthetic: [editorial / cinematic / minimal / glassmorphism / luxury / monochrome]
- Mood: [calm / bold / futuristic / premium / poetic]
- Density: [airy / immersive / compact]
- Avoid: [generic SaaS UI / extra libraries / random gradients / visual clutter]

Design System
- Display font: [font]
- Body font: [font]
- Accent font: [font]
- Import fonts in [file path]
- Colors:
  - Background: [color]
  - Foreground: [color]
  - Primary: [color]
  - Secondary: [color]
  - Muted: [color]
  - Border: [color]

Page Structure
- Include: Navbar, Hero, CTA group, [supporting element]
- Layout: [hero-only / single-page / multi-section]
- Container: [max width]
- Padding: [value]

Background & Layering
- Background type: [video / image / 3D / glow / solid]
- Source: [URL if needed]
- Behavior: [autoplay / loop / muted / HLS / static]
- Layer order:
  - Background: z-0
  - Overlay/glow: z-10
  - Content: z-20

Components
- Navbar: [details]
- Badge: [details]
- Heading: "[headline]"
- Subtitle: "[subcopy]"
- Primary CTA: [text]
- Secondary CTA: [text]

Motion
- Use [animation system]
- Badge: [animation]
- Heading: [animation]
- Subtitle: [animation]
- CTA: [animation]
- Hover: [behavior]

Responsive
- Collapse navbar on mobile
- Scale heading down on smaller screens
- Stack split layouts on mobile
- Keep spacing balanced

Engineering Constraints
- Strict TypeScript
- [allowed / forbidden libraries]
- Include required CSS and dependencies
- Keep code production-ready

Negative Constraints
- Do not make it look templated
- Do not add unnecessary sections
- Do not use colors outside the defined palette

Output
- Provide complete runnable code
- Include required CSS/theme additions
- Do not return pseudocode
```

## 常见页面类型的偏好策略

### Hero Only
优先强调：
- headline
- CTA
- 背景媒体
- layer stack
- above-the-fold 质感

### SaaS Landing
优先强调：
- 产品导向
- social proof
- feature rhythm
- 控制模板味
- 信息层次

### Portfolio / Agency
优先强调：
- typography
- whitespace
- authored feeling
- signature motif
- 少而精的内容结构

### Glassmorphism
优先强调：
- 玻璃只用于关键节点
- 文字清晰度优先
- blur、border、inner highlight 组合
- 不要全页面无差别玻璃化

### Monochrome Minimal
优先强调：
- 类型层次
- 空间控制
- 动效克制
- 色彩纪律

## 自检清单

输出前检查：

- 是否先定义了气质？
- 是否有完整设计系统？
- 是否有页面骨架？
- 是否定义了分层？
- 是否定义了动效协议？
- 是否定义了响应式？
- 是否定义了工程边界？
- 是否写了负约束？
- 是否给了最终可复制 Prompt？
- 是否避免了空泛审美词堆砌？

如果有任何一项缺失，先补全。

## 成功标准

一个成功的网页 Prompt 应该满足：

- 读完后能立即感知页面气质
- 设计系统完整但不过载
- 页面结构明确
- 有至少一个强识别视觉装置
- 工程实现路径清晰
- 负约束有效减少跑偏
- 可以直接用于生成高质量代码
