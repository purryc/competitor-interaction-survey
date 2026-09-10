# Microsoft｜2026 Q3 交互素材包

采集处置完成于 2026-09-09。三项特性均达到数量要求，但证据闭环仍有缺口：Windows runtime 与 Copilot agent mode 为 `PARTIAL`，系统级权限模型为 `PARTIAL`；主要缺口是本机 agent 调度/运行数/kill、消费者统一权限总览、当前版接管点击与退出。素材状态以“画面实际可见”为准。

## §1 一句话结论

Microsoft 正把 Windows 做成 agent 的受控运行底座：2026 Build 的重点已落到 agent identity、MXC 隔离与声明式权限，但面向普通用户的统一调度、运行数和终止控制仍未在公开实机 UI 中形成可验证闭环。

## §2 产品矩阵

| 产品 / 模式 | 能碰到什么 | 权限边界 | 产物落点 | 本包定位 |
|---|---|---|---|---|---|
| Copilot chat | 用户提供的上下文与当前会话 | 对话范围，默认不代表可操作外部应用 | 会话文本 | 对照基线，不单独采集 |
| Edge `Browse with Copilot` | 当前浏览器标签及受控网页 | 浏览器 agent 模式；最终发帖前再次确认 | 目标网站中的草稿 | 当前 2026 agent 模式主序列 |
| Microsoft 365 Copilot / Agent365 | M365 数据、已部署 agent 与 host products | 管理员按用户、host product、agent 实例治理 | M365 应用或 agent 结果 | 补充注册库存与 block，不能冒充 Windows 本机 runtime |
| GitHub Copilot CLI | 工作目录、命令、可配置网络 | Filesystem / Network sandbox | 本地代码与终端结果 | 权限粒度的当前实机 UI |
| Windows agent platform（Agent ID + MXC） | 声明允许的文件、网络、UI 能力与进程 | OS agent identity、session/process isolation、MXC policy | 允许路径与受控应用 | 本包系统级核心；Build 2026 early/public preview 证据 |

## §3 特性详解 ×N

### A. Windows 作为 agent runtime — `PARTIAL`

六状态核对：进入 `已观察`；委托 `未在同一 runtime 片段观察`；过程 `已观察`；接管 `未观察`；产物 `仅观察到运行结果/拒绝，不是完整用户产物`；退出 `未观察`。

交互流程证据分成三组，彼此不是同一任务：

1. Agent ID 实机：Teams 中进入 agent 会话 → Task Manager `Users` 视图同屏展示该用户会话下的进程。画面本身没有可读 agent identity 字段，因此只记为“用户会话/进程可观察”，不据此声称独立 agent 身份已经由 UI 证明。
2. MXC 实机：声明运行约束 → 未授权文件写入被拒绝 → 恶意文件/网络/UI 行为被 MXC Shield 拦截。
3. Agent365 管理补充：管理中心看到 agent 库存与部署入口 → Block agent 配置入口。这里的总数是注册/治理库存，不是本机“正在运行数”；Block 图中复选框未勾、Save 为灰，不证明动作已经执行，也不是本机 kill。

![Agent 会话入口](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/01-agent-entry-teams.png)
![Task Manager Users 视图中的会话进程](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/02-agent-session-processes.png)
![MXC 声明式运行合同](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/03-mxc-declarative-contract.png)
![未授权写入被拒绝](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/04-runtime-file-write-denied.png)
![恶意行为被 MXC Shield 拦截](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/05-malicious-agent-contained.png)
![Agent365 注册与部署库存](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/06-agent-registry-inventory.png)
![Agent365 Block 操作](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/07-block-agent-governance.png)

短片：[Agent ID `08:00–08:29.9`](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/clip-agent-identity.mp4) · [MXC 拒绝 `15:00–15:30`](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/clip-mxc-runtime-denial.mp4)

一句差异点：系统把 agent 从“某个应用里的功能”提升为带独立身份、进程/会话隔离和 OS 强制约束的执行主体；当前公开 UI 仍更偏开发者与管理员。

缺口：没有找到 2026 官方实机画面证明 Windows 终端用户能看到运行中 agent 数、调度队列或对失控 agent 执行 kill。

### B. 系统级权限模型 — `PARTIAL`

六状态核对：进入 `已观察（配置页/合同）`；委托 `已观察（执行命令上下文）`；过程 `已观察`；接管 `未观察`；产物 `观察到拒绝结果`；退出 `未观察`。

权限粒度可见证据：MXC 合同同时声明 workload、execution entrypoint、文件读写路径、网络 allow/block 与 UI/clipboard 能力；GitHub Copilot CLI 的 sandbox 直接分成 Filesystem 和 Network；Agent365 部署页按 Copilot/Microsoft 365/Outlook/Teams 等 host product 限定应用面。已知文件夹清单只来自 2025 背景图。

![文件、网络、UI 能力的声明式模型](../../../media/q3-2026/06-microsoft/assets/system-permissions/01-declarative-permission-model.png)
![readwritePaths 与 readonlyPaths](../../../media/q3-2026/06-microsoft/assets/system-permissions/02-filesystem-readonly-paths.png)
![文件写入拒绝态](../../../media/q3-2026/06-microsoft/assets/system-permissions/03-file-write-denied.png)
![Copilot CLI Filesystem policy](../../../media/q3-2026/06-microsoft/assets/system-permissions/04-copilot-cli-filesystem-policy.png)
![Copilot CLI Network policy](../../../media/q3-2026/06-microsoft/assets/system-permissions/05-copilot-cli-network-policy.png)
![Agent365 host product 范围](../../../media/q3-2026/06-microsoft/assets/system-permissions/06-app-host-scope.png)
![已知文件夹设置提示，BACKGROUND](../../../media/q3-2026/06-microsoft/assets/system-permissions/07-known-folders-background.png)

短片：[文件系统配置→拒绝 `15:00–15:30`](../../../media/q3-2026/06-microsoft/assets/system-permissions/clip-filesystem-denial.mp4)

一句差异点：Microsoft 的公开方向是把权限合同下沉到执行容器，并允许按路径、网络与 UI 能力拆开；消费者侧“应用×能力”的统一可视总览尚未被本包证据证明。

与 Cowork 的并排比较：本包只完成 Microsoft 侧证据；跨品牌比较留给总览阶段，避免在未读取对方同口径素材时先下结论。

### C. Copilot 的 agent 模式 — `PARTIAL`

六状态核对：进入 `已观察`；委托 `已观察`；过程 `已观察`；接管 `仅 2025 BACKGROUND 观察到 Take control 按钮`；产物 `已观察草稿与最终确认`；退出 `未观察`。

`01–05` 是同一条 2026 Edge 官方连续演示：选择 Browse with Copilot → 输入 LinkedIn 发帖任务 → Copilot 打开目标站并持续显示 working/browsing → 生成草稿 → 显示“Reasoning completed in 6 steps”，把发布动作留给用户确认。`06` 是另一条 2025 Copilot Actions 背景图，只证明 paused + Take control 控件存在，不能接在前五帧后面当作同一任务。

![进入 Browse with Copilot](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/01-enter-browse-with-copilot.png)
![委托任务](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/02-delegate-task.png)
![Copilot 正在 LinkedIn 工作](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/03-working-on-linkedin.png)
![草稿弹窗形成](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/04-progress-draft-modal.png)
![完成六步推理并等待最终确认](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/05-artifact-confirmation.png)
![Paused 与 Take control，BACKGROUND](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/06-take-control-background.png)

短片：[2026 Edge 连续 29.90 秒](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/clip-edge-agentic-30s.mp4)

一句差异点：委托仍需明确文字表达，但执行期间在目标网页保留全局进度提示，外部发布动作在最后一步回到用户确认；当前 2026 片段没有证明即时接管与退出。

## §4 新硬件

2026 年已确认两条硬件线：

- 新 Surface Pro 13 英寸与 Surface Laptop 13.8/15 英寸使用 Snapdragon X2 系列，属于 Copilot+ PC 路线。官方发布页把它们描述为兼顾本地 AI 与云端能力的常规生产力设备；本包未发现专门为 agent 增加的新手势或常驻控制面。
- Surface RTX Spark Dev Box 面向开发者和持续本地 AI 工作负载，官方页标注 `Pre-release product; not available for sale`；Build 资料称 later 2026、美国 Microsoft.com。它用 GPU/大显存补长时间、本地、多 agent/模型工作负载，不应与普通 Copilot+ PC 的 NPU 营销口径混为一谈。

![2026 Surface Pro / Laptop](../../../media/q3-2026/06-microsoft/assets/hardware/01-surface-pro-laptop-2026.png)
![2026 Surface Pro](../../../media/q3-2026/06-microsoft/assets/hardware/02-surface-pro-2026.png)
![2026 Surface Laptop](../../../media/q3-2026/06-microsoft/assets/hardware/03-surface-laptop-2026.png)
![Surface RTX Spark Dev Box](../../../media/q3-2026/06-microsoft/assets/hardware/04-surface-rtx-spark-dev-box.png)
![Surface RTX Spark 端口](../../../media/q3-2026/06-microsoft/assets/hardware/05-surface-rtx-spark-ports.png)

为什么要有：普通 Surface 用 NPU 承接低功耗、持续的本地 AI；RTX Spark Dev Box 用 GPU 与 128GB 统一内存承接更长、更重的本地 agent 开发和执行。前者改善移动载体，后者解决开发工作站级持续算力，不是同一层产品。

新交互形式：已确认的硬件级入口仍是 Copilot 键；另一份 Windows 上访问 Copilot 的官方支持页列出 `Win+C`、`Hey Copilot` 和可配置的 pen shortcut。Copilot 键更新页称其未来可在 Settings > Bluetooth & devices > Keyboard 中改为 Context Menu 或 Right Ctrl，但该页没有可核实发布日期，因此不能把 `later this year` 推定成 2026 承诺；本包也没有 2026 高分辨率真实设置 UI。未发现 2026 Surface 新增 agent 专用触控板手势。

## §5 拆分逻辑

| 归因 | 为什么要拆开看 |
|---|---|
| 工具装载 | Edge agent 装载浏览器上下文；GitHub Copilot CLI 装载开发工具与工作目录；Windows runtime 装载 OS identity/MXC；Agent365 负责组织级部署。入口与可调用工具不同，不能合并成一个 Copilot 功能清单。 |
| 产物形态 | Edge 的产物可落到目标网站草稿；CLI 落到本地代码/终端；M365 agent 落到业务应用；MXC 本身是执行与约束底座，并不定义单一内容产物。 |
| 爆炸半径 | chat 最小；浏览器/CLI 扩展到网页和文件；Windows runtime 可触及进程、网络、文件与 UI，所以必须用 identity、隔离与声明式策略控制。 |
| 反馈回路 | Edge 通过 browsing/working、步骤完成和最终确认回报；CLI 通过终端与 sandbox 设置反馈；MXC 通过拒绝/blocked 日志反馈；Agent365 通过 inventory、activity、block 提供治理反馈。 |
| 买单人 | Copilot 面向个人/知识工作者；GitHub Copilot 面向开发团队；Agent365 面向 IT/安全/合规；Surface RTX Spark 面向需要本地持续算力的开发者与组织。不同买单人决定了可见控制面的位置。 |

## §6 三个必答问题

1. **它把能力拆成了几块，边界画在哪？** 至少五块：chat、浏览器代理、M365 业务 agent、开发者 CLI agent、Windows agent runtime。边界按可触达对象划分：会话上下文 → 浏览器标签/网页 → 组织数据与 host products → 本地工作目录/网络 → OS 文件、网络、UI 与进程；产物分别落在会话、目标网站、M365 应用、本地代码或被 runtime 约束的目标位置。
2. **它的委托面在往哪走——更显式还是更隐式？** 当前公开证据仍处于“必须打字说清楚”到“选定模式后代执行”之间。Browse with Copilot 把模式选择和任务文字保留为显式动作，执行过程更隐式地跨标签工作，但高影响发布留到最终确认。近半年变化主要是把执行和系统约束做深，并非取消委托表达。
3. **它的硬件在补软件的哪块短板？没硬件的怎么绕过去？** Surface/Copilot+ PC 用 NPU 提供低功耗本地 AI 载体，RTX Spark Dev Box 用 GPU/大内存补持续、本地、重型 agent 工作负载；Copilot 键提供硬件召唤入口。软件仍可用任务栏、`Win+C`、语音和笔快捷键进入，因此专用键是捷径，不是能力前提。

## §7 素材与出处表

以下逐文件表与 [SOURCES.md](SOURCES.md) 同步；同源重复参考不增加独立流程帧数。

抓取日期：`2026-09-09`。全部交付素材来自 Microsoft 官方页面、Microsoft Learn 或 Microsoft 官方频道。逐素材的证据边界与原始分辨率见 [runtime](assets/windows-agent-runtime/source.md)、[permissions](assets/system-permissions/source.md)、[Copilot agent mode](assets/copilot-agent-mode/source.md)、[hardware](assets/hardware/source.md)。

| 文件名 | 对应特性 | 来源 URL | 时间码 / 页面状态 | 抓取日期 | 官方 |
| --- | --- | --- | --- | --- | --- |
| [assets/windows-agent-runtime/01-agent-entry-teams.png](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/01-agent-entry-teams.png) | Windows runtime | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 08:20 | 2026-09-09 | 是 |
| [assets/windows-agent-runtime/02-agent-session-processes.png](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/02-agent-session-processes.png) | Windows runtime | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 08:45；Users 视图，没有可读 agent identity 字段 | 2026-09-09 | 是 |
| [assets/windows-agent-runtime/03-mxc-declarative-contract.png](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/03-mxc-declarative-contract.png) | Windows runtime | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 14:00 | 2026-09-09 | 是 |
| [assets/windows-agent-runtime/04-runtime-file-write-denied.png](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/04-runtime-file-write-denied.png) | Windows runtime | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 15:20 | 2026-09-09 | 是 |
| [assets/windows-agent-runtime/05-malicious-agent-contained.png](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/05-malicious-agent-contained.png) | Windows runtime | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 16:35 | 2026-09-09 | 是 |
| [assets/windows-agent-runtime/06-agent-registry-inventory.png](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/06-agent-registry-inventory.png) | Windows runtime | https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-actions?view=o365-worldwide | Agent365 Deploy agent；页更新 2026-08-31 | 2026-09-09 | 是 |
| [assets/windows-agent-runtime/07-block-agent-governance.png](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/07-block-agent-governance.png) | Windows runtime | https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-actions?view=o365-worldwide | Agent365 Block agent 配置入口，未勾选/未执行；页更新 2026-08-31 | 2026-09-09 | 是 |
| [assets/windows-agent-runtime/clip-agent-identity.mp4](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/clip-agent-identity.mp4) | Windows runtime | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 08:00–08:29.9 | 2026-09-09 | 是 |
| [assets/windows-agent-runtime/clip-mxc-runtime-denial.mp4](../../../media/q3-2026/06-microsoft/assets/windows-agent-runtime/clip-mxc-runtime-denial.mp4) | Windows runtime | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 15:00–15:30 | 2026-09-09 | 是 |
| [assets/system-permissions/01-declarative-permission-model.png](../../../media/q3-2026/06-microsoft/assets/system-permissions/01-declarative-permission-model.png) | 系统权限 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 14:00 | 2026-09-09 | 是 |
| [assets/system-permissions/02-filesystem-readonly-paths.png](../../../media/q3-2026/06-microsoft/assets/system-permissions/02-filesystem-readonly-paths.png) | 系统权限 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 15:35 | 2026-09-09 | 是 |
| [assets/system-permissions/03-file-write-denied.png](../../../media/q3-2026/06-microsoft/assets/system-permissions/03-file-write-denied.png) | 系统权限 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 15:20 | 2026-09-09 | 是 |
| [assets/system-permissions/04-copilot-cli-filesystem-policy.png](../../../media/q3-2026/06-microsoft/assets/system-permissions/04-copilot-cli-filesystem-policy.png) | 系统权限 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 22:25；Filesystem，No paths yet | 2026-09-09 | 是 |
| [assets/system-permissions/05-copilot-cli-network-policy.png](../../../media/q3-2026/06-microsoft/assets/system-permissions/05-copilot-cli-network-policy.png) | 系统权限 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 23:30；Network，No hosts yet | 2026-09-09 | 是 |
| [assets/system-permissions/06-app-host-scope.png](../../../media/q3-2026/06-microsoft/assets/system-permissions/06-app-host-scope.png) | 系统权限 | https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-actions?view=o365-worldwide | Host products；页更新 2026-08-31 | 2026-09-09 | 是 |
| [assets/system-permissions/07-known-folders-background.png](../../../media/q3-2026/06-microsoft/assets/system-permissions/07-known-folders-background.png) | 系统权限 | https://blogs.windows.com/windowsexperience/2025/10/16/securing-ai-agents-on-windows/ | Known folders；BACKGROUND 2025-10-16 | 2026-09-09 | 是 |
| [assets/system-permissions/clip-filesystem-denial.mp4](../../../media/q3-2026/06-microsoft/assets/system-permissions/clip-filesystem-denial.mp4) | 系统权限 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 15:00–15:30 | 2026-09-09 | 是 |
| [assets/copilot-agent-mode/01-enter-browse-with-copilot.png](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/01-enter-browse-with-copilot.png) | Copilot agent mode | https://www.youtube.com/watch?v=mQv0EBvj2nI | 00:03 | 2026-09-09 | 是 |
| [assets/copilot-agent-mode/02-delegate-task.png](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/02-delegate-task.png) | Copilot agent mode | https://www.youtube.com/watch?v=mQv0EBvj2nI | 00:12 | 2026-09-09 | 是 |
| [assets/copilot-agent-mode/03-working-on-linkedin.png](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/03-working-on-linkedin.png) | Copilot agent mode | https://www.youtube.com/watch?v=mQv0EBvj2nI | 00:21 | 2026-09-09 | 是 |
| [assets/copilot-agent-mode/04-progress-draft-modal.png](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/04-progress-draft-modal.png) | Copilot agent mode | https://www.youtube.com/watch?v=mQv0EBvj2nI | 00:27 | 2026-09-09 | 是 |
| [assets/copilot-agent-mode/05-artifact-confirmation.png](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/05-artifact-confirmation.png) | Copilot agent mode | https://www.youtube.com/watch?v=mQv0EBvj2nI | 00:33 | 2026-09-09 | 是 |
| [assets/copilot-agent-mode/06-take-control-background.png](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/06-take-control-background.png) | Copilot agent mode | https://blogs.windows.com/windowsexperience/2025/10/16/securing-ai-agents-on-windows/ | Paused + Take control；BACKGROUND 2025-10-16 | 2026-09-09 | 是 |
| [assets/copilot-agent-mode/clip-edge-agentic-30s.mp4](../../../media/q3-2026/06-microsoft/assets/copilot-agent-mode/clip-edge-agentic-30s.mp4) | Copilot agent mode | https://www.youtube.com/watch?v=mQv0EBvj2nI | 00:06–00:35.9 | 2026-09-09 | 是 |
| [assets/hardware/01-surface-pro-laptop-2026.png](../../../media/q3-2026/06-microsoft/assets/hardware/01-surface-pro-laptop-2026.png) | 新硬件 | https://news.microsoft.com/source/asia/2026/06/16/微软推出新一代-surface-pro-与-surface-laptop，兼顾性能与灵活性/?lang=zh-hans | 2026-06-16 发布页主图 | 2026-09-09 | 是 |
| [assets/hardware/02-surface-pro-2026.png](../../../media/q3-2026/06-microsoft/assets/hardware/02-surface-pro-2026.png) | 新硬件 | https://news.microsoft.com/source/asia/2026/06/16/微软推出新一代-surface-pro-与-surface-laptop，兼顾性能与灵活性/?lang=zh-hans | Surface Pro 产品图 | 2026-09-09 | 是 |
| [assets/hardware/03-surface-laptop-2026.png](../../../media/q3-2026/06-microsoft/assets/hardware/03-surface-laptop-2026.png) | 新硬件 | https://news.microsoft.com/source/asia/2026/06/16/微软推出新一代-surface-pro-与-surface-laptop，兼顾性能与灵活性/?lang=zh-hans | Surface Laptop 产品图 | 2026-09-09 | 是 |
| [assets/hardware/04-surface-rtx-spark-dev-box.png](../../../media/q3-2026/06-microsoft/assets/hardware/04-surface-rtx-spark-dev-box.png) | 新硬件 | https://www.microsoft.com/en-us/surface/devices/surface-rtx-spark-dev-box | Pre-release 主图 | 2026-09-09 | 是 |
| [assets/hardware/05-surface-rtx-spark-ports.png](../../../media/q3-2026/06-microsoft/assets/hardware/05-surface-rtx-spark-ports.png) | 新硬件 | https://www.microsoft.com/en-us/surface/devices/surface-rtx-spark-dev-box | Ports | 2026-09-09 | 是 |

### 文字事实补充

- Build 2026 Windows 平台与 MXC：https://blogs.windows.com/windowsdeveloper/2026/06/02/build-2026-furthering-windows-as-the-trusted-platform-for-development/
- Windows agent security：https://blogs.windows.com/windowsdeveloper/2026/06/02/windows-platform-security-for-ai-agents/
- Edge for Business 2026 说明页：https://blogs.windows.com/msedgedev/2026/05/20/new-in-edge-for-business-ai-for-work-safe-from-day-one/
- Agent 实例数量与 block 语义：https://learn.microsoft.com/en-us/microsoft-365/admin/manage/manage-agent-instances?view=o365-worldwide
- Copilot 键更新（页面未提供可核实发布日期）：https://support.microsoft.com/en-US/accessibility/windows/copilot/understand-updates-to-the-copilot-key-on-windows-devices
- Windows 上访问 Microsoft 365 Copilot：https://support.microsoft.com/en-US/Microsoft-365-Copilot/access-microsoft-365-copilot-on-windows

### 明确排除

- `Microsoft 365 admin center` 的总 agent 数是注册/治理库存，不作为本机正在运行数。
- Agent365 的 `Block agent` 不作为 Windows 本机 kill 证据。
- 2025 Copilot Actions 的 `Take control` 图只标 `BACKGROUND`，不接到 2026 Edge 序列。
- `_work/brk262-highmp4.partial` 是中断的下载缓存，不是交付素材。

## 待人填：观点 / 对我们的启发
