---
id: SKILLS-20260522-001
title: All Installed Skills Reference
title_zh: 全部已安装技能知识库
category: SKILLS
tags: [general, reference, opencode, claude-code, gstack, superpowers, engineering, productivity]
created: 2026-05-22
updated: 2026-05-22
summary: OpenCode / Claude Code 已安装的 8 个技能合集共 900+ SKILL.md 的完整使用指南
source: https://github.com/affaan-m/everything-claude-code / https://github.com/obra/superpowers / https://github.com/garrytan/gstack / https://github.com/mattpocock/skills 等
---

# All Installed Skills Reference (全部已安装技能知识库)

> 最后更新: 2026-05-22
> 已安装 Skill 合集: **8 个合集，共 900+ SKILL.md 文件**
> 安装位置: `~/.claude/skills/`（opencode 和 Claude Code 自动扫描）

---

## 目录

1. [Everything Claude Code](#1-everything-claude-code)
2. [Superpowers](#2-superpowers)
3. [GStack](#3-gstack)
4. [Matt Pocock Skills](#4-matt-pocock-skills)
5. [Andrej Karpathy Skills](#5-andrej-karpathy-skills)
6. [Understand-Anything](#6-understand-anything)
7. [Academic Research Skills](#7-academic-research-skills)
8. [Anthropic 官方 Skills](#8-anthropic-官方-skills)
9. [如何正确调用 Skill](#9-如何正确调用-skill)

---

## 1. Everything Claude Code

| 属性 | 内容 |
|------|------|
| **GitHub** | https://github.com/affaan-m/everything-claude-code |
| **Stars** | ~100k |
| **安装路径** | `~/.claude/skills/everything-claude-code/` |
| **Skill 数量** | ~773 个 |

### 功能介绍

到目前为止最大的社区 Skill 合集。由 Anthropic 黑客松冠军 Affaan Mustafa 开发，将 AI 编码代理变成一个**完整的工程团队**。包含 28 个子 Agent、119+ 技能、60+ 命令、20+ 自动化钩子、14 个 MCP 服务器。

### Skill 分类速览

| 分类 | 包含 Skill | 适用领域 |
|------|-----------|---------|
| **前端** | frontend-patterns, frontend-design-direction, frontend-slides, ui-to-vue, vite-patterns, nextjs-turbopack, nuxt4-patterns, design-system, liquid-glass-design, motion-ui | Web/移动端开发 |
| **后端** | backend-patterns, fastapi-patterns, django-patterns, nestjs-patterns, springboot-patterns, quarkus-patterns, laravel-patterns, rust-patterns, golang-patterns, dotnet-patterns | API/服务端开发 |
| **数据库** | postgres-patterns, mysql-patterns, redis-patterns, prisma-patterns, database-migrations, clickhouse-io | 数据持久化 |
| **测试** | e2e-testing, browser-qa, python-testing, rust-testing, golang-testing, csharp-testing, fsharp-testing, cpp-testing, kotlin-testing, perl-testing | 质量保障 |
| **安全** | security-review, security-scan, security-bounty-hunter, hipaa-compliance, gateguard, safety-guard, defi-amm-security, llm-trading-agent-security | 安全审计 |
| **架构** | hexagonal-architecture, android-clean-architecture, architecture-decision-records, coding-standards, error-handling | 架构设计 |
| **AI/ML** | mle-workflow, deep-research, eval-harness, prompt-optimizer, recsys-pipeline-architect, foundation-models-on-device | AI/ML 工程 |
| **DevOps** | docker-patterns, deployment-patterns, git-workflow, github-ops, mcp-server-patterns, flox-environments, terminal-ops | 基础设施 |
| **iOS** | swiftui-patterns, swift-concurrency-6-2, swift-actor-persistence, swift-protocol-di-testing, compose-multiplatform-patterns | Apple 平台 |
| **业务** | finance-billing-ops, logistics-exception-management, inventory-demand-planning, returns-reverse-logistics, production-scheduling | 企业业务 |
| **内容** | article-writing, content-engine, seo, brand-voice, video-editing, manim-video, remotion-video-creation | 内容创作 |

### 调用方式

直接说需要做的事，opencode 会自动匹配。例如：
- "帮我审查这个后端 API 的安全漏洞" → 触发 `/security-review`
- "写一个 SwiftUI 的列表页面" → 触发 `/swiftui-patterns`
- "设计数据库迁移方案" → 触发 `/database-migrations`

---

## 2. Superpowers

| 属性 | 内容 |
|------|------|
| **GitHub** | https://github.com/obra/superpowers |
| **Stars** | ~41k |
| **安装路径** | `~/.claude/skills/superpowers/` |
| **Skill 数量** | 14 个 |

### 功能介绍

第二大社区 Skill 库，提供完整的**软件开发全生命周期流程**：从头脑风暴、需求分析、TDD 开发、子 Agent 实现、代码审查、到合并发布。每个 skill 可以链式调用，形成一个完整的工作流。

### Skill 清单

| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/brainstorming` | 交互式需求探索，提取真实需求规格 | "帮我 brainstorm 一下这个功能" |
| `/writing-plans` | 将需求拆分为 2-5 分钟可实现的任务 | "把需求写成开发计划" |
| `/test-driven-development` | TDD 红-绿-重构循环 | "用 TDD 开发这个功能" |
| `/subagent-driven-development` | 子 Agent 驱动开发 + 双阶段代码审查 | "派个子 Agent 去实现这个模块" |
| `/verification-before-completion` | 完成前的自动验证 | "验证这个实现是否符合需求" |
| `/requesting-code-review` | 请求 PR 审查 | "帮我 review 这个 PR" |
| `/receiving-code-review` | 接收审查意见并修改 | "按 review 意见修改代码" |
| `/systematic-debugging` | 系统化调试循环 | "这个 bug 帮我系统地排查一下" |
| `/dispatching-parallel-agents` | 并行派发多个子 Agent | "同时做 A 和 B 两个任务" |
| `/executing-plans` | 执行开发计划 | "开始执行这个开发计划" |
| `/finishing-a-development-branch` | 完成分支并准备合并 | "做完这个分支，准备合并" |
| `/using-git-worktrees` | Git worktree 管理 | "用 worktree 模式开始新功能" |
| `/writing-skills` | 创建自定义 Skill | "帮我创建一个新的 skill" |
| `/using-superpowers` | Superpowers 使用指南 | "告诉我怎么用 superpowers" |

### 完整流程示例

```
brainstorming → writing-plans → subagent-driven-development
  → requesting-code-review → receiving-code-review → finishing-a-development-branch
```

---

## 3. GStack

| 属性 | 内容 |
|------|------|
| **GitHub** | https://github.com/garrytan/gstack |
| **Stars** | ~66k |
| **安装路径** | `~/.claude/skills/gstack/` |
| **Skill 数量** | 57 个 |

### 功能介绍

YC CEO Garry Tan 开源的个人 AI 编码工具集。将 AI 变成**虚拟工程团队**——CEO、设计师、QA、运维等角色。覆盖从规划、设计、开发、测试、部署、到监控的全流程。

### Skill 分类

#### 规划审查
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/plan-ceo-review` | CEO 视角审查——挑战前提、扩展范围 | "帮我从 CEO 角度审查这个方案" |
| `/plan-eng-review` | 架构评审——锁定数据流、边界条件、测试覆盖 | "帮我做架构评审" |
| `/plan-design-review` | 设计评审——评分+优化方案 | "审查一下这个设计方案" |
| `/plan-devex-review` | 开发者体验审查 | "评审这个 API 的开发者体验" |
| `/plan-tune` | 调整问题询问频率和个人画像 | "调一下你的提问偏好" |

#### 创业/产品
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/office-hours` | YC 式创业答疑——6 个强力问题 | "帮我做一次 office hours" |
| `/design-consultation` | 建立完整设计系统 | "为我的产品设计一套设计系统" |
| `/design-shotgun` | 多方案设计探索 | "给这个页面出几个不同风格的设计" |
| `/design-html` | 设计稿→生产级 HTML/CSS | "把这个设计变成 HTML" |
| `/design-review` | 视觉 QA——找间距、层次、交互问题 | "检查这个页面视觉有没有问题" |

#### 测试/QA
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/browse` | 浏览器自动化导航 | "打开这个页面看看" |
| `/qa` | 全面 QA 测试（发现+修复验证） | "对这个页面做一轮 QA" |
| `/qa-only` | 只报告不修复 | "只报告 bug，不用修" |
| `/scrape` | 网页数据抓取 | "抓取这个页面的数据" |
| `/setup-browser-cookies` | 导入浏览器 Cookie 用于测试 | "导一下 cookie，我要测试登录态" |

#### 发布/部署
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/ship` | 合并+创建 PR | "帮我 ship 这个分支" |
| `/land-and-deploy` | 合并+等待 CI+验证生产环境 | "合并并部署到生产" |
| `/canary` | 灰度发布监控 | "启动灰度监控" |
| `/setup-deploy` | 配置部署设置 | "配置部署" |

#### 安全
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/cso` | 安全审计（密钥/依赖/CI/CD/LLM） | "做一次安全审计" |
| `/careful` | 破坏性命令警告 | "开启小心模式" |
| `/freeze` | 限制编辑范围到指定目录 | "冻结编辑范围到 src/" |
| `/guard` | 完全保护模式 | "开启完全保护" |

#### 文档
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/document-generate` | 从零生成文档 | "给这个模块写文档" |
| `/document-release` | 发布后更新文档 | "更新发布后的文档" |

#### 其他
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/make-pdf` | Markdown→PDF | "把这篇文档转成 PDF" |
| `/retro` | 周回顾分析 | "这周做了什么回顾一下" |
| `/health` | 代码健康评分 | "检查代码健康状况" |
| `/review` | PR 预合并审查 | "审查这个 PR" |
| `/investigate` | 系统化调试 | "调查这个生产问题" |
| `/codex` | 用 OpenAI Codex 做第二意见 | "让 codex 也看看这个" |
| `/learn` | 管理项目经验教训 | "我们学到了什么" |

---

## 4. Matt Pocock Skills

| 属性 | 内容 |
|------|------|
| **GitHub** | https://github.com/mattpocock/skills |
| **Stars** | ~138k |
| **安装路径** | `~/.claude/skills/mattpocock-skills/` |
| **Skill 数量** | 28 个 |

### 功能介绍

TypeScript 教父 Matt Pocock 的个人 skill 合集，聚焦**工程效率工具箱**。每个 skill 解决一个具体的工程痛点，质量极高，代码风格出色。

### Skill 清单

#### 工程（engineering）
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/diagnose` | 严格调试循环：复现→最小化→假设→仪表→修复→回归测试 | "诊断这个bug" |
| `/tdd` | 红-绿-重构 TDD 循环 | "用 TDD 实现" |
| `/review` | 双轴审查：代码规范 vs 需求匹配 | "review 这些改动" |
| `/prototype` | 快抛弃原型 | "帮我快速验证这个想法" |
| `/zoom-out` | 宏观代码视角 | "帮我 zoom out 看看全貌" |
| `/to-prd` | 会话→PRD 文档 | "把讨论写成 PRD" |
| `/to-issues` | 需求拆解为 issue | "拆成 issue" |
| `/triage` | Issue 分类管理 | "给这些 issue 分类" |
| `/improve-codebase-architecture` | 架构改进机会挖掘 | "帮我找架构改进点" |
| `/grill-with-docs` | 基于领域文档的拷问 | "基于文档拷问我的方案" |
| `/setup-matt-pocock-skills` | 初始化这些 skill 的配置 | "初始化技能配置" |

#### 生产力（productivity）
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/grill-me` | 方案拷问：逐层追问直到达成共识 | "拷问一下我的方案" |
| `/handoff` | 会话→交接文档 | "整理成交接文档" |
| `/caveman` | 极简模式（省 75% token） | "开启 caveman 模式" |
| `/write-a-skill` | 创建自定义 skill | "帮我创建一个 skill" |

#### 个人（personal）
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/obsidian-vault` | 管理 Obsidian 笔记 | "查一下 Obsidian 笔记" |
| `/edit-article` | 编辑和优化文章 | "帮我润色这篇文章" |

#### 杂项（misc）
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/setup-pre-commit` | 配置 git hooks | "设置 pre-commit 钩子" |
| `/scaffold-exercises` | 创建练习脚手架 | "创建练习题结构" |
| `/migrate-to-shoehorn` | 迁移测试断言 | "迁移到 shoehorn" |
| `/git-guardrails-claude-code` | 禁止危险 git 命令 | "装一下 git 保护" |

#### 写作（in-progress）
| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/writing-beats` | 叙事式文章结构 | "以叙事方式组织这篇文章" |
| `/writing-fragments` | 碎片化创意收集 | "帮我把这些碎片想法整理出来" |
| `/writing-shape` | 草稿→成文 | "帮我把草稿变成完整文章" |

---

## 5. Andrej Karpathy Skills

| 属性 | 内容 |
|------|------|
| **GitHub** | https://github.com/multica-ai/andrej-karpathy-skills |
| **Stars** | ~141k |
| **安装路径** | `~/.claude/skills/andrej-karpathy-skills/` |
| **Skill 数量** | 1 个（全局 CLAUDE.md） |

### 功能介绍

基于 Karpathy 对 LLM 编码经验的观察提炼而成的**编码行为规范**。不是传统意义上的 skill 合集，而是一份经过验证的 `CLAUDE.md` 配置，指导 AI 更好地理解代码库、避免常见陷阱、提高代码质量。

### 核心原则

- 先理解再修改：不要跳过代码阅读直接写代码
- 小步提交：频繁提交小改动，而不是一次性大改
- 优先使用现有工具和库：不要重新发明轮子
- 测试先行：关键逻辑必须有测试覆盖

### 调用方式

安装后自动生效（全局行为规范），无需手动调用。

---

## 6. Understand-Anything

| 属性 | 内容 |
|------|------|
| **GitHub** | https://github.com/Lum1104/Understand-Anything |
| **Stars** | ~17k |
| **安装路径** | `~/.claude/skills/understand-anything/` |
| **Skill 数量** | 8 个 |

### 功能介绍

把任何代码库变成**交互式知识图谱**。通过图谱可视化架构、组件关系和领域边界，解决"看不懂代码库"的问题。

### Skill 清单

| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/understand` | 扫描代码库生成交互式知识图谱 | "帮我理解这个项目" |
| `/understand-chat` | 基于知识图谱的代码问答 | "这个模块在做什么？" |
| `/understand-dashboard` | 启动 Web 版知识图谱仪表盘 | "打开代码可视化面板" |
| `/understand-diff` | 分析 diff 改动的影响范围 | "这次改动的风险是什么？" |
| `/understand-domain` | 提取业务领域知识图谱 | "帮我把业务逻辑画成图谱" |
| `/understand-explain` | 深入解释某个文件/函数/模块 | "给我解释这个函数" |
| `/understand-knowledge` | 分析 LLM Wiki 知识库 | "分析这个知识库" |
| `/understand-onboard` | 为新成员生成入职指南 | "为新成员写 onboarding 文档" |

---

## 7. Academic Research Skills

| 属性 | 内容 |
|------|------|
| **GitHub** | https://github.com/Imbad0202/academic-research-skills |
| **Stars** | ~19k |
| **安装路径** | `~/.claude/skills/academic-research-skills/` |
| **Skill 数量** | 4 个 |

### 功能介绍

完整的**学术研究全流程**——从深度调研到论文撰写、同行评审、终稿输出。13 Agent 驱动的深度研究管线 + 12 Agent 论文写作管线 + 5 角色同行评审。

### Skill 清单

| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/deep-research` | 13 Agent 深度研究管线。7 种模式：全面研究、快速简报、论文审查、文献综述、事实核查、苏格拉底式研究、系统综述（含 Meta 分析） | "帮我研究一下这个课题" |
| `/academic-paper` | 12 Agent 论文写作管线。10 种模式、6 种论文类型、LaTeX/DOCX 输出 | "帮我写一篇论文" |
| `/academic-paper-reviewer` | 5 角色同行评审（主编+3 审稿人+魔鬼代言人） | "帮我评审这篇论文" |
| `/academic-pipeline` | 完整工作流编排器：研究→撰写→审查→修改→终稿 | "走一遍完整学术研究流程" |

---

## 8. Anthropic 官方 Skills

| 属性 | 内容 |
|------|------|
| **GitHub** | https://github.com/anthropics/skills |
| **Stars** | —（官方仓库） |
| **安装路径** | `~/.claude/skills/anthropic-skills/` |
| **Skill 数量** | 18 个 |

### 功能介绍

Anthropic 官方维护的 Skill 仓库，包含高质量的生产环境就绪 skill。

### Skill 清单

| Skill | 功能 | 调用方式 |
|-------|------|---------|
| `/docx` | 生成 .docx 文档 | "帮我生成 Word 文档" |
| `/xlsx` | 生成 .xlsx 表格 | "创建 Excel 表格" |
| `/pdf` | 生成 PDF 文件 | "生成 PDF" |
| `/pptx` | 生成 PPT 演示文稿 | "帮我做 PPT 幻灯片" |
| `/algorithmic-art` | 算法艺术生成 | "生成算法艺术作品" |
| `/canvas-design` | Canvas 设计 | "设计一个 Canvas 画布" |
| `/webapp-testing` | Web 应用测试 | "测试这个 Web 应用" |
| `/mcp-builder` | MCP 服务器构建 | "帮我搭一个 MCP 服务器" |
| `/claude-api` | Claude API 集成 | "帮我写 Claude API 调用" |
| `/skill-creator` | 创建自定义 skill（官方版） | "创建一个 skill" |
| `/web-artifacts-builder` | 网络构件构建 | "创建 Web 构件" |
| `/frontend-design` | 前端设计 | "帮我设计前端界面" |
| `/theme-factory` | 主题工厂 | "创建一个主题" |
| `/slack-gif-creator` | Slack GIF 创建 | "创建一个 Slack GIF" |
| `/internal-comms` | 内部沟通 | "写内部通讯" |
| `/doc-coauthoring` | 文档协作 | "协作编辑文档" |
| `/brand-guidelines` | 品牌指南 | "制定品牌指南" |

---

## 9. 如何正确调用 Skill

### 在 OpenCode 中

opencode 会自动扫描 `~/.claude/skills/`、`~/.config/opencode/skills/`、`.opencode/skills/` 下的所有 SKILL.md。

**不需要手动调用**——用自然语言描述你要做的事即可自动匹配。

### 推荐的说话方式

```
"这个 CRUD API 帮我做一轮安全检查"           → /security-review
"把这段代码做成可交互的知识图谱"               → /understand
"帮我把这几天的讨论整理成 PRD 文档"              → /to-prd
"用 TDD 方式开发这个功能"                       → /tdd
"帮我 review 这个分支，从 CEO 角度审查方案"       → /plan-ceo-review
"帮我从架构角度评审一下这个设计方案"               → /plan-eng-review
"我想做一轮学术研究，写一篇论文并找审稿人review"    → /academic-pipeline
"帮我生成一份 Word 文档，里面包含这个功能说明"      → /docx
```

### 按场景选择 Skill

| 场景 | 推荐 Skill 合集 | 推荐 Skill |
|------|----------------|-----------|
| 接手新项目，需要快速理解 | Understand-Anything | `/understand` `/understand-onboard` |
| 想一个产品方案 | gstack | `/office-hours` `/plan-ceo-review` |
| 开始写代码 | Superpowers | `/brainstorming` → `/writing-plans` |
| TDD 开发 | Matt Pocock / Superpowers | `/tdd` |
| 调试顽固 bug | Matt Pocock | `/diagnose` |
| 做架构评审 | GStack | `/plan-eng-review` |
| 写 API 文档 | Everything Claude Code | `/api-design` |
| 做自动化 QA | GStack | `/qa` `/browse` |
| 学术研究到论文 | Academic Research | `/academic-pipeline` |
| 写文章/内容 | Matt Pocock | `/writing-shape` `/edit-article` |
| 代码安全审计 | Everything Claude Code | `/security-review` |
| 生成文档/PPT/表格 | Anthropic 官方 | `/docx` `/pptx` `/xlsx` |

### 注意

- 同名 skill 按优先级：项目级 > 全局级 > `~/.claude/skills/`
- 安装新合集后**重启 opencode** 才能识别
