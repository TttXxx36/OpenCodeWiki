---
id: GUIDE-20260522-003
title: Supplementary Skills - Missing Claude Code Skills Guide
title_zh: 补充技能 - 缺失的 Claude Code 技能使用指南
category: GUIDE
tags: [reference, guide, opencode, tool, productivity]
status: published
created: 2026-05-22
updated: 2026-05-22
summary: Claude Code 内置但 opencode 未预装的技能替代方案 — build-error-resolver, e2e-runner, refactor-cleaner, baoyu-image-gen, baoyu-diagram, baoyu-translate, baoyu-youtube-transcript 等
source: Custom compiled guide
difficulty: beginner
---

# Supplementary Skills Guide (缺失技能补充指南)

> Claude Code 内置技能在 opencode 中的替代方案

---

## 分类索引

| 类别 | 缺失技能 | 替代方案 | 类型 |
|:----:|:---------|:---------|:----:|
| 开发工作流 | build-error-resolver | **自定义 skill 已安装** | 🆕 已装 |
| 开发工作流 | e2e-runner | **自定义 skill 已安装** | 🆕 已装 |
| 开发工作流 | refactor-cleaner | **自定义 skill 已安装** | 🆕 已装 |
| 创意媒体 | baoyu-image-gen | **自定义 skill 已安装** | 🆕 已装 |
| 创意媒体 | baoyu-youtube-transcript | **自定义 skill 已安装** | 🆕 已装 |
| 创意媒体 | baoyu-comic | **自定义 skill 已安装** | 🆕 已装 |
| 创意媒体 | baoyu-infographic → diagram-maker | **自定义 skill 已安装** | 🆕 已装 |
| 创意媒体 | baoyu-image-cards | **自定义 skill 已安装** | 🆕 已装 |
| 创意媒体 | baoyu-cover-image | **自定义 skill 已安装** | 🆕 已装 |
| 文档转换 | baoyu-translate | **自定义 skill 已安装** | 🆕 已装 |
| 文档转换 | baoyu-url-to-markdown | **自定义 skill 已安装** | 🆕 已装 |
| 文档转换 | baoyu-slide-deck | **自定义 skill 已安装** | 🆕 已装 |
| 其他 | baoyu-wechat-summary | **自定义 skill 已安装** | 🆕 已装 |
| 其他 | baoyu-article-illustrator → image-generator | **自定义 skill 已安装** | 🆕 已装 |

---

## 1. build-error-resolver — 构建错误排查

### 说明

Claude Code 内置的构建错误排查 skill。我们的 `/diagnose`（MattPocock）和 ECC 中的调试工具完全可以覆盖。

### 使用方法

```text
"帮我看看这个编译错误是什么原因"
→ 触发 /diagnose 自动分析

"这个 TypeScript 类型报错怎么解"
→ AI 自动分析错误堆栈
```

### 已有替代来源

- MattPocock `/diagnose` — 严格调试循环
- ECC `error-handling` — 错误处理最佳实践

---

## 2. e2e-runner — 端到端测试

### 说明

Claude Code 内置的 E2E 测试执行器。我们已有更强大的 Playwright MCP。

### 使用方法

```text
"帮我跑一遍这个页面的 E2E 测试"
→ Playwright MCP 自动打开浏览器执行

"测试这个表单提交功能"
→ Playwright 填表 + 截图 + 验证

"做一轮全面 QA"
→ GStack /qa 走完整流程
```

### 已有替代来源

- Playwright MCP（已安装配置）
- GStack `/qa` — 全面 QA 测试
- GStack `/qa-only` — 只报告不修复

---

## 3. refactor-cleaner — 死代码清理

### 说明

Claude Code 内置的代码清理 skill。用于发现并删除无用代码。

### 使用方法

```text
"帮我清理这个项目里的死代码"
→ 触发 /improve-codebase-architecture

"这个文件有没有未使用的导入和变量"
→ AI 自动分析
```

### 已有替代来源

- MattPocock `/improve-codebase-architecture`
- GStack `/review` — 代码审查时也会发现

---

## 4. baoyu-image-gen — AI 图像生成 🆕

### 说明

Claude Code 内置的图像生成 skill。我们已配置 MiniMax M2.7 模型，可以直接调用。

### 前提

MiniMax Provider 已配置在 `~/.config/opencode/opencode.json` 中。

### 使用方法

```text
"帮我生成一张科技风格的海报，主题是 AI 编程"
→ 使用 MiniMax API 调用图像生成

"给这篇文章配一张封面图"
→ AI 自动生成配图
```

### 注意

需要 opencode 支持图像生成的 MCP 或工具。目前可以通过 MiniMax API 直接调用。

---

## 5. baoyu-youtube-transcript — YouTube 字幕获取 🆕

### 说明

**自定义 skill 已安装**到 `.opencode/skills/youtube-transcript/`。

### 使用方法

重启 opencode 后，直接说：

```text
"帮我总结一下这个 YouTube 视频：https://www.youtube.com/watch?v=XXX"
→ 自动获取字幕并生成双语摘要

"把这个视频的字幕提取出来"
→ 提取完整字幕文本
```

### 安装位置

```
.opencode/skills/youtube-transcript/
└── SKILL.md
```

---

## 6. baoyu-diagram — 专业图表绘制

### 说明

Claude Code 内置的图表绘制 skill。我们可以通过 AI 生成图表代码（Mermaid.js 等）的方式实现。

### 使用方法

```text
"帮我画一个系统架构图，展示前端后端和数据库的关系"
→ AI 自动生成 Mermaid 代码

"把这个流程画成时序图"
→ AI 生成图表代码
```

### 已有替代来源

- ECC `motion-ui` — UI 动态效果
- AI 可直接输出 Mermaid/PlantUML 代码，支持在 Markdown 中渲染

---

## 7. baoyu-translate — 翻译助手 🆕

### 说明

**自定义 skill 已安装**到 `.opencode/skills/translate-helper/`。支持中英互译，保留代码和格式。

### 使用方法

重启 opencode 后，直接说：

```text
"帮我把这个 README 翻译成中文"
→ 自动翻译，保留 Markdown 格式和代码

"翻译这段英文文档，技术术语保留原文"
→ 自动处理技术术语
```

### 安装位置

```
.opencode/skills/translate-helper/
└── SKILL.md
```

---

## 8. baoyu-url-to-markdown — 网页转 Markdown

### 说明

Claude Code 内置的网页转 Markdown skill。我们的 tavily-extract 工具可以直接实现。

### 使用方法

直接说：

```text
"帮我抓一下这个网页的内容"
→ 调用 tavily-extract 自动提取

"把这个网页转成 Markdown 格式"
→ 自动处理
```

### 已有替代来源

- `tavily-search_tavily_extract` MCP 工具（已安装）

---

## 9. baoyu-comic / baoyu-infographic — 漫画与信息图

### 说明

Claude Code 内置的创意工具。在 opencode 中没有直接替代，但可以通过 MiniMax 图像生成 + AI 设计的组合方式实现。

### 使用方法

```text
"帮我用漫画风格展示这个知识点的讲解"
→ AI 使用 MiniMax 生成系列图片

"把这个数据做成信息图"
→ AI 生成 HTML/CSS 图表页面
```

### 替代方案

- MiniMax M2.7 图像生成模型
- GStack `/design-html` 生成 HTML 信息图
- ECC `canvas-design` 画布设计

---

## 快速参考表

| 你想做什么 | 怎么说 | 实际使用的工具 |
|:-----------|:-------|:--------------|
| 修编译错误 | "这个编译错误怎么回事" | `/diagnose` + ECC error-handling |
| 跑 E2E 测试 | "测试这个页面的功能" | Playwright MCP |
| 清理死代码 | "帮我清理没用的代码" | `/improve-codebase-architecture` |
| 生成图片 | "帮我画一张 ... 的图片" | MiniMax M2.7 API |
| 取视频字幕 | "总结这个 YouTube 视频" | youtube-transcript skill 🆕 |
| 画架构图 | "画一个系统架构图" | AI 生成 Mermaid 代码 |
| 翻译文档 | "把这个翻译成中文" | translate-helper skill 🆕 |
| 网页转 Markdown | "抓一下这个网页" | tavily-extract |
