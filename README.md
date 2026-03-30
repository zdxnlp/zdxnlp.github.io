# zdxnlp.github.io

这是一个基于 Astro 的个人博客，当前使用 [Koharu](https://astro.build/themes/details/koharu/) 主题进行构建，并通过 GitHub Pages 自动部署。

## 本地开发

```bash
npm install
ASTRO_TELEMETRY_DISABLED=1 npm run dev
```

## 构建

```bash
ASTRO_TELEMETRY_DISABLED=1 npm run build
```

## 内容位置

- 站点配置：`config/site.yaml`
- 关于页：`src/pages/about.md`
- 博客文章：`src/content/blog/`

## 部署

推送到 `main` 分支后，GitHub Actions 会自动构建并发布到 GitHub Pages。

## Attribution

本项目基于 [cosZone/astro-koharu](https://github.com/cosZone/astro-koharu) 主题进行定制。

主题上游使用 `AGPL-3.0` 许可证发布，因此仓库中保留了原始 [LICENSE](./LICENSE) 文件。
