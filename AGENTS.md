# AI Memory Protocol
- ⚠️ 本项目与 `opskitpro-ops` 后端共用全局记忆库；这份记忆同时用于不同仓库、不同 Agent、不同会话之间同步信息。
- 启动时请强制读取相对路径 `../opskitpro-ops/.ai/index.md`，并按其中 Read Order 继续读取权威记忆。
- 至少读取 `../opskitpro-ops/.ai/memory_maintenance.md`、`../opskitpro-ops/.ai/recent_context.md`、`../opskitpro-ops/.ai/current_state.md`、`../opskitpro-ops/.ai/decisions.md` 和 `../opskitpro-ops/.ai/repositories/opskitpro-public.md`。
- 绝不要在本仓库目录创建 `.ai/` 文件夹。
- 所有任务结束后的日志、决策、风险和下一步，请统一写回 `../opskitpro-ops/.ai/session_log.md`、`../opskitpro-ops/.ai/task_board.md` 或相关 `.ai` 文件，方便下一个 Agent 接手。

## Knowledge Base Boundary

This repository is public. Only publish reviewed, public-safe knowledge base content here.

Do not commit private notes, analytics, credentials, drafts, publishing strategy, or `.ai/` memory into this repository.
