# Windows agent runtime 素材出处

抓取日期统一为 `2026-09-09`。视频帧保留 Microsoft Build 会场、演示窗口和 Windows 桌面边界，没有裁切或放大伪造。

| 文件 | 对应状态 | 来源 URL | 时间码 / 页面状态 | 官方 | 原始规格 | 证据边界 |
|---|---|---|---|---|---|---|
| `01-agent-entry-teams.png` | 进入 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `08:20`，OpenClaw/Agent ID 演示进入 Teams agent 会话 | 是，Microsoft Developer，2026-06-03 | 1920×1080 | 展示 agent 会话入口，不证明注册 UI |
| `02-agent-session-processes.png` | 过程 / 监督 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `08:45`，Task Manager `Users` 视图与 Teams agent 会话同屏 | 是 | 1920×1080 | 演示者口述不同用户隔离；画面仅显示该用户会话下的进程清单，没有可读 agent identity 字段，也没有“当前运行 agent 总数” |
| `03-mxc-declarative-contract.png` | 限权配置 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `14:00`，MXC declarative approach | 是 | 1920×1080 | 讲解页含 workload、入口、文件、网络、UI 权限；不是最终用户设置页 |
| `04-runtime-file-write-denied.png` | 运行时拒绝 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `15:20`，写入未授权路径报 `PermissionError` | 是 | 1920×1080 | 实机拒绝态 |
| `05-malicious-agent-contained.png` | 运行时拦截 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `16:35`，MXC Shield 显示文件、网络、UI 等操作被 blocked | 是 | 1920×1080 | 实机攻击演示；不是普通用户日常控制面板 |
| `06-agent-registry-inventory.png` | 注册 / 库存补充 | https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-actions?view=o365-worldwide | 文档页 `Deploy agents` 官方 UI，页面更新 2026-08-31 | 是，Microsoft Learn | 2400×1379 | Agent365 管理库存，不等于本机 Windows 正在运行数 |
| `07-block-agent-governance.png` | 停用入口补充 | https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-actions?view=o365-worldwide | 文档页 `Block agent` 配置面板，复选框未勾且 Save 灰；页面更新 2026-08-31 | 是 | 2388×1407 | 只证明企业治理入口存在，不证明 block 已执行，更不等于杀掉本机失控进程 |
| `clip-agent-identity.mp4` | 进入 / 过程 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `08:00–08:29.9` | 是 | 1920×1080，29.93 秒 | 与 MXC 演示是不同片段 |
| `clip-mxc-runtime-denial.mp4` | 限权 / 拒绝 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `15:00–15:30` | 是 | 1920×1080，30.0 秒 | 与 Agent ID 演示是不同片段 |

未观察到的要求：公开 2026 UI 中的调度队列、本机正在运行 agent 数量、面向用户的一键 kill。Agent365 的库存数字和 Block 操作不得替代这些状态。

## V47 网页可读性派生

原 1920×1080 Microsoft Build 会场录像包含彩色舞台边框，在网页缩略图中容易被误判为花屏。V47 从同一官方录像和同一时间码裁出中央演示区；只改变网页展示构图，不改变来源、动作判断或证据边界。原始派生文件的 SHA-256 保存在 `qa/iteration-47-unified-survey/microsoft-media-repair.json`。
