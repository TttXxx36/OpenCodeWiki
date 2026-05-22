# OpenCodeWiki

> 个人知识库 → 团队共享
> 最后更新: 2026-05-22 | 文档数: 1

---

## 快速导航

| 入口 | 说明 |
|------|------|
| **[INDEX.md](INDEX.md)** | 主索引（按来源 + 按主题） |
| **[KNOWLEDGE_GRAPH.md](KNOWLEDGE_GRAPH.md)** | 文档间交叉引用关系图 |
| **[TAXONOMY.md](TAXONOMY.md)** | 标签分类体系 |
| **[CHANGELOG.md](CHANGELOG.md)** | 变更记录 |
| **[compiled/](compiled/)** | 编译后的成熟文档 |
| **[raw/](raw/)** | 原始素材（待处理） |
| **[archive/](archive/)** | 过时文档归档 |

## 目录结构

```
OpenCodeWiki/
├── README.md              ← 快速入口
├── INDEX.md               ← 双索引（来源 + 主题）
├── KNOWLEDGE_GRAPH.md     ← 交叉引用
├── TAXONOMY.md            ← 标签规范
├── CHANGELOG.md           ← 变更记录
├── .template.md           ← 文档模板
├── raw/                   ← 原始素材（AI 待编译）
├── compiled/              ← 编译后成熟文档
└── archive/               ← 过时文档
```

## 使用流程

### 添加新内容

说 **「把这些文件放到知识库里」** → AI 会自动：

1. 先问：「这是原始素材还是已整理的内容？」
2. **原始素材** → 放到 `raw/`，等待后续编译
3. **已整理内容** → 放入 `compiled/`，带完整 frontmatter
4. 更新 `INDEX.md` + `KNOWLEDGE_GRAPH.md` + `CHANGELOG.md`

### 搜索内容

直接问 OpenCode：
- "知识库里关于 GStack 的内容有哪些？"
- "查一下 AI 安全相关的笔记"
- "帮我找找上周放进去的那篇文章"

### 同步到 GitHub

> GitHub 仓库待配置。说 **「同步到 GitHub」** 即可自动推送。
