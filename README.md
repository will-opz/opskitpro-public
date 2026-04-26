# OpsKitPro Public

这是 OpsKitPro 的**公开发布仓库**，用于站点构建、文章发布和工具说明。

## 这里放什么

- `content/02_Articles/`：已发布文章
- `content/03_Tools/`：工具说明与使用手册
- `content/05_Assets/`：公开展示资源
- `docs/`：站点与项目文档
- `quartz/`：Quartz 站点源码

## 不放什么

- 原始 Inbox
- 未整理草稿
- 内部排障记录
- 模板草案
- 带环境敏感信息的内容

这些内容都在私有仓库 `opskitpro-notes`。

## 本地开发

```bash
npm ci
npm run check
npm test
npx quartz build --serve -d content
```

## 发布流程

1. 在本地修改文章或工具文档。
2. 通过 `npm run check` 和 `npm test`。
3. 提交到 `main`。
4. 由 GitHub Actions / Pages 构建并发布。

## 仓库关系

- 私有工作仓库：`https://github.com/will-opz/opskitpro-notes`
- 本仓库只保留可公开引用的内容
