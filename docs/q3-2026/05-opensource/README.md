# 开源阵营｜2026 Q3 交互素材采集

核验日期：2026-09-09（America/Toronto）  
对象：OpenWork `different-ai/openwork` · Open Design `nexu-io/open-design`  
特性素材状态：**COMPLETE 1 / PARTIAL 5 / MISSING 0**。硬件核验：COMPLETE（本轮公开来源未发现自有硬件）。

## §1 一句话结论

开源阵营把设计与办公做成可挂给不同 agent 的本地能力层：入口仍有桌面壳，但任务、skills/MCP 与产物都尽量落回文件和 CLI。

任务书数据已实时校正：OpenWork 当前稳定版为 **v0.18.44（2026-09-09）**，仓库核验时为 **23,437 stars**，任务书“约 18.8k”已过时；Open Design 当前稳定版为 **0.22.1（2026-09-09）**，本轮实际可运行版本为 **v0.19.0**。v0.8.0（2026-05-22）“Everything is a plugin”仍是历史产品转折点，不代表当前版本号。

## §2 产品矩阵

| 表面/能力 | 入口与边界 | 文件/权限边界 | 产物落点 | 本轮证据 |
|---|---|---|---|---|
| OpenWork Desktop | 桌面会话列表 + 主输入框；后端由 OpenCode 驱动 | 任务在 workspace/HOME 内执行；本轮用 `--blank-slate` 将 user-data 与 HOME 隔离到临时目录 | 本地文件，并可在内置文件面板查看 | v0.18.44 真实三行文件任务 |
| Open Design Desktop | 选择 skill、design system、agent 后发起项目 | 项目级上下文；桌面壳通过本地 daemon 与外部 agent 协作 | managed project 中的 HTML/PDF/PPTX/MP4 等真实文件 | v0.19.0 全局 UI 与 Apple picker |
| Open Design CLI / daemon | `od`、loopback HTTP、MCP | daemon 绑定 `127.0.0.1`；项目参数限定目标；是否允许外部 agent 继续由对应 agent/config 决定 | project files + artifact manifest/version | 独立数据目录真实 project/artifact 测试 |
| Design systems | 151 个 `DESIGN.md`/token package；选择器是输入约束 | 设计系统只约束选中项目/后续 render，不等于全局改主题 | 进入 prompt/context，影响后续文件 | picker 已见；同任务前后产物未取得 |
| Plugins / skills | scaffold、validate、pack、apply/publish 命令 | 本轮只写 `_work/plugin-live`；publish 明确禁止 | plugin folder 与 `.tgz`；上架需额外发布动作 | 三步真实 CLI，validate 有 warning |
| 外部 agents | Codex、Claude Code、Cursor 等由 MCP 或 CLI 接入 | Open Design 不替代理解/认证/余额；各 agent 自己的配置与权限仍独立 | 产物回写项目文件或 MCP artifact | 仅三端配置 dry-run，未证明三端实际加载 |

## §3 特性详解 ×N

### OpenWork 桌面端 — PARTIAL

- 进入：`01-entry-global-ui.png` 显示新会话、历史会话侧栏与主输入区。
- 委托：`02-delegate-ready.png` 是“创建严格三行文件并读回”的完整提示，尚未执行。
- 过程：`03-running.png` 显示真实 `Working 6s` 与 `Wrote`。
- 接管：成功链没有人工审批；另一次独立失败链 `04-failure-no-result.png` 显示 `Resume`。这两次运行不拼接。
- 产物：`04-success-result.png` 出现 `Wrote`、`Read` 与完成回复；`05-artifact-preview.png` 在产品内显示三行文件内容。
- 退出：`06-exit-new-session.png` 返回新会话，旧任务仍在侧栏可恢复。
- 一句差异点：OpenWork 把 agent 的文件动作直接放进会话时间线，失败时以 Resume 暴露接管入口；但本轮没有看到细粒度授权门或人工编辑后续跑。
- 素材缺口：任务书要求“自录屏 + 截图”，本轮只有真实截图序列，没有连续原生录屏。

### 跨 agent 技能复用 — PARTIAL

- 进入：CLI 的 `mcp install --help` 列出 Codex、Claude Code、Cursor 等目标。
- 委托：分别执行 `od mcp install codex|claude|cursor --print`。
- 过程：每个目标返回自身命令或配置文件位置，说明抽象边界是“同一个本地 MCP server + 各 agent 自己的接入格式”。
- 接管：`--print` 将写配置这一步留给操作者确认；本轮未写入任何用户配置。
- 产物：4 张 dry-run 画面，包括三端汇总和每端详情。
- 退出：命令正常结束，未产生持久配置。
- 一句差异点：复用发生在协议与配置层，不要求所有 agent 共享一个 UI；代价是认证、权限和运行能力仍由每个 agent 各自承担。
- 素材缺口：没有在三端分别加载、调用并得到同任务结果；dry-run 不能当作安装成功。

### OpenDesign 的 CLI 优先 — PARTIAL

- 进入：原生 Terminal 图显示 v0.19.0 `daemon status` 与 CLI/MCP 入口；daemon 绑定 `127.0.0.1`。
- 委托：在独立 `OD_DATA_DIR` 中执行 `project create`，再执行 `artifacts create --input <LOCAL_FIXTURE>`。
- 过程：真实 stdout 返回 project id、artifact 结构与 manifest；实时转录 MP4 记录同一命令链。
- 接管：命令可逐步停止；重复写相同路径返回 409 `FILE_EXISTS`，没有静默覆盖。
- 产物：文件 API 返回 `evidence.html`、`kind=html`、`manifestStatus=complete`。
- 退出：查看文件列表后明确结束；未调用模型、未发布、无外部写入。
- 一句差异点：桌面端更像项目与预览壳，真实可编排边界在 loopback daemon、CLI/MCP 与 project files。
- 素材缺口：`clip.mp4` 是自建页面实时消费 CLI 子进程 stdout 的录屏，非原生 Terminal UI；原生 macOS 录屏接口仅得到 1 帧，故保留 PARTIAL。fixture 产物也不等于 agent 生成设计。

### 151 套设计系统 token 库 — PARTIAL

- 进入：Open Design v0.19.0 的 picker 返回真实 catalog；API 同日返回 151 项。
- 委托：Apple 条目 id=`apple`、status=`published`，显示白/灰/深灰/蓝色板。
- 过程：已创建同提示的 baseline/default 与 Apple 两个研究测试项目。
- 接管：四条真实生成通道均在产物前失败：Codex 缺 code-mode host；Claude 401；Hermes 401；AMR 余额不足。未登录、未改凭证、未充值。
- 产物：只有 picker 截图；两个测试项目均没有对照产物。
- 退出：停止换通道；定向官方检索只找到“Switch a system → the next render uses the new tokens”的说明与不同案例，未找到同任务成对素材。
- 一句差异点：Open Design 把设计系统显式做成项目输入，而 Claude Design 强调团队样式的自动套用；本轮只验证到“可选择”，未验证到“同任务改变多少”。
- 素材缺口：缺同任务 baseline、Apple 应用后结果与前后对比图，不能用 picker 或手工换色代替。

### 插件市场与自扩展 — PARTIAL

- 进入：调用真实 `plugin scaffold` 创建 `q3-live-capture` 本地目录。
- 委托：CLI 生成 `SKILL.md`、`open-design.json`、`README.md`。
- 过程：真实 `validate` 返回 `ok:true`，同时保留 `context.unresolved` warning。
- 接管：warning 可在发布前修复；本轮没有消除它。
- 产物：真实 `pack` 生成 `q3-live-capture.tgz`（3 files，974 bytes）。
- 退出：明确停在 pre-publish；没有调用 `publish-repo`、`open-design-pr` 或市场发布。
- 一句差异点：扩展链被压缩成 agent 可调用的脚手架/校验/打包命令，但上架仍是独立的外部状态变化。
- 素材缺口：有 warning、无市场发现页与上架结果；按授权也不能实际发布。

### 社区分歧点 — COMPLETE

1. **Open Design #6599 · Mandatory Login**：围绕 local-first 产品强制登录的原则冲突；48 条评论，已随 v0.21.1 相关调整关闭。
2. **Open Design #2986 · BYOK private IP / internal proxy**：私网 LLM endpoint 被阻断，影响企业内网与本地部署；40 条评论、p1，截至核验日仍 open。
3. **OpenWork #1103 · infinite session summary loop**：普通问候也触发摘要循环，导致会话无法正常推进，暴露可靠性与恢复问题；22 条评论，已关闭。

- 进入/委托/过程/接管/产物/退出不适用于 issue 作为产品任务流；本项按“候选筛选→真实 issue 页面→状态/日期/评论核验→三条定稿”验收。
- 一句差异点：开源路线的真实摩擦集中在登录/本地性、企业代理兼容与长任务恢复；这些争议比功能清单更能暴露能力层边界。

## §4 新硬件

**本轮未发现自有硬件发布。** 截至 2026-09-09，在 OpenWork 与 Open Design 的官方仓库、Release 与官网中未发现自有硬件发布；它们依赖用户现有的 Mac/Windows/Linux 电脑、桌面壳、CLI、agent 与 MCP 来承载能力。这里是本轮公开来源的“未发现”，不能写成永远不做硬件的承诺。

对趋势页的可用关系是：开源阵营把差异化集中在能力层与可移植文件；Apple 把系统级体验押在自有载体；Google 同时经营能力和设备入口。该比较只描述当前公开产品结构，不做优劣结论。

## §5 拆分逻辑

1. **工具装载**：skills、plugins、design systems、MCP 都是可组合装载项；产品不必为每个能力新开一个模式。
2. **产物形态**：核心交付是 HTML、文档、演示、视频等真实文件，桌面 UI 负责选择、预览和恢复，CLI 负责可编排写入。
3. **爆炸半径**：边界落在 project/workspace、选中的目录、agent 自己的配置与 daemon 的 loopback 地址；跨 agent 并不自动继承对方权限。
4. **反馈回路**：OpenWork 用 Wrote/Read/Resume 显示任务轨迹；Open Design 用 stdout、artifact manifest、文件列表和预览把结果闭环。两者都还会受底层 agent 认证和运行环境影响。
5. **买单人**：面向愿意自带 agent、模型或本地环境的个人与团队；他们为可移植性、自托管/本地性和避免单一厂商锁定买单，同时承担配置与故障排查成本。

## §6 三个必答问题

1. **它把能力拆成了几块，边界画在哪？** 两层：OpenWork 把办公任务收在桌面会话与本地 workspace；Open Design 把设计拆成 desktop shell、loopback daemon/CLI、skills/plugins/design systems、外部 agent。文件边界是所选 project/workspace；权限边界由本地 daemon 与被接入 agent 共同决定；产物边界是项目内可导出的真实文件。跨层失败不会自动转成另一层的成功。
2. **它的委托面在往哪走——更显式还是更隐式？** 委托仍然显式：输入任务、选择 skill/design system/agent、看到 Wrote/Read 或 CLI stdout。隐式化发生在工具装载与上下文注入——选中后 token/skill 被带入 agent，不要求用户逐条写 prompt。过程可见，但底层 agent 的认证/余额仍可能在执行前打断。
3. **它的硬件在补软件的哪块短板？没硬件的怎么绕过去？** 本轮未发现自有硬件。替代路径是进入用户已有电脑与 agent：桌面 app 提供可见入口和预览，CLI/MCP 接入 Codex、Claude Code、Cursor 等执行器，本地 project files 保留可交接产物。短板是体验质量受宿主系统、agent 配置和账号状态共同制约。

## §7 素材与出处表

以下逐文件表与 [SOURCES.md](SOURCES.md) 同步；同源重复参考不增加独立流程帧数。

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

### 版本与事实来源

| 事实 | 来源 | 核验结果 |
|---|---|---|
| OpenWork 仓库与最新稳定版 | https://api.github.com/repos/different-ai/openwork · https://api.github.com/repos/different-ai/openwork/releases/latest | 23,437 stars；v0.18.44；published 2026-09-09T05:32:36Z |
| Open Design 仓库与最新稳定版 | https://api.github.com/repos/nexu-io/open-design · https://api.github.com/repos/nexu-io/open-design/releases/latest | 95,141 stars；0.22.1；published 2026-09-09T12:30:14Z；Apache-2.0 |
| v0.8.0 “Everything is a plugin” | https://open-design.ai/zh/blog/open-design-0-8-0-everything-is-a-plugin/ | 2026-05-22 历史发布点；不是当前版本 |
| 当前 design-system 数量 | https://github.com/nexu-io/open-design | 当前 README 与本机 v0.19.0 API 均为 151；任务书 149 为历史口径 |
| Open Design v0.12.0 品牌系统 | https://github.com/nexu-io/open-design/blob/main/apps/landing-page/app/content/blog/open-design-0-12-0-brand-backed-design-system.md | 2026-06-26；说明品牌提取与可复用 design system 流程 |

逐目录的状态说明见各 `assets/*/source.md`；真实失败与替代路径见 `SEARCH-LOG.md`。

## 待人填：观点 / 对我们的启发
