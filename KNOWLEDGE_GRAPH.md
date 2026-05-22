# KNOWLEDGE_GRAPH — 交叉引用关系图

> 记录文档之间的依赖、关联、引用关系。
> 格式：`源文档 → 目标文档 : 关系说明`

---

## 当前引用关系

| 源文档 | 关系 | 目标文档 |
|--------|------|---------|
| SKILLS-20260522-001 | 概述了所有 | gstack / MattPocock / Superpowers / ECC / Karpathy / UnderstandAnything / AcademicResearch / AnthropicOfficial |
| SKILLS-20260522-001 | 配套标签体系 | TAXONOMY.md |
| TAXONOMY.md | 定义了标签 | 所有文档 |
| INDEX.md | 索引了所有 | 所有文档 |

## 按合集与 Skill 的对应关系

```
Everything Claude Code (ECC)
  ├── frontend-patterns → 前端开发
  ├── backend-patterns → 后端开发
  ├── security-review → 安全审计
  ├── api-design → API 设计
  └── ... (773 skills)

Superpowers
  ├── brainstorming → writing-plans → subagent-driven-development
  └── test-driven-development → requesting-code-review

GStack
  ├── plan-ceo-review → plan-eng-review → ship
  ├── design-shotgun → design-html → design-review
  └── qa → deploy → canary

Matt Pocock
  ├── diagnose → (debug debug debug)
  ├── tdd → (red → green → refactor)
  └── handoff → (交接文档)
```
