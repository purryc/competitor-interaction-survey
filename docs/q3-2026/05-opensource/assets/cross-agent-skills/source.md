# 跨 agent 素材账本

抓取日期：2026-09-09（America/Toronto）  
产品：Open Design v0.19.0 本地 CLI  
官方来源：[Open Design GitHub](https://github.com/nexu-io/open-design)

| 文件 | 实际状态 | 实际命令 | 证据边界 |
|---|---|---|---|
| `01-codex-claude-cursor-dry-run.png` | 三个目标的汇总预览 | `od mcp install ... --print` | 汇总图，不等于三端安装或加载 |
| `02-codex-dry-run.png` | Codex 目标命令预览 | `od mcp install codex --print` | 只打印目标配置；未改 `~/.codex` |
| `03-claude-dry-run.png` | Claude Code 目标命令预览 | `od mcp install claude --print` | 只打印目标配置；未改用户配置 |
| `04-cursor-dry-run.png` | Cursor 配置文件预览 | `od mcp install cursor --print` | 显示会写入的位置；未实际写入 |

所有用户主目录均在画面中替换为 `<USER_HOME>`。未在 Codex、Claude Code、Cursor 内分别加载和调用同一 MCP/skill，故为 PARTIAL。
