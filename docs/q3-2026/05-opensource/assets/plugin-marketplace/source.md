# 插件市场与自扩展素材账本

抓取日期：2026-09-09（America/Toronto）  
官方来源：[v0.8.0：Everything is a plugin](https://open-design.ai/zh/blog/open-design-0-8-0-everything-is-a-plugin/) · [v0.8.0 Release](https://github.com/nexu-io/open-design/releases/tag/open-design-v0.8.0)

| 文件 | 实际状态 | 实际命令 | 证据边界 |
|---|---|---|---|
| `01-scaffold-created.png` | `q3-live-capture` 文件夹与 3 个文件被创建 | `od plugin scaffold ...` | 真实脚手架；只在 `_work/plugin-live` |
| `02-validate-warning.png` | validate 返回 `ok:true` 与 warning | `od plugin validate ...` | `context.unresolved` 未消失，不能称无警告通过 |
| `03-pack-prepublish-stop.png` | tgz 已生成并明确停在 publish 前 | `od plugin pack ...` | 未运行 `publish-repo`、`open-design-pr` 或任何发布动作 |

早先只回显命令的组合图已移入 `_work/excluded/`，不计证据。现有三帧是真实分步运行。由于有 warning 且无市场发现/上架态，标 PARTIAL。
