# Anthropic｜2026 Q3 交互素材包

本包只覆盖 Anthropic。六项指定特性当前均为 `PARTIAL`：每项已有有效 UI 图，但至少一项任务书状态、时间窗或连续流程仍缺；`MISSING` 为 0。新硬件问题已完成本轮公开资料处置，结论边界见 §4。

## §1 一句话结论

Claude 目前把通用对话、代码、文件工作、视觉产物和 Slack 协作分别放在 Claude、Claude Code、Cowork、Claude Design、Claude Tag，并用跨设备 session、Slack thread 与 Design→Code 交接连接这些工作面。

## §2 产品矩阵

| 产品 / 模式 | 当前可核实状态 | 能碰到什么 / 权限边界 | 产物落在哪 |
|---|---|---|---|
| Claude（Chat） | Web、Desktop、Mobile | 用户上传内容、项目与已授权 connectors；权限随产品与组织设置 | 对话、项目、下载文件 |
| Claude Code | CLI、IDE、Web；Skills / Subagents 可用，Agent Teams 为 experimental | 本地 repo、终端与用户/项目配置允许的工具；Agent Teams 默认关闭 | repo 变更、终端结果、PR/远端任务结果 |
| Claude Cowork | 2026-01-12 research preview；2026-04-09 Desktop GA；2026-07-07 扩至 Web/Mobile，当前帮助页标 beta | 用户选择的文件夹、connectors、skills/plugins；本地文件/浏览器/电脑使用依赖 Desktop；永久删除前要求显式 Allow | Cowork session 与可跨端打开/下载的文件 |
| Claude Design | 2026-04-17 Anthropic Labs research preview，Pro / Max / Team / Enterprise | Design 项目、选中对象、批注、参数与直接文字编辑 | Design 文件夹、zip、PDF、PPTX、Canva、HTML，或交接给 Claude Code |
| Claude Tag | 2026-06-23 Slack beta，Team / Enterprise | 管理员允许的 Slack channels、tools、data、codebases；可设预算和日志 | Slack thread 回复、链接与跨系统工作结果 |

## §3 特性详解 ×N

### 1. Cowork 的文件夹授权 — PARTIAL

- 进入：第三方实录显示 Cowork 在任务中请求本地文件夹访问；背景期官方视频显示 macOS 文件夹选择器。
- 委托：原任务存在于 Cowork 会话，但取帧段没有重新展示完整委托文本。
- 过程：选择文件夹后回到 Cowork；本段未展示完整文件读取过程。
- 接管：`Deny all / Allow` 与 `Cancel / Always allow / Allow` 已看见。弹窗没有写 `Allow once`。
- 产物：本组未展示授权后产物。
- 退出：背景期官方视频显示从选择器返回 Cowork；未见撤销持久权限。
- 一句差异点：权限以用户选定的 workspace folder 为边界，并把一次允许与持续允许分开呈现。
- 未达项：没有“实际永久删除动作发生时”的动作级审批弹窗；现有范围警告不能替代它。同一视频后段只把 `project_plan.txt` 内容清空，文件仍存在，且没有再次审批。

素材序列 A（2026-05-06 第三方实录）：

| 请求文件夹访问 `01:53` | 范围警告 `03:07` | `Always allow / Allow` `03:18` |
|---|---|---|
| ![文件夹访问请求](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/01-folder-access-request.png) | ![文件夹权限范围警告](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/03-folder-scope-warning.png) | ![Allow 与 Always allow](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/04-allow-and-always-allow.png) |

素材序列 B（2026-02-09 官方背景）：

| 进入选择器 `24:23` | 选择器打开 `24:25` | 目标目录选中 `24:27` | 返回 Cowork `24:29` |
|---|---|---|---|
| ![进入选择器](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/06-background-folder-picker-entry.png) | ![文件夹选择器](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/07-background-folder-picker.png) | ![目录选中](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/08-background-folder-selected.png) | ![返回 Cowork](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/09-background-folder-return.png) |

逐图来源与边界：[assets/cowork-folder-permission/source.md](assets/cowork-folder-permission/source.md)。

### 2. Cowork 跨设备接力 — PARTIAL

- 进入：手机端 Cowork Dispatch 空态已看见；没有桌面起任务的画面。
- 委托：手机发送“打开下载目录中的 landing page proposal 并做 PPT”。
- 过程：同屏出现手机状态与桌面 Cowork，桌面显示计划/分析。
- 接管：手机可继续追问与改要求。
- 产物：桌面端显示已生成的 PowerPoint，多页产物可见；手机收到结果摘要。
- 退出：没有关闭 session 或显式返回桌面领取文件的画面。
- 一句差异点：官方演示把手机作为远程委托/追问面，把本地文件处理留在保持在线的桌面端。
- 未达项：任务书指定的“桌面起→手机看进度→回桌面拿产物”准确顺序与三阶段各两帧未出现；现有官方演示为“手机起→桌面做→手机看/追问”。

官方素材序列（2026-03-17；实际是手机→桌面→手机）：

| 手机委托 `00:06` | 手机/桌面工作 `00:10` | 桌面计划 `00:12` |
|---|---|---|
| ![手机委托](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/02-mobile-delegation.png) | ![手机与桌面同时工作](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/03-mobile-desktop-working.png) | ![桌面计划](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/04-desktop-plan.png) |

| 桌面产物 `00:14` | 手机结果 `00:22` | 手机追问 `00:28` |
|---|---|---|
| ![桌面产物](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/05-desktop-artifact.png) | ![手机结果](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/07-mobile-result.png) | ![手机追问](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/08-mobile-followup.png) |

逐图来源与边界：[assets/cowork-cross-device/source.md](assets/cowork-cross-device/source.md)。

### 3. Cowork 的过程可见性 — PARTIAL

- 进入：取帧从任务执行中段开始，未覆盖入口。
- 委托：完整初始委托未出现在本段。
- 过程：计划、逐项 checklist、运行状态和右侧 Progress 均可见。
- 接管：用户中途打开输入区并补充要求。
- 产物：本段没有最终产物。
- 退出：未见停止、取消或完成后退出。
- 一句差异点：计划与执行状态留在同一工作台，用户无需离开任务即可插话改方向。
- 未达项：清晰 UI 来自 2026-02-09，只能作背景；本季同等清晰的文件变更列表、产物和退出画面未取得。

官方背景序列（2026-02-09）：

| 计划 `25:10` | 清单推进 `25:20` | 运行状态 `25:28` | 插话入口 `25:32` | 输入附加要求 `25:37` |
|---|---|---|---|---|
| ![Cowork 计划](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/01-background-plan.png) | ![清单推进](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/03-background-checklist.png) | ![运行状态](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/04-background-progress.png) | ![插话入口](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/05-background-steering-entry.png) | ![输入附加要求](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/06-background-steering-input.png) |

逐图来源与边界：[assets/cowork-process-visibility/source.md](assets/cowork-process-visibility/source.md)。

### 4. Design 的三种收敛方式 — PARTIAL

- 进入：完整 Design 工作台与顶部 Comment / Edit text / Knobs 入口已看见。
- 委托：内联 Comment 中输入替换海岸照片的要求；直接文字编辑通过顶部模式切换进入。
- 过程：Comment 指令从输入到提交；Knobs 面板和两个实际滑杆组可见。
- 接管：用户可在 Comment、Knobs 和直接文字编辑之间切换。
- 产物：海岸照片替换结果和文字对象选择状态已看见。
- 退出：未见明确退出 Design。
- 一句差异点：同一画布同时提供自然语言批注、参数控件和对象级文字编辑三种收敛入口。
- 未达项：滑杆只见静态控件，没有同一滑杆拖动前后数值和画面变化的连续三帧；Knobs 的数值字段不当作滑杆证据。

官方序列 A：内联批注（2026-04-17）。

| Comment 打开 `00:50` | 指令完成 `00:51` | 图片替换结果 `00:52` |
|---|---|---|
| ![Comment 打开](../../../media/q3-2026/02-anthropic/assets/design-convergence/02-comment-entry.png) | ![指令完成](../../../media/q3-2026/02-anthropic/assets/design-convergence/03-comment-instruction.png) | ![图片替换结果](../../../media/q3-2026/02-anthropic/assets/design-convergence/04-comment-result.png) |

官方序列 B：直接文字编辑。

| Edit text 入口 `00:56.0` | 模式激活 `00:57.0` | 文字对象选中 `00:57.5` |
|---|---|---|
| ![Edit text 入口](../../../media/q3-2026/02-anthropic/assets/design-convergence/08-text-edit-entry.png) | ![Edit text 激活](../../../media/q3-2026/02-anthropic/assets/design-convergence/09-text-edit-activated.png) | ![文字对象选中](../../../media/q3-2026/02-anthropic/assets/design-convergence/10-text-selection.png) |

滑杆缺口证据（仅静态可见，不能冒充调参序列）：

| 地球参数滑杆 `00:24` | 字体尺寸滑杆 `00:42` |
|---|---|
| ![地球参数滑杆](../../../media/q3-2026/02-anthropic/assets/design-convergence/11-globe-sliders-visible.png) | ![字体尺寸滑杆](../../../media/q3-2026/02-anthropic/assets/design-convergence/12-typography-sliders-visible.png) |

逐图来源与边界：[assets/design-convergence/source.md](assets/design-convergence/source.md)。

### 5. Design → Code 的交接 — PARTIAL

- 进入：Export 菜单中选择 `Handoff to Claude Code`。
- 委托：弹窗可选 `Send to local coding agent` 或 `Send to Claude Code Web`。
- 过程：系统生成可复制命令，并允许补充实现细节。
- 接管：用户可复制命令、切换接收渠道或关闭弹窗。
- 产物：命令明确要求获取 Design file、读取 README，并实现 `Interactive globe.html`。
- 退出：Claude Code 接收、执行、回传结果均未见。
- 一句差异点：交接界面传递可获取的 Design 文件与 README/目标文件指令，而非只导出静态图。
- 未达项：接收端长什么样、执行中的状态和实现结果没有公开画面。

官方序列（2026-04-17）：

| Export 菜单 `01:06` | Handoff 渠道 `01:09` | 可复制实现命令 `01:10` |
|---|---|---|
| ![Export 菜单](../../../media/q3-2026/02-anthropic/assets/design-code-handoff/01-export-menu.png) | ![Handoff 渠道](../../../media/q3-2026/02-anthropic/assets/design-code-handoff/02-handoff-dialog.png) | ![Design 交接命令](../../../media/q3-2026/02-anthropic/assets/design-code-handoff/03-generated-command.png) |

逐图来源与边界：[assets/design-code-handoff/source.md](assets/design-code-handoff/source.md)。

### 6. Claude Code 的 Skills / Subagents / Agent Teams — PARTIAL

- 进入：第三方实录显示 Claude Code 的 `/` 命令列表和 `/skills` 面板。
- 委托：`/skill-creator` 可直接进入输入区；Subagents 官方讲义说明 `agents/` 角色定义和 hands-off delegation。
- 过程：官方讲义终端截图显示 `4 agents launched`，多个 agent 同时处于 Running in the background。
- 接管：官方文档说明可切换 teammate、直接发消息与查看任务列表；本包没有连续接管截图。
- 产物：未见从三类抽象到最终代码产物的连续画面。
- 退出：未见结束 subagent/team 的界面。
- 一句差异点：Skills 在命令/库面板中被调用，Subagents 以角色定义承接隔离任务，Agent Teams 在终端中显示多个并行 session。
- 未达项：来源混合了第三方实录和官方讲义；Subagents 页是结构说明，不是 live UI；缺少同一任务里的管理、接管与结束链路。

Skills 实录序列（2026-03-24 第三方）：

| `/` 命令列表 `07:44` | `/skill-creator` `07:48` | `/skills` 库面板 `08:06` |
|---|---|---|
| ![Skills 命令列表](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/01-skills-command.png) | ![Skill Creator](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/02-skills-panel.png) | ![Skills 库面板](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/03-skill-invocation.png) |

官方讲义（2026-03-24；两张并非连续流程）：

| Subagents 结构说明 p.13 | Agent Teams 终端 p.14 |
|---|---|
| ![Subagents 结构说明](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/04-subagents-official-slide.png) | ![Claude Code Agent Teams 终端](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/05-agent-teams-official-terminal.png) |

逐图来源与边界：[assets/claude-code-multi-agent/source.md](assets/claude-code-multi-agent/source.md)。

补充产品矩阵素材：`assets/claude-tag-slack/` 保存 2026-06-23 官方 Slack thread 委托、多人协作和结果画面，不计入上述六项完成度。

## §4 新硬件

截至 2026-09-09，本轮没有找到 Anthropic 宣布自有消费终端或自有硬件产品。2026-08-27 官方发布的 Model Hardware Standard（MHS）是让 AI agent 通过统一状态/动作规范操作实验室与制造设备的 research preview；其示例连接液体工作站、机械臂、读板机、显微镜和量子设备，设备来自实验室/制造商，不是 Anthropic 自有硬件。

“为什么不做自有硬件”：未找到 Anthropic 公开说明，保持空缺，不从渠道布局反推动机。

可核实的替代载体：Web、Desktop、Mobile、Slack、CLI/IDE，以及 Amazon Bedrock、Google Cloud Vertex AI、Microsoft Azure 等云平台。MHS 又增加了“进入既有物理设备”的标准层，但不改变“没有自有硬件”的边界。

![MHS 统一编排现有实验设备](../../../media/q3-2026/02-anthropic/assets/hardware-strategy/01-mhs-orchestration-diagram.png)

## §5 拆分逻辑

以下只对公开界面与产品边界做对号，不扩写品牌动机。

| 归因 | 可核实的产品边界 |
|---|---|
| 工具装载 | Cowork 装载 connectors / skills / plugins 与本地电脑能力；Claude Code 装载 repo、terminal、Skills / Subagents / Teams；Tag 装载 Slack 管理员授权的 channels/tools/data/codebases。 |
| 产物形态 | Chat 以对话/文件为主；Code 落到 repo/终端；Cowork 产出办公文件；Design 产出视觉文件、HTML 或 handoff bundle；Tag 把状态和结果留在 Slack thread。 |
| 爆炸半径 | Cowork 用 folder scope 与动作审批；Code 由项目/用户权限和工具规则约束；Tag 由 workspace 管理员控制访问范围、预算和日志。 |
| 反馈回路 | Cowork 用计划、进度、跨端 steering；Design 用批注、参数和直接编辑；Code 用终端任务状态；Tag 用多人 thread。 |
| 买单人 | Design 发布页覆盖 Pro/Max/Team/Enterprise；Cowork 当前帮助页覆盖 Pro/Max/Team，并允许 Enterprise 管理员启用；Tag 面向 Team/Enterprise；Claude Code 同时面向个人开发者与组织。 |

## §6 三个必答问题

1. **它把能力拆成了几块，边界画在哪？** 五个公开工作面：Chat 处理通用对话与项目；Code 处理 repo/终端；Cowork 处理选定文件夹和办公工具；Design 处理视觉画布及导出/交接；Tag 处理被授权 Slack 工作区内的多人委托。边界主要由文件范围、工具权限和产物落点表达。
2. **它的委托面在往哪走——更显式还是更隐式？** 公开素材同时存在显式输入（Chat/Code/Cowork）、选中对象即编辑（Design），以及在既有 Slack thread 中 `@Claude` 的就地委托（Tag）。本轮没有证据显示 Claude 在未经用户/管理员设置的情况下主动执行任务。
3. **它的硬件在补软件的哪块短板？没硬件的怎么绕过去？** 未找到自有终端；通过 Desktop/Mobile/Slack/IDE/云平台进入既有载体。MHS 把同一路径扩到实验室与制造设备，但它是共享接口规范，不是自有设备。

## §7 素材与出处表

以下逐文件表与 [SOURCES.md](SOURCES.md) 同步；同源重复参考不增加独立流程帧数。

格式：文件路径 | 对应特性 | 来源 URL | 视频时间码 / 页码 | 抓取日期 | 官方/第三方/背景

| 文件路径 | 对应特性 | 来源 URL | 时间码 / 页码 | 抓取日期 | 属性 |
| --- | --- | --- | --- | --- | --- |
| [assets/cowork-folder-permission/01-folder-access-request.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/01-folder-access-request.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=WWpJeiXgZpo | 00:01:53 | 2026-09-09 | 第三方 |
| [assets/cowork-folder-permission/02-folder-access-options.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/02-folder-access-options.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=WWpJeiXgZpo | 00:01:57 | 2026-09-09 | 第三方 |
| [assets/cowork-folder-permission/03-folder-scope-warning.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/03-folder-scope-warning.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=WWpJeiXgZpo | 00:03:07 | 2026-09-09 | 第三方 |
| [assets/cowork-folder-permission/04-allow-and-always-allow.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/04-allow-and-always-allow.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=WWpJeiXgZpo | 00:03:18 | 2026-09-09 | 第三方 |
| [assets/cowork-folder-permission/05-folder-warning-late-state.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/05-folder-warning-late-state.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=WWpJeiXgZpo | 00:03:28 | 2026-09-09 | 第三方 |
| [assets/cowork-folder-permission/06-background-folder-picker-entry.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/06-background-folder-picker-entry.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:24:23 | 2026-09-09 | 官方/背景 |
| [assets/cowork-folder-permission/07-background-folder-picker.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/07-background-folder-picker.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:24:25 | 2026-09-09 | 官方/背景 |
| [assets/cowork-folder-permission/08-background-folder-selected.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/08-background-folder-selected.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:24:27 | 2026-09-09 | 官方/背景 |
| [assets/cowork-folder-permission/09-background-folder-return.png](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/09-background-folder-return.png) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:24:29 | 2026-09-09 | 官方/背景 |
| [assets/cowork-folder-permission/clip.mp4](../../../media/q3-2026/02-anthropic/assets/cowork-folder-permission/clip.mp4) | Cowork 文件夹授权 | https://www.youtube.com/watch?v=WWpJeiXgZpo | 00:03:04–00:03:33.5 | 2026-09-09 | 第三方 |
| [assets/cowork-cross-device/01-mobile-empty.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/01-mobile-empty.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:02 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/02-mobile-delegation.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/02-mobile-delegation.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:06 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/03-mobile-desktop-working.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/03-mobile-desktop-working.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:10 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/04-desktop-plan.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/04-desktop-plan.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:12 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/05-desktop-artifact.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/05-desktop-artifact.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:14 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/06-desktop-artifact-later.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/06-desktop-artifact-later.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:16 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/07-mobile-result.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/07-mobile-result.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:22 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/08-mobile-followup.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/08-mobile-followup.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:28 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/09-mobile-followup-result.png](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/09-mobile-followup-result.png) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:32 | 2026-09-09 | 官方 |
| [assets/cowork-cross-device/clip.mp4](../../../media/q3-2026/02-anthropic/assets/cowork-cross-device/clip.mp4) | Cowork 跨设备接力 | https://www.youtube.com/watch?v=fVIV-L49eBs | 00:00:04–00:00:33.5 | 2026-09-09 | 官方 |
| [assets/cowork-process-visibility/01-background-plan.png](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/01-background-plan.png) | Cowork 过程可见性 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:25:10 | 2026-09-09 | 官方/背景 |
| [assets/cowork-process-visibility/02-background-plan-expanded.png](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/02-background-plan-expanded.png) | Cowork 过程可见性 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:25:14 | 2026-09-09 | 官方/背景 |
| [assets/cowork-process-visibility/03-background-checklist.png](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/03-background-checklist.png) | Cowork 过程可见性 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:25:20 | 2026-09-09 | 官方/背景 |
| [assets/cowork-process-visibility/04-background-progress.png](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/04-background-progress.png) | Cowork 过程可见性 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:25:28 | 2026-09-09 | 官方/背景 |
| [assets/cowork-process-visibility/05-background-steering-entry.png](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/05-background-steering-entry.png) | Cowork 过程可见性 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:25:32 | 2026-09-09 | 官方/背景 |
| [assets/cowork-process-visibility/06-background-steering-input.png](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/06-background-steering-input.png) | Cowork 过程可见性 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:25:37 | 2026-09-09 | 官方/背景 |
| [assets/cowork-process-visibility/clip.mp4](../../../media/q3-2026/02-anthropic/assets/cowork-process-visibility/clip.mp4) | Cowork 过程可见性 | https://www.youtube.com/watch?v=zfWfczd6keE | 00:25:10–00:25:39.5 | 2026-09-09 | 官方/背景 |
| [assets/design-convergence/01-global-ui.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/01-global-ui.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:48 | 2026-09-09 | 官方 |
| [assets/design-convergence/02-comment-entry.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/02-comment-entry.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:50 | 2026-09-09 | 官方 |
| [assets/design-convergence/03-comment-instruction.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/03-comment-instruction.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:51 | 2026-09-09 | 官方 |
| [assets/design-convergence/04-comment-result.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/04-comment-result.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:52 | 2026-09-09 | 官方 |
| [assets/design-convergence/05-knobs-entry.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/05-knobs-entry.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:53 | 2026-09-09 | 官方 |
| [assets/design-convergence/06-knobs-panel.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/06-knobs-panel.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:54 | 2026-09-09 | 官方 |
| [assets/design-convergence/07-knobs-object-selected.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/07-knobs-object-selected.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:55 | 2026-09-09 | 官方 |
| [assets/design-convergence/08-text-edit-entry.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/08-text-edit-entry.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:56.0 | 2026-09-09 | 官方 |
| [assets/design-convergence/09-text-edit-activated.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/09-text-edit-activated.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:57.0 | 2026-09-09 | 官方 |
| [assets/design-convergence/10-text-selection.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/10-text-selection.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:57.5 | 2026-09-09 | 官方 |
| [assets/design-convergence/11-globe-sliders-visible.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/11-globe-sliders-visible.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:24 | 2026-09-09 | 官方 |
| [assets/design-convergence/12-typography-sliders-visible.png](../../../media/q3-2026/02-anthropic/assets/design-convergence/12-typography-sliders-visible.png) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:42 | 2026-09-09 | 官方 |
| [assets/design-convergence/clip.mp4](../../../media/q3-2026/02-anthropic/assets/design-convergence/clip.mp4) | Design 三种收敛方式 | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:00:48–00:00:58 | 2026-09-09 | 官方 |
| [assets/design-code-handoff/01-export-menu.png](../../../media/q3-2026/02-anthropic/assets/design-code-handoff/01-export-menu.png) | Design → Code | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:01:06 | 2026-09-09 | 官方 |
| [assets/design-code-handoff/02-handoff-dialog.png](../../../media/q3-2026/02-anthropic/assets/design-code-handoff/02-handoff-dialog.png) | Design → Code | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:01:09 | 2026-09-09 | 官方 |
| [assets/design-code-handoff/03-generated-command.png](../../../media/q3-2026/02-anthropic/assets/design-code-handoff/03-generated-command.png) | Design → Code | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:01:10 | 2026-09-09 | 官方 |
| [assets/design-code-handoff/clip.mp4](../../../media/q3-2026/02-anthropic/assets/design-code-handoff/clip.mp4) | Design → Code | https://www.youtube.com/watch?v=t_LBECIQQqs | 00:01:04–00:01:11.5 | 2026-09-09 | 官方 |
| [assets/claude-code-multi-agent/01-skills-command.png](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/01-skills-command.png) | Claude Code Skills/Subagents/Teams | https://www.youtube.com/watch?v=epZy_NajGnA | 00:07:44 | 2026-09-09 | 第三方 |
| [assets/claude-code-multi-agent/02-skills-panel.png](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/02-skills-panel.png) | Claude Code Skills/Subagents/Teams | https://www.youtube.com/watch?v=epZy_NajGnA | 00:07:48 | 2026-09-09 | 第三方 |
| [assets/claude-code-multi-agent/03-skill-invocation.png](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/03-skill-invocation.png) | Claude Code Skills/Subagents/Teams | https://www.youtube.com/watch?v=epZy_NajGnA | 00:08:06 | 2026-09-09 | 第三方 |
| [assets/claude-code-multi-agent/04-subagents-official-slide.png](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/04-subagents-official-slide.png) | Claude Code Skills/Subagents/Teams | https://resources.anthropic.com/hubfs/Claude%20Code%20Advanced%20Patterns_%20Subagents%2C%20MCP%2C%20and%20Scaling%20to%20Real%20Codebases.pdf | p.13 | 2026-09-09 | 官方讲义 |
| [assets/claude-code-multi-agent/05-agent-teams-official-terminal.png](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/05-agent-teams-official-terminal.png) | Claude Code Skills/Subagents/Teams | https://resources.anthropic.com/hubfs/Claude%20Code%20Advanced%20Patterns_%20Subagents%2C%20MCP%2C%20and%20Scaling%20to%20Real%20Codebases.pdf | p.14 | 2026-09-09 | 官方讲义/终端截图 |
| [assets/claude-code-multi-agent/clip.mp4](../../../media/q3-2026/02-anthropic/assets/claude-code-multi-agent/clip.mp4) | Claude Code Skills/Subagents/Teams | https://www.youtube.com/watch?v=epZy_NajGnA | 00:07:43–00:08:12.5 | 2026-09-09 | 第三方 |
| [assets/claude-tag-slack/01-slack-global-ui.png](../../../media/q3-2026/02-anthropic/assets/claude-tag-slack/01-slack-global-ui.png) | Claude Tag 补充 | https://www.youtube.com/watch?v=VojDzHaciKQ | 00:00:36 | 2026-09-09 | 官方 |
| [assets/claude-tag-slack/02-thread-delegation.png](../../../media/q3-2026/02-anthropic/assets/claude-tag-slack/02-thread-delegation.png) | Claude Tag 补充 | https://www.youtube.com/watch?v=VojDzHaciKQ | 00:00:44 | 2026-09-09 | 官方 |
| [assets/claude-tag-slack/03-claude-thread-response.png](../../../media/q3-2026/02-anthropic/assets/claude-tag-slack/03-claude-thread-response.png) | Claude Tag 补充 | https://www.youtube.com/watch?v=VojDzHaciKQ | 00:00:52 | 2026-09-09 | 官方 |
| [assets/claude-tag-slack/04-multiplayer-thread.png](../../../media/q3-2026/02-anthropic/assets/claude-tag-slack/04-multiplayer-thread.png) | Claude Tag 补充 | https://www.youtube.com/watch?v=VojDzHaciKQ | 00:01:04 | 2026-09-09 | 官方 |
| [assets/claude-tag-slack/05-artifact-link.png](../../../media/q3-2026/02-anthropic/assets/claude-tag-slack/05-artifact-link.png) | Claude Tag 补充 | https://www.youtube.com/watch?v=VojDzHaciKQ | 00:01:20 | 2026-09-09 | 官方 |
| [assets/claude-tag-slack/06-followup.png](../../../media/q3-2026/02-anthropic/assets/claude-tag-slack/06-followup.png) | Claude Tag 补充 | https://www.youtube.com/watch?v=VojDzHaciKQ | 00:01:32 | 2026-09-09 | 官方 |
| [assets/claude-tag-slack/clip.mp4](../../../media/q3-2026/02-anthropic/assets/claude-tag-slack/clip.mp4) | Claude Tag 补充 | https://www.youtube.com/watch?v=VojDzHaciKQ | 00:00:36–00:01:05.5 | 2026-09-09 | 官方 |
| [assets/hardware-strategy/01-mhs-orchestration-diagram.png](../../../media/q3-2026/02-anthropic/assets/hardware-strategy/01-mhs-orchestration-diagram.png) | 新硬件 / MHS | https://www.anthropic.com/news/model-hardware-standard-research-preview | 静态图 | 2026-09-09 | 官方 |
| [assets/hardware-strategy/02-lab-plate-photo.png](../../../media/q3-2026/02-anthropic/assets/hardware-strategy/02-lab-plate-photo.png) | 新硬件 / MHS | https://www.anthropic.com/news/model-hardware-standard-research-preview | 静态图；官方 JPG 转 PNG | 2026-09-09 | 官方 |
| [assets/hardware-strategy/03-mhs-lab-comparison.png](../../../media/q3-2026/02-anthropic/assets/hardware-strategy/03-mhs-lab-comparison.png) | 新硬件 / MHS | https://www.anthropic.com/news/model-hardware-standard-research-preview | 静态图 | 2026-09-09 | 官方 |

## 待人填：观点 / 对我们的启发
