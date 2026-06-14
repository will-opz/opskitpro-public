# OpsKitPro Public

这是 OpsKitPro 的**公开知识库仓库**，用于构建并发布 `kb.opskitpro.com`。

它只保存已经整理完成、可以长期公开引用的内容。草稿、发布队列、私有记录和自动化状态由私有仓库 `opskitpro-ops` 管理。

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

新的结构化发布状态已经迁入 `opskitpro-ops` Django 后台。`opskitpro-notes` 只作为历史 Markdown 来源或临时 Obsidian 工作区使用。

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
4. GitHub Actions 构建 Quartz 并部署到 AWS Lightsail。
5. Nginx 通过 `kb.opskitpro.com` 提供静态文件。

## 仓库关系

- 主站仓库：`https://github.com/will-opz/opskitpro`
- 私有后台仓库：`https://github.com/will-opz/opskitpro-ops`
- 本仓库只保留可公开引用的内容

## 部署

`main` 分支 push 后自动发布到：

```text
https://kb.opskitpro.com
```

GitHub Actions 使用以下 repository secrets：

- `LIGHTSAIL_HOST`
- `LIGHTSAIL_USER`
- `LIGHTSAIL_SSH_KEY`
