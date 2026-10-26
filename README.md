# 艾戈（Aige）

个人博客：关于 AI 模型与工具的观察和笔记。基于 [Astro](https://astro.build) 构建，静态站点，部署在 Cloudflare Pages，域名 <https://aige.lol>。

## 本地开发

```bash
npm install
npm run dev      # 开发服务器
npm run build    # 构建到 dist/
npm run preview  # 预览构建结果
```

## 写文章

在 `src/content/blog/` 下新建 Markdown 文件，frontmatter 格式：

```yaml
---
title: 文章标题
description: 一句话摘要
date: 2026-01-01
---
```

## 部署

Cloudflare Pages 直接上传 `dist/`：

```bash
npm run build
npx wrangler pages deploy dist --project-name aige
```

自定义域名 `aige.lol` 在 Cloudflare Pages 项目设置中绑定。
