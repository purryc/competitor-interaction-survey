# 开源阵营检索日志

抓取日期均为 2026-09-09（America/Toronto）。

| 时间 | 对象 | 检索词/路径 | 结果 | 后续 |
|---|---|---|---|---|
| 2026-09-09 | OpenWork | `site:github.com/different-ai/openwork ...` | 找到官方 GitHub 仓库与 Releases；任务书约 18.8k stars 需实时复核 | GitHub API、README、release、issues |
| 2026-09-09 | OpenDesign | `site:open-design.ai OpenDesign v0.8.0 plugins CLI` | 找到官网 v0.8.0 文章及 `nexu-io/open-design`；当前仓库检索结果称 151 套设计系统，任务书 149 需按时间点区分 | 核实 release/tag/date、CLI 是否已实现、设计库目录 |
| 2026-09-09 | OpenDesign | `site:github.com open-design.ai OpenDesign CLI plugins` | 找到官方插件规范；页面明确标为 draft/awaiting review，不能当成已发布功能 | 以代码、release 和实跑为准 |
| 2026-09-09 | OpenWork release | GitHub API `repos/different-ai/openwork`、`releases/latest` | 实时仓库 23,437 stars；最新稳定 v0.18.44，2026-09-09 发布。任务书“约 18.8k”已过时 | 用实时值，保留任务书仅作草案 |
| 2026-09-09 | OpenDesign release | GitHub API `repos/nexu-io/open-design`、`releases/latest` | 实时仓库 95,141 stars；最新稳定 0.22.1，2026-09-09 发布；本机已装 app/CLI 为 0.19.0 | 明确区分上游当前版与实测版本 |
| 2026-09-09 | OpenWork 桌面 | v0.18.44 官方 DMG、`--blank-slate`、隔离临时 HOME | 实际完成三行文件创建/读取；另一次运行出现“task accepted, no result arrived · Resume” | 成功链与失败链分别记录，不拼接 |
| 2026-09-09 | OpenWork 错误截图排除 | 逐图目检 | 更新弹窗、黑 helper、错 Terminal、把失败错标 progress、含个人路径、错窗口等图移入 `_work/excluded/` | 正式目录不引用这些图 |
| 2026-09-09 | OpenDesign CLI | 独立 `OD_DATA_DIR`、`127.0.0.1:58214` | 真实创建 project；`artifacts create` 写入本地 HTML fixture；文件 API 返回 `manifestStatus=complete`；重复写返回 409 `FILE_EXISTS` | 此链证明 headless 文件通道，不是模型生成 |
| 2026-09-09 | 原生 Terminal 录屏 | `screencapture -v -V18`、窗口/区域帧抓取 | 系统录屏只生成 0.0667 秒/1 帧；窗口与区域连续抓取均被 macOS 拒绝 | 保留缺口，不把失败说成完成 |
| 2026-09-09 | CLI 实时转录录屏 | Playwright 页面实时消费实际 CLI 子进程 stdout | 生成 7.68 秒、1600×1000 H.264 MP4；完整解码通过，1/4/7 秒代表帧已目检 | 明确是自建实时转录查看器，非原生 Terminal UI |
| 2026-09-09 | 跨 agent | `od mcp install codex|claude|cursor --print` | 三端均返回目标配置预览；未写用户配置、未在三端加载 | 标 PARTIAL，dry-run 不等于安装成功 |
| 2026-09-09 | 插件生命周期 | `scaffold q3-live-capture` → `validate` → `pack` | 三步均真实运行；validate `ok:true` 但有 `context.unresolved` warning；pack 生成 974-byte tgz；publish 未运行 | 早先只回显命令的组合图已排除 |
| 2026-09-09 | 设计系统目录 | `GET /api/design-systems` | 实测 v0.19.0 返回 151 项；Apple id=`apple`，有明确色板与 published 状态 | 任务书 149 为历史值；当前口径用 151 |
| 2026-09-09 | 设计系统对照 / project import-folder | CLI 创建 `_work/token-*` 目录后 `project import-folder` | 两次均 403 `desktop import token rejected: token missing` | 改用不触碰既有项目的 managed test project |
| 2026-09-09 | 设计系统对照 / Codex | 同提示、baseline/default、`frontend-design`、Codex | run 启动；缺失 `codex-code-mode-host`，随后 GUI 工具因未批准/锁屏不可用；人工取消；0 artifact | 环境失败，不推断产品能力 |
| 2026-09-09 | 设计系统对照 / Claude Code | 同一 baseline 项目与提示 | 401 `OAuth access token has been revoked`；run failed；0 artifact | 不要求登录，不改用户凭证 |
| 2026-09-09 | 设计系统对照 / Hermes | 同一 baseline 项目与提示 | OpenRouter 401 `Missing Authentication header`；run 表面 succeeded 但 artifactCount=0 | 以产物数判定失败，不按状态词误判 |
| 2026-09-09 | 设计系统对照 / AMR Cloud | 将自建项目以 Personal Workspace headers 启动同提示 | `AMR_INSUFFICIENT_BALANCE`；0 artifact | 不充值、不购买，停止换通道 |
| 2026-09-09 | 设计系统对照 / 官方替代素材 | `site:open-design.ai design system before after tokens demo`、官方仓库/教程定向检索 | 找到官方 README “Switch a system → the next render uses the new tokens”、v0.12.0 品牌系统说明和不同案例；未找到同任务 baseline/应用后成对素材 | 不把不同案例拼成前后对照，保留 PARTIAL |
| 2026-09-09 | 社区 issues | GitHub Search/API + issue 页面 | #6599 登录强制、#2986 BYOK 私网代理、OpenWork #1103 摘要循环为争议强且有真实交互影响的三条 | 报告中区分 open/closed 和问题已修复边界 |
