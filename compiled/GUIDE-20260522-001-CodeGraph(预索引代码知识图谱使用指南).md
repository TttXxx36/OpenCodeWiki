---
id: GUIDE-20260522-001
title: CodeGraph - Pre-indexed Code Knowledge Graph
title_zh: CodeGraph - 预索引代码知识图谱使用指南
category: GUIDE
tags: [tool, ai-ml, productivity, reference, opencode, claude-code]
status: published
created: 2026-05-22
updated: 2026-05-22
summary: Pre-indexed code knowledge graph for AI coding agents — fewer tokens, fewer tool calls, 100% local
source: https://github.com/colbymchenry/codegraph
difficulty: intermediate
---

# CodeGraph - Pre-indexed Code Knowledge Graph (预索引代码知识图谱使用指南)

> 仓库: https://github.com/colbymchenry/codegraph
> Stars: ~12.4k | 作者: Colby McHenry | 安装位置: `~/.claude/skills/codegraph/`

## 简介

CodeGraph 是一个预索引的代码知识图谱工具。它在 AI 工作之前**提前扫描整个代码库**，生成结构化的知识图谱。之后 AI 直接查询图谱就能理解代码，不需要反复调用 grep/read 工具。

**关键指标**：
- 减少 94% 的工具调用次数
- 加快 77% 的代码探索速度
- 100% 本地运行，代码不离开本机

## 工作原理

| 传统方式 | CodeGraph 方式 |
|---------|---------------|
| AI 需要理解代码 → 反复 grep/read → 大量 Token 消耗 | 提前索引代码库 → 生成知识图谱 → AI 直接查图谱 → 极少 Token |

## 使用方法

已安装到 `~/.claude/skills/codegraph/`，重启 opencode 后 AI 会自动使用它。

### 在项目中启用

```bash
# 在项目根目录运行（按项目 README 配置）
cd ~/.claude/skills/codegraph
# 按照指示指向你的项目目录生成索引
```

### 调用方式

不需要手动调用。AI 在理解代码时会自动利用 CodeGraph 的预索引数据。

```text
用户问："这个模块的架构是什么样的？"
→ AI 直接查 CodeGraph 图谱回答，不需要 grep 文件

用户问："帮我改一下这个函数"
→ AI 先查图谱确认函数位置和依赖关系，再修改
```

## 适用场景

- 大型代码库（10万+ 行代码）
- 需要频繁切换上下文的长会话
- Token 成本敏感的项目
- 新成员快速理解项目结构
