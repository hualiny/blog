# 部署说明

本站为 **静态站点**（`output: 'static'`），将 `dist/` 部署到任意静态托管即可。

## 环境变量

构建时会读取（见 `astro.config.ts`）：

| 变量 | 说明 |
|------|------|
| `SITE_URL` | 站点完整 URL，如 `https://username.github.io` 或自定义域名 |
| `BASE_PATH` | 子路径部署时填写，如 `/blog`；根路径部署可留空或 `/` |

## GitHub Pages

仓库已包含 [`.github/workflows/deploy-pages.yml`](.github/workflows/deploy-pages.yml)：推送到 `main` / `master` 时自动 `bun install` → `bun run build` → 上传 `dist` 并发布。

1. 仓库 **Settings → Pages**：**Source** 选择 **GitHub Actions**。  
2. **Settings → Secrets and variables → Actions → Variables** 中配置 `SITE_URL`（以及按需配置 `BASE_PATH`）。

## 其他平台

在 **Cloudflare Pages**、**Vercel**、**Netlify** 等平台连接同一仓库时，构建命令使用 `bun run build`，输出目录为 `dist`，并在面板中设置与上文一致的 `SITE_URL` / `BASE_PATH`。更细的适配说明见主题文档：[部署](https://astro-pure.js.org/docs/setup/deployment)。
