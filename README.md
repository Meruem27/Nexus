# Nexus

一个基于 **Hugo + PaperMod** 的个人 Markdown 笔记平台。

## 使用方式

1. 将仓库推送到 GitHub 的 `main` 分支。
2. 在仓库的 **Settings → Pages → Build and deployment** 中选择 **GitHub Actions**。
3. 在 `docs/` 文件夹中新建或上传 `.md` 文件。
4. 推送后，`.github/workflows/hugo.yml` 会自动构建并发布到 GitHub Pages。

### Markdown 示例

```markdown
---
title: "我的新笔记"
date: 2026-08-11
tags: [学习]
---

正文内容。
```

### Mermaid 示例

````markdown
```mermaid
flowchart LR
  A[开始] --> B[完成]
```
````

## 本地预览

安装 Hugo Extended `0.146.0` 或更高版本，并确保已拉取主题子模块：

```powershell
git submodule update --init --recursive
hugo server -D
```

浏览器打开 `http://localhost:1313/`。

## 目录说明

- `docs/`：所有笔记 Markdown 文件
- `hugo.yaml`：站点与 PaperMod 配置
- `assets/css/extended/nexus.css`：Nexus 的轻量视觉覆盖
- `layouts/partials/extend_head.html`：Mermaid 与 favicon
- `.github/workflows/hugo.yml`：GitHub Pages 自动部署
- `themes/PaperMod/`：PaperMod Git 子模块
