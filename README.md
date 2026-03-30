# DXZ 的个人博客

这是一个基于 Astro 的静态博客项目，已经预置了：

- 中文首页、博客页和关于页
- Markdown 内容集合
- RSS 与 Sitemap
- GitHub Pages 自动部署工作流

## 本地开发

```sh
npm install
npm run dev
```

默认开发地址是 `http://localhost:4321`。

## 常用命令

| 命令 | 说明 |
| :-- | :-- |
| `npm install` | 安装依赖 |
| `npm run dev` | 启动本地开发服务器 |
| `npm run build` | 生成生产环境静态文件到 `dist/` |
| `npm run preview` | 预览构建结果 |

## 文章内容

博客文章放在 `src/content/blog/` 目录下。

- 新建 `.md` 文件即可新增文章
- 文件名会成为文章链接的一部分
- `title`、`description`、`pubDate` 等字段在文章头部配置

## 部署到 GitHub Pages

1. 在 GitHub 上创建一个新仓库。
2. 在项目根目录执行：

```sh
git remote add origin <你的仓库地址>
git add .
git commit -m "init astro blog"
git push -u origin main
```

3. 打开 GitHub 仓库的 `Settings -> Pages`，把部署来源设置为 `GitHub Actions`。
4. 之后每次推送到 `main` 或 `master`，仓库里的 `.github/workflows/deploy.yml` 都会自动构建并发布。

这个工作流会自动根据你的仓库名处理 GitHub Pages 的 `base path`：

- 用户主页仓库：`<username>.github.io`
- 项目主页仓库：`<repo-name>`
