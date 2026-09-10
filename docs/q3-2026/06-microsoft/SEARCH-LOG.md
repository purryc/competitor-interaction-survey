# Microsoft 检索与尝试日志

抓取日期：2026-09-09（America/Toronto）

| 时间 | 检索词/入口 | 站点 | 实际结果 | 后续 |
|---|---|---|---|---|
| 2026-09-09 | `Windows agent runtime Build 2026 agent platform registration permissions agents running kill` | Windows Blog / Microsoft Learn / Microsoft Build / YouTube | 定位 Build 2026 Windows 官方博客、MXC 安全博客、BRK262 官方技术 session；尚未下载完整审阅 | 下载 BRK262，按章节实看 |
| 2026-09-09 | `Microsoft Execution Containers MXC video`、`Build 2026 Windows agent platform security AI agents session video` | YouTube / Microsoft Build | 定位 Microsoft Developer 官方 `BRK262`，说明和章节含 identity、MXC 恶意 agent、continuous supervision | 主素材候选 |
| 2026-09-09 | `Copilot agent mode 2026 progress take control` | Microsoft Learn / Microsoft Blog / YouTube | 找到 M365 Copilot Agent activity 文档与 Microsoft Mechanics `AI in Windows 11`；后者 2026-02-18，只能列 BACKGROUND | 继续找 03-09 后真实接管 UI |
| 2026-09-09 | `Copilot Actions Windows demo 2026 official` | Windows Blog / TechCommunity / YouTube | 找到 2026-05-20 Edge for Business 官方说明与 2026-02-26 Microsoft Mechanics 页面；尚需实看媒体 | 审视频与页面媒体，不用文字代替 UI |
| 2026-09-09 | `Surface RTX Spark Dev Box`、`Copilot+ PC 2026 NPU Copilot key` | Windows Developer Blog / Windows Experience Blog | 官方 Build 文确认 Surface RTX Spark Dev Box；Windows Experience Blog 确认 RTX Spark 秋季设备、首批含 Surface | 核上市、区域、键/手势与真实硬件图 |

## 收口记录

| 目标 | 查询 / 站点 | 结果 | 处置 |
|---|---|---|---|
| Build 2026 agent runtime | Microsoft Build BRK262 / YouTube / Medius | 找到 Agent ID、MXC、supervision、GitHub Copilot CLI sandbox 的官方实机演示 | 远程分段抓取 1080p；逐 5 秒审阅；正式抽帧与 30 秒片段入库 |
| BRK262 完整下载 | YouTube yt-dlp 1080p | 403 | 改用 Build 页面解析出的 Medius `HIGHMP4`；3.2GB 全片下载中止，保留 `.partial`，以精确远程 seek 分段，不把缓存列为交付 |
| 本机运行数 / kill | Microsoft Learn Agent Registry、Manage agent instances、Agent365 governance | 找到注册库存数量、Block agent 与 Foundry start/stop 语义；没有 Windows 本机运行中 agent 数/kill UI | 作为治理补充并明确排除替代关系；特性保留 PARTIAL |
| 权限粒度 | BRK262 14:00–24:00、Windows agent security、GitHub Copilot CLI | 找到路径读写、网络 allow/block、UI/clipboard 能力与 sandbox 面板 | 2026 主证据入库；消费者统一权限总览缺失 |
| 文件夹权限 | Windows Experience Blog `Securing AI agents on Windows` | 找到 1920×1307 known folders 设置提示，但发布时间 2025-10-16 | 只标 `BACKGROUND` |
| Copilot 进度与产物 | Microsoft Edge 官方 `Edge for Business demo: Browse with Copilot` | 找到 45.975 秒 1920×1080 官方连续演示，覆盖模式、委托、working/browsing、草稿、最终确认 | 完整下载、全解码、逐 3 秒审阅；抽 5 帧 + 30 秒片段 |
| Copilot 接管 | 2026 Edge 演示、2025 Copilot Actions 官方图 | 2026 连续片段无 takeover；2025 图有 Paused + Take control | 2025 图只作 BACKGROUND，不与 2026 序列拼接；未声称点击过 |
| Surface 2026 | Microsoft Source Asia 2026-06-16 | 找到 Surface Pro/Laptop 官方发布与 2560/1710px 产品图 | 3 张入库 |
| Surface RTX Spark | Microsoft Surface 产品页、Build 2026 blog | 找到 2700px 主图、2880px 端口图；页面为 Pre-release/not for sale | 2 张入库；标预发布和 later 2026/US 边界 |
| Copilot 键 | Microsoft Support 两页：Copilot-key updates；Access Microsoft 365 Copilot on Windows | 前者支持 2024 起专用键与未来 remap（页面无可核实发布日期）；后者支持 Win+C、Hey Copilot、pen shortcut | 分开归因；不把 `later this year` 推定为 2026；无 2026 高分辨率真实设置 UI，未造图 |
