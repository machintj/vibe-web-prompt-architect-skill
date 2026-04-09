# Vibe Web Prompt Architect

`vibe-web-prompt-architect` 是一个用于 Codex 的 Skill 包，用来把模糊的网页创意、Hero 区块或 Landing Page 需求，转写为高质量、低歧义、可直接生成前端页面代码的结构化 Prompt。

## 适用场景

- 品牌首屏
- SaaS 官网
- 作品集
- Agency 页面
- AI 产品页
- 视频背景页面
- Glassmorphism / Liquid Glass 页面

## 目录结构

```text
.
├── SKILL.md
├── agents
│   └── openai.yaml
└── references
    └── prompt-patterns.md
```

## 文件说明

- `SKILL.md`
  - Skill 主定义，包含触发条件、执行原则、Prompt 结构和标准流程。
- `agents/openai.yaml`
  - UI 元信息，用于在技能列表中展示名称、简介和默认提示。
- `references/prompt-patterns.md`
  - 可复用的网页 Prompt 模板集合，覆盖 Hero、SaaS、Portfolio、Glassmorphism、Video Background、Monochrome 等模式。

## 安装

将整个目录复制到本机 Codex skills 目录：

```bash
mkdir -p ~/.codex/skills
cp -R ./vibe-web-prompt-architect ~/.codex/skills/
```

或直接放置为：

```text
~/.codex/skills/vibe-web-prompt-architect
```

## 使用方式

当你希望将网页 vibe coding 需求整理为结构化 Prompt 时，触发该 Skill，让模型按以下顺序输出：

1. 创意方向
2. 设计系统
3. 页面骨架
4. 分层关系
5. 动效协议
6. 响应式规则
7. 工程约束
8. 负约束
9. 最终 Prompt

## 示例输入

你可以像下面这样触发它：

```md
为一个 AI 设计工作室生成高端视频背景 Hero Prompt，风格要 cinematic、premium、dark，使用 React + TypeScript + Tailwind CSS，避免通用 SaaS 模板感。
```

```md
把一个极简黑白内容平台首页需求整理成结构化 Prompt，要求强调字体层次、留白、克制动效和单色系统。
```

```md
为一个 SaaS 官网生成 Landing Page Prompt，要求更品牌化、更少 feature-card 模板味，并包含设计系统、动效和工程约束。
```

## 示例输出结构

建议模型输出：

```md
## 规律摘要
[3-6 条规律]

## 结构化拆解
### 创意方向
### 设计系统
### 页面骨架
### 分层关系
### 动效协议
### 工程约束
### 负约束

## 最终 Prompt
[可直接复制使用的完整 Prompt]
```

## 设计目标

这个 Skill 的目标不是直接生成页面代码，而是先生成一份更稳定、更高级、更少模板味的网页 Prompt，再交给代码生成模型执行。

核心原则：

- 先定气质，再定组件
- 审美必须翻译成工程约束
- 关键节点高精度，非关键区域保留自由度
- 必须包含负约束
- 高级感来自层次，不来自组件数量

## 开发

如果你要扩展模板，优先在 `references/prompt-patterns.md` 中追加新的模式，而不是把所有内容堆进 `SKILL.md`。

建议新增模式时保持这几个维度稳定：

- 风格
- 设计系统
- 页面骨架
- 分层
- 动效
- 响应式
- 工程约束
- 负约束

## License

本仓库使用 MIT License，详见 `LICENSE`。
