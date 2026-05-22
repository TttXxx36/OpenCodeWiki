---
id: SKILLS-20260522-002
title: Skills and MCP Complete Usage Guide
title_zh: Skills 与 MCP 完整使用指南
category: SKILLS
tags: [reference, guide, opencode, claude-code, tool, general]
status: published
created: 2026-05-22
updated: 2026-05-22
summary: 8 个已安装技能合集的详细使用方法 + MCP 配置与使用指南 + 未来安装指南
source: https://github.com/affaan-m/everything-claude-code / https://github.com/obra/superpowers / https://github.com/garrytan/gstack / https://github.com/mattpocock/skills 等
---

# Skills and MCP Complete Usage Guide (Skills 与 MCP 完整使用指南)

---

## 目录

- [第一部分：技能合集](#第一部分技能合集)
  - [1. Everything Claude Code (ECC)](#1-everything-claude-code-ecc)
  - [2. Superpowers](#2-superpowers)
  - [3. GStack](#3-gstack)
  - [4. Matt Pocock Skills](#4-matt-pocock-skills)
  - [5. Andrej Karpathy Skills](#5-andrej-karpathy-skills)
  - [6. Understand-Anything](#6-understand-anything)
  - [7. Academic Research Skills](#7-academic-research-skills)
  - [8. Anthropic Official Skills](#8-anthropic-official-skills)
- [第二部分：插件与 MCP](#第二部分插件与-mcp)
  - [已安装插件](#已安装插件)
  - [已安装 MCP 服务器](#已安装-mcp-服务器)
  - [如何安装新的 MCP 服务器](#如何安装新的-mcp-服务器)
  - [如何安装新的插件](#如何安装新的插件)

---

# 第一部分：技能合集

## 1. Everything Claude Code (ECC)

> **仓库**: https://github.com/affaan-m/everything-claude-code
> **Stars**: ~100k | **Skills**: ~773 个
> **安装位置**: `~/.claude/skills/everything-claude-code/`

### 简介

社区最大 skill 合集。Anthropic 黑客松冠军作品，相当于给 AI 配了一个**完整的工程团队**。

### 核心技术栈覆盖

| 技术栈 | 对应 Skill |
|--------|-----------|
| **React / Next.js** | `frontend-patterns`, `nextjs-turbopack`, `vite-patterns`, `design-system` |
| **Vue / Nuxt** | `ui-to-vue`, `nuxt4-patterns` |
| **Swift / SwiftUI** | `swiftui-patterns`, `swift-concurrency-6-2` |
| **Rust** | `rust-patterns`, `rust-testing` |
| **Python** | `python-patterns`, `python-testing`, `fastapi-patterns`, `django-patterns` |
| **Go** | `golang-patterns`, `golang-testing` |
| **Java / Spring Boot** | `springboot-patterns`, `springboot-security`, `springboot-tdd` |
| **Kotlin** | `kotlin-patterns`, `kotlin-testing`, `kotlin-ktor-patterns` |
| **Laravel / PHP** | `laravel-patterns`, `laravel-security`, `laravel-tdd` |
| **Node.js / NestJS** | `nestjs-patterns`, `nodejs-keccak256` |
| **PostgreSQL / MySQL / Redis** | `postgres-patterns`, `mysql-patterns`, `redis-patterns`, `prisma-patterns` |
| **Docker / K8s** | `docker-patterns`, `deployment-patterns` |
| **iOS** | `swiftui-patterns`, `compose-multiplatform-patterns` |
| **Android** | `android-clean-architecture`, `compose-multiplatform-patterns` |

### 调用方式

```text
直接说："帮我用 Spring Boot 最佳实践写这个 API"
→ 自动匹配 /springboot-patterns

直接说："给这个 SwiftUI 页面加个列表"
→ 自动匹配 /swiftui-patterns

直接说："做一次安全审查"
→ 自动匹配 /security-review
```

---

## 2. Superpowers

> **仓库**: https://github.com/obra/superpowers
> **Stars**: ~41k | **Skills**: 14 个
> **安装位置**: `~/.claude/skills/superpowers/`

### 简介

第二大社区 Skill 库。提供**完整开发流程**，每个 skill 可以链式调用。

### 完整流程

```text
/brainstorming          →  需求头脑风暴
     ↓
/writing-plans          →  拆分为可实现的任务
     ↓
/subagent-driven-development  →  子 Agent 实现
     ↓
/requesting-code-review →  请求审查
     ↓
/receiving-code-review  →  按意见修改
     ↓
/verification-before-completion →  终验
     ↓
/finishing-a-development-branch →  合并
```

### 各 Skill 详细用法

| Skill | 触发词 | 作用 |
|-------|--------|------|
| `/brainstorming` | "帮我 brainstorm" "头脑风暴" | 交互式需求探索，问问题直到需求明确 |
| `/writing-plans` | "写成开发计划" "拆任务" | 把需求拆成 2-5 分钟的子任务 |
| `/test-driven-development` | "用 TDD" "红绿重构" | 强制测试先行的 TDD 循环 |
| `/subagent-driven-development` | "派个子 Agent" "并行开发" | 每个任务在独立子会话中执行，防止上下文污染 |
| `/systematic-debugging` | "系统排查" "仔细调试" | 结构化调试：观察→假设→验证→修复 |
| `/requesting-code-review` | "帮我 review" "审查代码" | 提交代码审查请求 |
| `/receiving-code-review` | "按 review 意见改" | 处理审查意见并修改 |
| `/verification-before-completion` | "验证实现" "检查完成度" | 自动对照需求验证 |
| `/finishing-a-development-branch` | "合并分支" "准备发布" | 完成分支收尾工作 |
| `/using-git-worktrees` | "用 worktree" | Git worktree 管理 |
| `/dispatching-parallel-agents` | "同时做这两个任务" | 并行派发多个子 Agent |
| `/executing-plans` | "执行计划" "开始开发" | 按 plan 驱动开发 |
| `/writing-skills` | "创建 skill" | 创建自定义 skill |
| `/using-superpowers` | "superpowers 怎么用" | 查看 superpowers 完整指南 |

### 使用示例

```text
用户：我想加一个用户登录功能，帮我用 Superpowers 流程走一遍
AI 响应：
  1. 先 /brainstorming 问清楚需求细节
  2. 生成 /writing-plans 开发计划
  3. 用 /subagent-driven-development 派子 Agent 实现
  4. 完成后 /requesting-code-review 审查
```

---

## 3. GStack

> **仓库**: https://github.com/garrytan/gstack
> **Stars**: ~66k | **Skills**: 57 个
> **安装位置**: `~/.claude/skills/gstack/`

### 简介

YC CEO Garry Tan 的个人工具集，把 AI 变成**虚拟工程团队**。

### 按角色分类

#### 🏢 CEO / 创始人

| Skill | 触发词 | 用法说明 |
|-------|--------|---------|
| `/plan-ceo-review` | "CEO 审查" "从老板角度看" | 挑战你的前提假设，找到被忽略的机会。会问：为什么做这个？不做会怎样？有没有更简单的方案？ |
| `/office-hours` | "office hours" "创业答疑" | YC 式 6 个强力问题：需求是否真实？用户现在怎么解决？最小切入点在哪？ |

#### 🎨 设计师

| Skill | 触发词 | 用法说明 |
|-------|--------|---------|
| `/plan-design-review` | "设计评审" "设计审查" | 给设计方案打分（0-10 分），解释怎样能到 10 分，然后直接修改方案 |
| `/design-shotgun` | "出几个方案" "多方案设计" | 同时生成多个设计变体，开一个浏览器看对比，选方向后迭代 |
| `/design-consultation` | "设计系统" "品牌指南" | 了解你的产品、调研竞品，输出完整设计系统（色彩/字体/间距/动效） |
| `/design-html` | "设计转 HTML" "写前端代码" | 把设计稿变成生产级 HTML/CSS，零依赖，30KB 开销 |
| `/design-review` | "视觉检查" "UI 走查" | 逐一检查间距/层次/交互/AI 生成痕迹，自动修复 |

#### 🧪 QA / 测试

| Skill | 触发词 | 用法说明 |
|-------|--------|---------|
| `/browse` | "打开这个页面" "看看这个网站" | 浏览器自动导航、点击、填表单、截图、diff。~100ms 一个命令 |
| `/qa` | "做 QA" "全面测试" | 系统性测试：发现 bug → 自动修复 → 重新验证 → 确认修复 |
| `/qa-only` | "只报告 bug" "只测不改" | 和 qa 一样但只出报告，不修改代码 |
| `/scrape` | "抓取数据" "爬这个页面" | 首次调用原型化抓取流程返回 JSON，之后同类型抓取 ~200ms 完成 |
| `/setup-browser-cookies` | "导入 cookie" "登录浏览器" | 从你真实的 Chrome 浏览器导入 cookie，用于测试已登录页面 |

#### 🚢 发布 / 运维

| Skill | 触发词 | 用法说明 |
|-------|--------|---------|
| `/ship` | "ship 这个" "发布" | 检测 base 分支 → 运行测试 → review diff → 打版本 → 更新 CHANGELOG → commit → push → 创建 PR |
| `/land-and-deploy` | "合并部署" "上线" | 合并 PR → 等 CI → 部署 → 验证生产环境健康 |
| `/canary` | "灰度发布" "监控上线" | 持续监控页面错误/性能/截图，与上线前基线对比 |
| `/setup-deploy` | "配置部署" | 检测部署平台（Fly/Render/Vercel 等），写入部署配置 |
| `/benchmark` | "性能测试" "测速度" | 建立页面加载时间基线，对比 PR 前后变化 |

#### 🔒 安全

| Skill | 触发词 | 用法说明 |
|-------|--------|---------|
| `/cso` | "安全审计" "安全扫描" | 双重模式：日常（零噪音，8/10 置信度门槛）和全面扫描（月级深度扫描）|
| `/careful` | "小心模式" "安全模式" | 在 rm -rf / DROP TABLE / force-push 等危险操作前警告 |
| `/freeze` | "冻结范围" "只改这个目录" | 限制 AI 只能修改指定目录内的文件 |
| `/guard` | "完全保护" "锁定" | = careful + freeze，最大保护 |

#### 📝 文档

| Skill | 触发词 | 用法说明 |
|-------|--------|---------|
| `/document-generate` | "写文档" "生成文档" | 使用 Diataxis 框架（教程/参考/解释/操作指南）生成完整文档 |
| `/document-release` | "更新文档" "发布后文档" | 读取所有文档 → 对比 diff → 更新 README/ARCHITECTURE → 清理 TODO |

#### 📊 其他

| Skill | 触发词 | 用法说明 |
|-------|--------|---------|
| `/make-pdf` | "转 PDF" "导出 PDF" | Markdown → 出版物质量 PDF（封面/目录/页眉/页码/水印） |
| `/retro` | "回顾" "这周总结" | 分析 commit 历史、工作模式、代码质量指标，每人贡献报告 |
| `/health` | "健康检查" "代码评分" | 跑类型检查/格式化/测试/死代码检测 → 加权 0-10 分 + 趋势追踪 |
| `/review` | "审查 PR" "代码审查" | SQL 安全、LLM 信任边界、条件副作用检查 |
| `/investigate` | "调查" "根因分析" | 四阶段：调查→分析→假设→修复。铁律：未找到根因不修复 |
| `/codex` | "第二意见" "问 codex" | 交给 OpenAI Codex 独立 review / 对抗测试 / 咨询 |
| `/learn` | "学到了什么" "经验教训" | 管理跨 session 的项目经验积累 |

### 典型使用场景

```text
场景 1：产品方案阶段
"我想做一个新功能，帮我从 CEO 角度审查" → /plan-ceo-review
"顺便出几个 UI 方案看看" → /design-shotgun
设计定稿后 → "转成 HTML" → /design-html

场景 2：上线前
"做一轮安全审计" → /cso
"做全面 QA" → /qa
"部署上线" → /ship → /land-and-deploy
"开启灰度监控" → /canary
```

---

## 4. Matt Pocock Skills

> **仓库**: https://github.com/mattpocock/skills
> **Stars**: ~138k | **Skills**: 28 个
> **安装位置**: `~/.claude/skills/mattpocock-skills/`

### 简介

TypeScript 教父的个人工具集，聚焦**高质量工程实践**。

### 工程类

#### `/diagnose` — 严格调试

```text
触发词: "诊断这个 bug" "debug" "为什么崩了" "性能下降"
流程:
  复现 → 最小化复现条件 → 提出假设 → 加日志/仪表 → 修复 → 回归测试
铁律: 没有找到根因就不准修代码
```

#### `/tdd` — 测试驱动开发

```text
触发词: "TDD" "红绿重构" "先写测试"
流程:
  Red（写失败测试）→ Green（写最简实现通过）→ Refactor（重构）
```

#### `/review` — 双轴代码审查

```text
触发词: "review" "审查代码" "检查改动"
审查两轴:
  - Standards：是否符合项目编码规范
  - Spec：是否符合需求文档/PRD
并行派发两个子 Agent 分别审查，报告放一起对比
```

#### `/prototype` — 快速原型

```text
触发词: "原型验证" "试试这个想法" "prototype"
两条路:
  - 终端可运行的原型（验证逻辑/状态）
  - 多个 UI 变体（验证设计方向）
用完即弃，不提交到代码库
```

#### `/zoom-out` — 宏观视角

```text
触发词: "zoom out" "全貌" "大局" "看不懂"
作用:
  AI 退后一步，从系统层面解释当前代码在整个项目中的位置
```

#### `/to-prd` — 会议→文档

```text
触发词: "写成 PRD" "整理成需求文档"
作用:
  把当前对话中的讨论提炼成结构化的 PRD 文档
```

#### `/to-issues` — 需求→Issue

```text
触发词: "拆成 issue" "分成任务"
作用:
  按 tracer bullet 原则把需求拆成可独立执行的 issue
```

#### `/triage` — Issue 分类

```text
触发词: "给 issue 分类" "triage"
作用:
  通过状态机驱动对 issue 进行分类、打标签、分配优先级
```

#### `/improve-codebase-architecture` — 架构改进

```text
触发词: "找架构问题" "改进架构"
作用:
  结合 CONTEXT.md 领域语言和 ADR 决策记录，找到解耦机会
```

#### `/grill-with-docs` — 基于文档的拷问

```text
触发词: "基于文档拷问我" "审查方案"
作用:
  读取项目文档 → 在文档上下文中拷问你的方案 → 同步更新文档
```

### 生产力类

| Skill | 触发词 | 说明 |
|-------|--------|------|
| `/grill-me` | "拷问我" "审查方案" | 逐层追问直到达成共识，一次只问一个问题 |
| `/handoff` | "交接" "整理会话" | 把当前会话压缩成另一 Agent 可以直接接手的交接文档 |
| `/caveman` | "caveman" "极简模式" | 省 ~75% token：去 filler / 去语气词 / 去礼貌用语 |
| `/write-a-skill` | "创建 skill" | 指导创建标准 SKILL.md 结构和资源 |

### 个人类

| Skill | 触发词 | 说明 |
|-------|--------|------|
| `/obsidian-vault` | "Obsidian" "查笔记" | 搜索/创建/管理 Obsidian vault 笔记 |
| `/edit-article` | "润色文章" "编辑文章" | 重构段落结构、改善清晰度、精简语言 |

### 杂项

| Skill | 触发词 | 说明 |
|-------|--------|------|
| `/setup-pre-commit` | "设置 pre-commit" "装 git hooks" | 配置 Husky + lint-staged + 类型检查 + 测试 |
| `/scaffold-exercises` | "创建练习题" "scaffold" | 创建标准练习结构（章节/题目/解答/讲解）|
| `/git-guardrails-claude-code` | "git 保护" "禁止 git push" | 阻止危险 git 命令（push/reset --hard/clean -f 等）|

### 写作类

| Skill | 触发词 | 说明 |
|-------|--------|------|
| `/writing-beats` | "按节奏写" "叙事结构" | 让用户选择起始 beat → 只写这一段 → 提供下步选择 |
| `/writing-fragments` | "碎片想法" "素材收集" | 挖掘用户的碎片化想法 → 追加到单文件中 |
| `/writing-shape` | "成型" "初稿→文章" | 从草稿出发 → 试写开头 → 逐段展开 → 优化格式 |

---

## 5. Andrej Karpathy Skills

> **仓库**: https://github.com/multica-ai/andrej-karpathy-skills
> **Stars**: ~141k | **Skills**: 1 个
> **安装位置**: `~/.claude/skills/andrej-karpathy-skills/`

### 简介

Karpathy 的 AI 编码行为规范。不是可调用的 skill，而是**全局行为准则**——自动生效。

### 核心原则

```
1. 先读代码再修改——不要跳过理解直接写
2. 小步提交——每次提交只做一件事
3. 复用现有——不要重新发明轮子
4. 测试先行——关键逻辑必须有测试
5. 问清楚再动手——需求不明确时先提问
```

### 使用方式

安装后自动生效，无需手动调用。在任何对话中 AI 都会遵循这些原则。

---

## 6. Understand-Anything

> **仓库**: https://github.com/Lum1104/Understand-Anything
> **Stars**: ~17k | **Skills**: 8 个
> **安装位置**: `~/.claude/skills/understand-anything/`

### 简介

把代码库变成**交互式知识图谱**，解决"看不懂这个项目"的问题。

### 各 Skill 用法

#### `/understand` — 全量扫描

```text
触发词: "帮我理解这个项目" "看看这个代码库"
作用:
  扫描整个项目 → 生成交互式知识图谱（架构图、组件关系图）
输出: 浏览器中打开的交互式图谱
```

#### `/understand-chat` — 图谱问答

```text
触发词: "这个模块在做什么" "哪个文件负责 X"
作用:
  基于已生成的知识图谱回答问题，不需要再次扫描
```

#### `/understand-dashboard` — 可视化面板

```text
触发词: "打开知识图谱面板" "可视化"
作用:
  启动 Web 版知识图谱仪表盘
```

#### `/understand-diff` — 变更影响分析

```text
触发词: "这次改动的风险" "diff 影响"
作用:
  分析 git diff → 标记受影响的组件 → 评估风险等级
```

#### `/understand-domain` — 领域分析

```text
触发词: "业务逻辑图谱" "领域模型"
作用:
  提取业务领域知识 → 生成交互式领域流程图
两种模式: 轻量快速扫描 / 基于已有图谱深度分析
```

#### `/understand-explain` — 深度解释

```text
触发词: "给我解释这个函数" "这段代码什么意思"
作用:
  针对单个文件/函数/模块做深层次解释
```

#### `/understand-knowledge` — 知识库分析

```text
触发词: "分析这个知识库" "LLM Wiki"
作用:
  分析 LLM Wiki 格式的知识库 → 提取实体/关系/主题聚类
```

#### `/understand-onboard` — 新成员指南

```text
触发词: "写 Onboarding" "入职文档"
作用:
  为新成员生成项目入职指南
```

### 典型流程

```text
接到新项目:
  /understand → 先全量扫描项目
  → /understand-chat 问具体问题
  → /understand-explain 深入看关键模块
  → /understand-domain 理解业务逻辑
  → /understand-onboard 生成文档给团队成员
```

---

## 7. Academic Research Skills

> **仓库**: https://github.com/Imbad0202/academic-research-skills
> **Stars**: ~19k | **Skills**: 4 个
> **安装位置**: `~/.claude/skills/academic-research-skills/`

### 简介

**完整学术研究全流程**——13 Agent 深度研究 + 12 Agent 论文写作 + 5 角色同行评审。

### 各 Skill 详解

#### `/deep-research` — 深度研究

```text
触发词: "研究一下" "调研" "文献综述" "fact check"

7 种模式:
  - full: 完整研究（13 Agent 全部上阵）
  - quick-brief: 快速简报
  - paper-review: 论文审查
  - lit-review: 文献综述
  - fact-check: 事实核查
  - socratic: 苏格拉底式研究对话
  - systematic-review: 系统综述（含 Meta 分析）

输出: APA 7.0 格式研究报告
```

#### `/academic-paper` — 论文写作

```text
触发词: "写论文" "学术写作"

10 种模式:
  - full: 完整论文
  - plan: 写作计划
  - outline: 大纲
  - revision: 修改
  - abstract: 摘要
  - lit-review: 文献综述
  - format-convert: 格式转换
  - citation-check: 引用检查
  - disclosure: 披露声明

支持 6 种论文类型、5 种引用格式、双语摘要
输出: LaTeX / DOCX / PDF
```

#### `/academic-paper-reviewer` — 同行评审

```text
触发词: "帮我审稿" "peer review" "评审论文"

5 个模拟审稿人:
  - EIC（主编）
  - 3 个同行审稿人（领域专长不同）
  - Devil's Advocate（魔鬼代言人）

6 种评审模式: full-review / re-review / quick / methodology / socratic / calibration
```

#### `/academic-pipeline` — 完整管线

```text
触发词: "走一遍学术流程" "research to paper"

10 阶段工作流:
  research → write → integrity-check → review
  → revise → re-review → re-revise
  → final-integrity-check → finalize
```

### 典型流程

```text
用户: "帮我研究一下 LLM Agent 的最新进展，写一篇综述论文"
AI 响应:
  1. /deep-research 开始深度研究
  2. 生成研究报告
  3. /academic-paper 写论文
  4. /academic-paper-reviewer 找审稿人评审
  5. 根据意见修改
  6. 输出最终版
```

---

## 8. Anthropic Official Skills

> **仓库**: https://github.com/anthropics/skills
> **Stars**: 官方仓库
> **安装位置**: `~/.claude/skills/anthropic-skills/`

### 文档生成类

| Skill | 触发词 | 输出格式 | 说明 |
|-------|--------|---------|------|
| `/docx` | "生成 Word" ".docx" | `.docx` | 生成 Microsoft Word 格式文档 |
| `/xlsx` | "生成 Excel" ".xlsx" | `.xlsx` | 生成 Excel 表格，支持公式和格式 |
| `/pdf` | "生成 PDF" | `.pdf` | 从 Markdown 生成 PDF |
| `/pptx` | "生成 PPT" "幻灯片" | `.pptx` | 生成 PowerPoint 演示文稿 |

### 开发工具类

| Skill | 触发词 | 说明 |
|-------|--------|------|
| `/mcp-builder` | "搭 MCP 服务器" | 从零搭建 MCP 服务器 |
| `/claude-api` | "用 Claude API" | Claude API 集成指南 |
| `/webapp-testing` | "测试 Web 应用" | Web 应用自动化测试 |
| `/web-artifacts-builder` | "创建 Web 构件" | 构建 Web artifacts |
| `/skill-creator` | "创建 skill" | Anthropic 官方版 skill 创建器 |

### 设计类

| Skill | 触发词 | 说明 |
|-------|--------|------|
| `/algorithmic-art` | "算法艺术" | 生成算法艺术作品 |
| `/canvas-design` | "Canvas 设计" | Canvas 交互式设计 |
| `/frontend-design` | "前端设计" | 前端界面设计 |
| `/theme-factory` | "创建主题" | 主题创建工厂 |
| `/brand-guidelines` | "品牌指南" | 品牌视觉规范 |

### 其他

| Skill | 触发词 | 说明 |
|-------|--------|------|
| `/doc-coauthoring` | "协作编辑" | 多人协作编辑文档 |
| `/internal-comms` | "内部通讯" | 内部沟通文档 |
| `/slack-gif-creator` | "Slack GIF" | 生成 Slack 用 GIF |

---

# 第二部分：插件与 MCP

## 当前系统配置总览

| 配置项 | 文件路径 | 内容 |
|--------|---------|------|
| 全局 MCP + 插件 | `~/.config/opencode/opencode.jsonc` | MCP: tavily-search, playwright, github / 插件: visual-cache, skill-creator |
| Provider | `~/.config/opencode/opencode.json` | MiniMax 模型配置 |
| 项目插件 | `~/.opencode/opencode.json` | opencode-visual-cache@latest |

---

## 已安装插件

### 1. opencode-visual-cache

| 属性 | 内容 |
|------|------|
| **版本** | latest |
| **安装方式** | `~/.opencode/opencode.json` 和 `~/.config/opencode/opencode.jsonc` 中注册 |
| **作用** | 提供 TUI（终端界面）的视觉缓存，支持历史会话浏览 |

**功能说明**：
- 缓存当前和历史的 opencode 会话数据
- 让 TUI 能显示会话列表和消息历史
- 插件加载时自动从 `opencode.db` 同步数据到 `opencode-opencodex.db`

**使用方法**：无需手动调用，后台自动运行。重启 opencode 后生效。

**常见问题**：
- 如果 TUI 看不到历史会话，说明缓存未同步。重新启动 opencode 即可自动同步
- 如果同步有问题，可手动运行同步脚本

### 2. opencode-skill-creator

| 属性 | 内容 |
|------|------|
| **版本** | 0.2.16 |
| **安装方式** | `npx opencode-skill-creator install --global` |
| **安装位置** | `~/.config/opencode/skills/opencode-skill-creator/` |
| **作用** | 创建、测试、优化自定义 Skill |

**注册的工具**：

| 工具 | 作用 |
|------|------|
| `skill_validate` | 验证 SKILL.md 结构和 frontmatter |
| `skill_parse` | 解析 SKILL.md 提取 name/description |
| `skill_eval` | 测试 skill 触发准确率 |
| `skill_improve_description` | 用 LLM 优化 desctiption |
| `skill_optimize_loop` | 自动 eval→优化迭代循环 |
| `skill_aggregate_benchmark` | 汇总测试结果生成统计 |
| `skill_generate_report` | 生成 HTML 优化报告 |
| `skill_serve_review` | 启动 Web 审查界面 |
| `skill_stop_review` | 停止审查服务 |
| `skill_export_static_review` | 导出静态 HTML 审查文件 |

**使用流程**：
```text
1. 说 "Use opencode-skill-creator to create a skill"
2. AI 会问你 3-5 个问题明确需求
3. 生成 SKILL.md 草稿到临时目录
4. 跑 eval 测试触发准确率
5. 自动优化 description
6. 你确认后安装到正式路径
```

---

## 已安装 MCP 服务器

### tavily-search — 互联网搜索

| 属性 | 内容 |
|------|------|
| **类型** | remote（远程 MCP） |
| **端点** | `https://tavily.ivanli.cc/mcp` |
| **状态** | 已启用 |
| **作用** | AI 可以通过这个 MCP 进行互联网搜索、网页抓取和内容提取 |

**提供的工具**：

| 工具 | 参数 | 说明 |
|------|------|------|
| `tavily-search_tavily_search` | query, max_results, search_depth | 互联网搜索，返回带摘要的结果 |
| `tavily-search_tavily_extract` | urls, extract_depth, format | 提取指定 URL 的内容 |
| `tavily-search_tavily_crawl` | url, max_depth, max_pages | 深度爬取网站 |
| `tavily-search_tavily_research` | query | 深度研究（生成结构化报告） |

**使用方式**：不需要手动调用，AI 需要查资料时自动使用。

**高效使用技巧**：
- 需要最新信息时，直接说"帮我查一下最新的 X"
- 需要阅读某个网页时，说"帮我抓一下这个链接"
- 需要深度研究报告时，说"帮我深度研究一下 X 主题"

---

### playwright — 浏览器自动化

| 属性 | 内容 |
|------|------|
| **类型** | local（本地 MCP） |
| **命令** | `npx -y @playwright/mcp` |
| **状态** | 已启用 |
| **依赖** | Chromium 浏览器已安装（`playwright install chromium`） |
| **作用** | AI 可以控制真实浏览器：导航页面、点击元素、填表单、截图、验证页面状态 |

**提供的核心能力**：

| 操作 | 说明 |
|------|------|
| 页面导航 | 打开任意 URL，等待页面加载 |
| 点击元素 | 点击按钮、链接、菜单项 |
| 表单填写 | 输入文本、选择下拉框、勾选复选框 |
| 页面截图 | 截取全页或特定区域，添加标注 |
| 状态验证 | 检查元素可见性、文本内容、属性值 |
| 对话框处理 | 自动确认/取消 alert/confirm/prompt |
| 文件上传 | 上传文件到表单 |
| 响应式测试 | 设置不同视口大小测试自适应布局 |
| Diff 对比 | 操作前后截图对比，发现视觉变化 |

**使用方式**：不需要手动调用，AI 需要测试浏览器时自动调用。

**高效使用技巧**：

```text
✅ 正确用法:
  "打开 https://example.com 帮我看看这个页面"
  "在这个搜索框输入 'hello' 然后点搜索按钮"
  "截图给我看看现在的页面状态"
  "帮我测试这个表单提交功能"
  "分别用手机和桌面分辨率打开这个页面"
  "点这个按钮前后各截一张图，对比有什么变化"

❌ 错误用法:
  "用 playwright 打开百度"                    ← 不需要提具体工具名
  "写一段 playwright 代码"                     ← 这不是 MCP 的目的
  "帮我装个 playwright 环境"                    ← 已经装好了
```

**对比 GStack 内置 `/browse`**：

| 维度 | GStack `/browse` | Playwright MCP |
|------|-----------------|----------------|
| 速度 | ~100ms/命令 | 稍慢（启动浏览器有开销）|
| 能力 | 导航/截图/点击 | 导航/截图/点击/填表/上传/对话框/响应式 |
| 适用场景 | 快速验证 | 复杂交互测试 |

> 日常快速查看用 GStack `/browse`，复杂交互测试用 Playwright MCP。

---

### github — GitHub API 操作

| 属性 | 内容 |
|------|------|
| **类型** | local（本地 MCP） |
| **命令** | `npx -y @modelcontextprotocol/server-github` |
| **状态** | 已启用 |
| **认证** | GitHub Personal Access Token |
| **作用** | AI 可以直接操作 GitHub：管理 Issue、PR、Code Review、搜索代码 |

**提供的核心能力**：

| 操作 | 说明 |
|------|------|
| Issue 管理 | 创建/查看/更新/关闭 Issue |
| PR 管理 | 创建/查看/合并 Pull Request |
| 代码审查 | 查看 PR diff、提交审查意见 |
| 代码搜索 | 搜索仓库中的代码 |
| 文件操作 | 读取/创建/更新仓库文件 |
| 仓库信息 | 查看仓库详情、分支、标签 |

**使用方式**：不需要手动调用，AI 需要操作 GitHub 时自动使用。

**高效使用技巧**：

```text
✅ 正确用法:
  "帮我给这个仓库创建一个 Issue"                ← 自动调用 GitHub MCP
  "看看这个 PR 的改动内容"                      ← 自动读取 PR diff
  "帮我把这个文件改成 ..."                       ← 直接操作文件
  "在这个仓库里搜索所有 API 相关代码"            ← 代码搜索
  "帮我 review 这个 PR"                         ← 自动分析 + 提交意见

❌ 错误用法:
  "用 GitHub MCP 帮我做 X"                     ← 不需要提具体工具名
  "我的 Token 是 ..."                           ← 已经配置好了
```

**安全提醒**：
- Token 存储在 `~/.config/opencode/opencode.jsonc` 中
- 该文件不在项目 Git 仓库中，不会被意外提交
- 如果 Token 泄露，可以在 GitHub Settings → Developer settings → Personal access tokens 撤销

---

## 当前 MCP 配置（共 3 个）

```jsonc
// ~/.config/opencode/opencode.jsonc
{
  "mcp": {
    "tavily-search": {          // 互联网搜索
      "type": "remote",
      "url": "https://tavily.ivanli.cc/mcp",
      "headers": { "Authorization": "Bearer <token>" },
      "enabled": true
    },
    "playwright": {             // 浏览器自动化
      "type": "local",
      "command": ["npx", "-y", "@playwright/mcp"],
      "enabled": true
    },
    "github": {                 // GitHub API 操作
      "type": "local",
      "command": ["npx", "-y", "@modelcontextprotocol/server-github"],
      "enabled": true,
      "env": { "GITHUB_TOKEN": "<your-token>" }
    }
  }
}
```

---

## 如何安装新的 MCP 服务器

MCP（Model Context Protocol）服务器让 AI 能连接外部工具和数据源。

### 配置文件位置

```
全局配置: ~/.config/opencode/opencode.jsonc   ← 适用于所有项目
项目配置: .opencode/opencode.json              ← 仅当前项目
用户配置: ~/.opencode/opencode.json             ← 早期版本
```

`opencode.jsonc` 支持注释，`opencode.json` 不支持注释。推荐用 `opencode.jsonc`。

### 安装步骤

#### 本地 MCP（在本机运行）

```jsonc
// ~/.config/opencode/opencode.jsonc
{
  "mcp": {
    "my-local-server": {
      "type": "local",
      "command": ["node", "path/to/server.js"],  // 启动命令（数组形式）
      "enabled": true,                            // 是否启用
      "env": {                                     // 环境变量（可选）
        "API_KEY": "your-key"
      }
    }
  }
}
```

#### 远程 MCP（运行在服务器上）

```jsonc
{
  "mcp": {
    "my-remote-server": {
      "type": "remote",
      "url": "https://example.com/mcp",
      "enabled": true,
      "headers": {
        "Authorization": "Bearer your-token"
      }
    }
  }
}
```

#### 禁用 MCP

```jsonc
{
  "mcp": {
    "old-server": {
      "enabled": false  // 设为 false 即可禁用，不需要删除
    }
  }
}
```

### 其他推荐 MCP（尚未安装）

| MCP 服务器 | 作用 | 类型 | 推荐理由 |
|-----------|------|------|---------|
| **Filesystem MCP** | 安全文件系统访问 | local | 限制 AI 只能访问指定目录 |
| **Sequential Thinking MCP** | 增强 AI 推理能力 | local | 复杂问题分步推理 |
| **PostgreSQL MCP** | 数据库查询 | local | 直接查询数据库 |
| **Brave Search MCP** | 备选搜索引擎 | remote | 如果 tavily 不能用 |

### 安装示例：Playwright MCP

```jsonc
{
  "mcp": {
    "playwright": {
      "type": "local",
      "command": ["npx", "-y", "@playwright/mcp"],
      "enabled": true
    }
  }
}
```

安装后重启 opencode，AI 就可以控制浏览器做自动化测试。

### 注意事项

1. 修改配置后**必须重启 opencode** 才能生效
2. `command` 必须是数组，不能是字符串
3. 远程 MCP 注意 Token 安全，不要提交到 Git
4. 可以用 `enabled: false` 临时禁用，不必删除配置

---

## 如何安装新的插件

### 从 npm 安装

```jsonc
// ~/.config/opencode/opencode.jsonc
{
  "plugin": [
    "opencode-visual-cache@latest",  // 已安装
    "opencode-skill-creator",        // 已安装
    "新的插件名称"                     // 添加新插件
  ]
}
```

### 从本地文件安装

```jsonc
{
  "plugin": [
    "./local-plugin.js",             // 相对路径
    "file:///abs/path/plugin.js"     // 绝对路径
  ]
}
```

### 自动发现插件

opencode 会自动加载 `.opencode/plugin/` 和 `.opencode/plugins/` 目录下的所有 `.ts` 和 `.js` 文件，不需要手动注册。

### 配置示例：添加一个新插件

```bash
# 1. 编辑全局配置文件
notepad $env:USERPROFILE\.config\opencode\opencode.jsonc

# 2. 在 plugin 数组中加入新插件名
# 3. 保存文件
# 4. 重启 opencode
```

---

## 附录：推荐工作流组合

### 从零开始一个功能

```text
1. /office-hours            → 确认需求价值
2. /brainstorming           → 头脑风暴具体方案
3. /plan-ceo-review         → 从商业角度审查
4. /plan-eng-review         → 架构评审
5. /writing-plans           → 拆开发计划
6. /subagent-driven-development  → 子 Agent 实现
7. /review                  → 代码审查
8. /qa                      → 全面测试
9. /cso                     → 安全审计
10. /ship                   → 发布
```

### 接手旧项目

```text
1. /understand              → 全量扫描项目图谱
2. /understand-chat         → 问清楚每个模块
3. /improve-codebase-architecture  → 找架构改进点
4. /diagnose（如果有 bug）  → 诊断遗留问题
```

### 写技术文章

```text
1. /writing-fragments       → 收集碎片想法
2. /writing-shape           → 成型为文章
3. /edit-article            → 润色优化
4. /make-pdf                → 导出 PDF（GStack）
```

### 学术研究

```text
1. /deep-research           → 深度研究
2. /understand-knowledge    → 可视化知识图谱
3. /academic-paper          → 写论文
4. /academic-paper-reviewer → 同行评审
5. 按意见修改 → 终稿
```
