# 知行园

个人技术博客，使用 [Astro](https://astro.build/) 与 [Astro Theme Pure](https://github.com/cworld1/astro-theme-pure) 搭建，静态生成，侧重文章、搜索与阅读体验。

## 本地开发

环境：[Bun](https://bun.sh/)（推荐）或 Node.js 18+。

```shell
bun install
bun dev
```

常用命令：

| 命令 | 说明 |
|------|------|
| `bun dev` | 本地预览 |
| `bun run build` | 生产构建，输出 `dist/` |
| `bun preview` | 本地预览构建结果 |
| `bun pure new` | 通过 astro-pure 创建新文章（若已配置） |

构建脚本会执行 `astro-pure check`、`astro check` 与 `astro build`。

部署（GitHub Pages、环境变量、其他平台等）见 [deploy.md](./deploy.md)。

## 主题致谢

博客界面与大量功能来自开源主题 **[Astro Theme Pure](https://github.com/cworld1/astro-theme-pure)**（[npm: astro-pure](https://www.npmjs.com/package/astro-pure)）。感谢作者 [cworld1](https://github.com/cworld1) 与贡献者的维护与文档。主题官方文档与组件说明见 [astro-pure.js.org/docs](https://astro-pure.js.org/docs)。
