---
title: "开始使用 Nexus"
date: 2026-08-11T09:00:00+08:00
draft: false
description: "Nexus 的 Markdown 写作与发布说明"
tags:
  - Nexus
  - Markdown
  - Hugo
categories:
  - 指南
---

Nexus 是一个以 Markdown 为源文件、以 GitHub 为发布入口的个人知识空间。

## 写一篇新笔记

在 `docs/` 下新建 Markdown 文件，写入 front matter：

```markdown
---
title: "我的第一篇笔记"
date: 2026-08-11
tags: [读书, 思考]
categories: [随笔]
---

正文从这里开始。
```

保存并推送到 `main` 分支，GitHub Actions 会自动构建并发布网站。

## Mermaid 图表

使用 `mermaid` 代码块即可渲染流程图：

```mermaid
flowchart LR
  A[写 Markdown] --> B[推送到 GitHub]
  B --> C[GitHub Actions 构建]
  C --> D[Nexus 页面]
```

## 代码块

普通代码块会自动获得语法高亮与复制按钮：

```python
from pathlib import Path

notes = list(Path("docs").glob("**/*.md"))
print(f"发现 {len(notes)} 篇笔记")
```

> 建议一篇笔记只表达一个主题，并给它添加 1～3 个标签，之后会更容易检索。
