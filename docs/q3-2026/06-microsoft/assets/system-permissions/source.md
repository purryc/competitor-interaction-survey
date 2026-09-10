# 系统级权限模型素材出处

抓取日期统一为 `2026-09-09`。

| 文件 | 权限粒度 | 来源 URL | 时间码 / 页面状态 | 官方 | 原始规格 | 证据边界 |
|---|---|---|---|---|---|---|
| `01-declarative-permission-model.png` | 文件 / 网络 / UI 能力 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `14:00` | 是，Microsoft Developer，2026-06-03 | 1920×1080 | 技术讲解页，非普通用户设置页 |
| `02-filesystem-readonly-paths.png` | 文件路径读写 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `15:35`，JSON 中 `readwritePaths` 与 `readonlyPaths` | 是 | 1920×1080 | 实际演示配置文件 |
| `03-file-write-denied.png` | 文件路径运行时拒绝 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `15:20`，`PermissionError` | 是 | 1920×1080 | 实机拒绝态 |
| `04-copilot-cli-filesystem-policy.png` | 文件系统 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `22:25`，GitHub Copilot CLI sandbox Filesystem 页 | 是 | 1920×1080 | Public Preview；可见 include working directory / clear policy on exit，但路径列表仍为 `No paths yet` |
| `05-copilot-cli-network-policy.png` | 网络能力 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `23:30`，GitHub Copilot CLI sandbox Network tab 已选中 | 是 | 1920×1080 | Public Preview；可见 outbound、local network 与 host allow list，当前列表为 `No hosts yet` |
| `06-app-host-scope.png` | 应用 / host product | https://learn.microsoft.com/en-us/microsoft-365/admin/manage/agent-actions?view=o365-worldwide | `Deploy agent` UI，Host products 为 Copilot、Microsoft 365、Outlook、Teams；更新 2026-08-31 | 是，Microsoft Learn | 2400×1379 | 企业部署范围，不是 OS 单次授权弹窗 |
| `07-known-folders-background.png` | 已知文件夹 | https://blogs.windows.com/windowsexperience/2025/10/16/securing-ai-agents-on-windows/ | 页面状态：Actions 设置提示，Documents/Downloads/Desktop/Videos/Pictures/Music；发布 2025-10-16 | 是，Windows Experience Blog | 1920×1307 | `BACKGROUND`：早于 2026-03-09，只补“文件夹粒度”视觉 |
| `clip-filesystem-denial.mp4` | 文件路径配置→拒绝 | https://www.youtube.com/watch?v=CU4Wngb3JnA | BRK262 `15:00–15:30` | 是 | 1920×1080，30.0 秒 | 仅这一段为连续流程 |

当前素材可确认三层：MXC 能按文件路径、网络与 UI/clipboard 等能力声明；Copilot CLI 有文件系统和网络沙箱面板；Agent365 可按 host product 部署。普通消费者 Windows 的统一“应用×能力”权限总览未在当前公开素材中观察到。

## V47 网页可读性派生

原 1920×1080 Microsoft Build 会场录像包含彩色舞台边框，在网页缩略图中容易被误判为花屏。V47 从同一官方录像和同一时间码裁出中央演示区；只改变网页展示构图，不改变来源、动作判断或证据边界。原始派生文件的 SHA-256 保存在 `qa/iteration-47-unified-survey/microsoft-media-repair.json`。
