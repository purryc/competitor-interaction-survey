# 开源阵营素材出处总表

抓取日期均为 2026-09-09（America/Toronto）。“官方性”中的“官方产品自测”表示运行官方发布的软件，不表示厂商审核了本报告。

| 文件路径 | 对应特性 | 来源 URL | 时间码/页面状态 | 官方性 | 证据边界 | 抓取日期 |
| --- | --- | --- | --- | --- | --- | --- |
| [assets/openwork-desktop/01-entry-global-ui.png](../../../media/q3-2026/05-opensource/assets/openwork-desktop/01-entry-global-ui.png) | OpenWork 桌面端 | https://github.com/different-ai/openwork/releases/tag/v0.18.44 | 新会话全局 UI | 官方产品自测 | 真实空态 | 2026-09-09 |
| [assets/openwork-desktop/02-delegate-ready.png](../../../media/q3-2026/05-opensource/assets/openwork-desktop/02-delegate-ready.png) | OpenWork 桌面端 | https://github.com/different-ai/openwork/releases/tag/v0.18.44 | 提示已输入、未执行 | 官方产品自测 | 只证明委托内容 | 2026-09-09 |
| [assets/openwork-desktop/03-running.png](../../../media/q3-2026/05-opensource/assets/openwork-desktop/03-running.png) | OpenWork 桌面端 | https://github.com/different-ai/openwork/releases/tag/v0.18.44 | Working 6s / Wrote | 官方产品自测 | 同一隔离成功链过程态 | 2026-09-09 |
| [assets/openwork-desktop/04-success-result.png](../../../media/q3-2026/05-opensource/assets/openwork-desktop/04-success-result.png) | OpenWork 桌面端 | https://github.com/different-ai/openwork/releases/tag/v0.18.44 | Wrote / Read / 完成回复 | 官方产品自测 | agent 报告成功，另有产物面板复核 | 2026-09-09 |
| [assets/openwork-desktop/05-artifact-preview.png](../../../media/q3-2026/05-opensource/assets/openwork-desktop/05-artifact-preview.png) | OpenWork 桌面端 | https://github.com/different-ai/openwork/releases/tag/v0.18.44 | 内置文件预览 | 官方产品自测 | 同一隔离成功链产物 | 2026-09-09 |
| [assets/openwork-desktop/06-exit-new-session.png](../../../media/q3-2026/05-opensource/assets/openwork-desktop/06-exit-new-session.png) | OpenWork 桌面端 | https://github.com/different-ai/openwork/releases/tag/v0.18.44 | 退出到新会话 | 官方产品自测 | 旧会话仍在侧栏 | 2026-09-09 |
| [assets/openwork-desktop/04-failure-no-result.png](../../../media/q3-2026/05-opensource/assets/openwork-desktop/04-failure-no-result.png) | OpenWork 桌面端 | https://github.com/different-ai/openwork/releases/tag/v0.18.44 | no result arrived / Resume | 官方产品自测 | 另一次失败链，不与成功链拼接 | 2026-09-09 |
| [assets/openwork-desktop/05-artifact-result.png](../../../media/q3-2026/05-opensource/assets/openwork-desktop/05-artifact-result.png) | OpenWork 桌面端 | https://github.com/different-ai/openwork/releases/tag/v0.18.44 | MacDown 外部查看 | 本机派生核验 | 非 OpenWork UI、非同一隔离链 | 2026-09-09 |
| [assets/cross-agent-skills/01-codex-claude-cursor-dry-run.png](../../../media/q3-2026/05-opensource/assets/cross-agent-skills/01-codex-claude-cursor-dry-run.png) | 跨 agent 技能复用 | https://github.com/nexu-io/open-design | 三端 `--print` 汇总 | 官方 CLI 自测 | dry-run，不等于安装/加载 | 2026-09-09 |
| [assets/cross-agent-skills/02-codex-dry-run.png](../../../media/q3-2026/05-opensource/assets/cross-agent-skills/02-codex-dry-run.png) | 跨 agent 技能复用 | https://github.com/nexu-io/open-design | Codex 配置预览 | 官方 CLI 自测 | 未改用户配置 | 2026-09-09 |
| [assets/cross-agent-skills/03-claude-dry-run.png](../../../media/q3-2026/05-opensource/assets/cross-agent-skills/03-claude-dry-run.png) | 跨 agent 技能复用 | https://github.com/nexu-io/open-design | Claude Code 配置预览 | 官方 CLI 自测 | 未改用户配置 | 2026-09-09 |
| [assets/cross-agent-skills/04-cursor-dry-run.png](../../../media/q3-2026/05-opensource/assets/cross-agent-skills/04-cursor-dry-run.png) | 跨 agent 技能复用 | https://github.com/nexu-io/open-design | Cursor 配置预览 | 官方 CLI 自测 | 未写 `.cursor/mcp.json` | 2026-09-09 |
| [assets/opendesign-cli/01-headless-cli-status.png](../../../media/q3-2026/05-opensource/assets/opendesign-cli/01-headless-cli-status.png) | OpenDesign CLI | https://github.com/nexu-io/open-design/releases/tag/open-design-v0.19.0 | daemon status + MCP help | 官方 CLI 自测 | 原生 Terminal；未提交生成任务 | 2026-09-09 |
| [assets/opendesign-cli/02-clean-global-ui.png](../../../media/q3-2026/05-opensource/assets/opendesign-cli/02-clean-global-ui.png) | OpenDesign CLI | https://github.com/nexu-io/open-design/releases/tag/open-design-v0.19.0 | 桌面全局 UI | 官方产品自测 | 证明桌面壳，不证明 headless 结果 | 2026-09-09 |
| [assets/opendesign-cli/03-headless-artifact-complete.png](../../../media/q3-2026/05-opensource/assets/opendesign-cli/03-headless-artifact-complete.png) | OpenDesign CLI | https://github.com/nexu-io/open-design/releases/tag/open-design-v0.19.0 | project/artifact/files 完成态 | 自建实时 stdout 查看器 + 官方 CLI | 本地 HTML fixture；非模型生成、非原生 Terminal | 2026-09-09 |
| [assets/opendesign-cli/clip.mp4](../../../media/q3-2026/05-opensource/assets/opendesign-cli/clip.mp4) | OpenDesign CLI | https://github.com/nexu-io/open-design/releases/tag/open-design-v0.19.0 | 00:00–00:07.68 | 自建实时 stdout 查看器 + 官方 CLI | 实际子进程输出；非静态回放、非原生 Terminal UI | 2026-09-09 |
| [assets/design-token-library/01-apple-token-picker.png](../../../media/q3-2026/05-opensource/assets/design-token-library/01-apple-token-picker.png) | 151 套设计系统 token 库 | https://github.com/nexu-io/open-design | Apple picker / palette | 官方产品自测 | 只证明可选择，不证明应用后产物 | 2026-09-09 |
| [assets/plugin-marketplace/01-scaffold-created.png](../../../media/q3-2026/05-opensource/assets/plugin-marketplace/01-scaffold-created.png) | 插件市场与自扩展 | https://open-design.ai/zh/blog/open-design-0-8-0-everything-is-a-plugin/ | scaffold 完成 | 官方 CLI 自测 | 本地 `_work` 文件 | 2026-09-09 |
| [assets/plugin-marketplace/02-validate-warning.png](../../../media/q3-2026/05-opensource/assets/plugin-marketplace/02-validate-warning.png) | 插件市场与自扩展 | https://open-design.ai/zh/blog/open-design-0-8-0-everything-is-a-plugin/ | validate `ok:true` + warning | 官方 CLI 自测 | warning 未解决 | 2026-09-09 |
| [assets/plugin-marketplace/03-pack-prepublish-stop.png](../../../media/q3-2026/05-opensource/assets/plugin-marketplace/03-pack-prepublish-stop.png) | 插件市场与自扩展 | https://github.com/nexu-io/open-design/releases/tag/open-design-v0.8.0 | pack 完成 / pre-publish stop | 官方 CLI 自测 | 未发布、未开 PR | 2026-09-09 |
| [assets/community-issues/01-opendesign-login-required-6599.png](../../../media/q3-2026/05-opensource/assets/community-issues/01-opendesign-login-required-6599.png) | 社区分歧点 | https://github.com/nexu-io/open-design/issues/6599 | closed issue 页面 | GitHub 原始 issue | 页面截图 + API 元数据交叉核验 | 2026-09-09 |
| [assets/community-issues/02-opendesign-byok-local-2986.png](../../../media/q3-2026/05-opensource/assets/community-issues/02-opendesign-byok-local-2986.png) | 社区分歧点 | https://github.com/nexu-io/open-design/issues/2986 | open / p1 issue 页面 | GitHub 原始 issue | 页面截图 + API 元数据交叉核验 | 2026-09-09 |
| [assets/community-issues/03-openwork-summary-loop-1103.png](../../../media/q3-2026/05-opensource/assets/community-issues/03-openwork-summary-loop-1103.png) | 社区分歧点 | https://github.com/different-ai/openwork/issues/1103 | closed issue 页面 | GitHub 原始 issue | 页面截图 + API 元数据交叉核验 | 2026-09-09 |

## 版本与事实来源

| 事实 | 来源 | 核验结果 |
|---|---|---|
| OpenWork 仓库与最新稳定版 | https://api.github.com/repos/different-ai/openwork · https://api.github.com/repos/different-ai/openwork/releases/latest | 23,437 stars；v0.18.44；published 2026-09-09T05:32:36Z |
| Open Design 仓库与最新稳定版 | https://api.github.com/repos/nexu-io/open-design · https://api.github.com/repos/nexu-io/open-design/releases/latest | 95,141 stars；0.22.1；published 2026-09-09T12:30:14Z；Apache-2.0 |
| v0.8.0 “Everything is a plugin” | https://open-design.ai/zh/blog/open-design-0-8-0-everything-is-a-plugin/ | 2026-05-22 历史发布点；不是当前版本 |
| 当前 design-system 数量 | https://github.com/nexu-io/open-design | 当前 README 与本机 v0.19.0 API 均为 151；任务书 149 为历史口径 |
| Open Design v0.12.0 品牌系统 | https://github.com/nexu-io/open-design/blob/main/apps/landing-page/app/content/blog/open-design-0-12-0-brand-backed-design-system.md | 2026-06-26；说明品牌提取与可复用 design system 流程 |

逐目录的状态说明见各 `assets/*/source.md`；真实失败与替代路径见 `SEARCH-LOG.md`。
