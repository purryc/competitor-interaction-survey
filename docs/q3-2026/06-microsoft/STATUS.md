# Microsoft 执行状态

状态：COLLECTION_DISPOSITION_COMPLETE_WITH_GAPS

独立 goal 合同：`../_control/06-microsoft-goal.md`

## 已实时核实

- 2026-06-02 Microsoft Build 2026 官方 Windows Developer Blog 将 Windows 的 agent 基础明确命名为 Microsoft Execution Containers（MXC）SDK（early preview），并说明 OS-enforced agent identity、process/session isolation、Entra/Intune/Defender/Purview 管理边界。
- 2026-06-03 Microsoft Developer 官方 Build breakout `BRK262 · Building Agents You Can Trust on Windows` 已定位；章节明确包含 Agent Identity 演示（06:03）、MXC 与恶意 agent 演示（14:14）、manageability/continuous supervision（19:03）。这是 runtime 与权限两项的主要视频候选。
- Copilot 相关候选已定位：Microsoft Learn `View agent activity in Microsoft 365 Copilot`（2026-05-15 更新）展示 activity list、in progress/completed/failed/waiting for input；Microsoft Mechanics 官方视频 `AI in Windows 11`（2026-02-18，BACKGROUND）含 taskbar agents 段落。最终当前版接管缺口与替代路径已记于下文及 SEARCH-LOG。
- 新硬件候选已核实：Build 2026 官方 Windows Developer Blog 宣布 Surface RTX Spark Dev Box；2026-05-31 Windows Experience Blog 说明 RTX Spark PC 秋季开始、首批含 Microsoft Surface，并仍归入 Copilot+ PC 类别。已完成产品图与专用键文字核验，未取得的新交互设置 UI 保留缺口。

## 已入库

- Windows agent runtime：7 张正式图、2 段 30 秒短片。覆盖演示中的会话进程（无可读 agent identity 字段）、MXC 声明式合同、运行时拒绝、恶意行为 containment、Agent365 库存与 block 补充。
- 系统级权限：7 张正式图、1 段 30 秒短片。覆盖路径读写、网络、UI/clipboard 能力、Copilot CLI 文件系统/网络 sandbox、Agent365 host product；已知文件夹图明确标为 `BACKGROUND`。
- Copilot agent mode：6 张正式图、1 段 30 秒短片。2026 Edge 连续序列覆盖进入、委托、过程、草稿与最终确认；`Take control` 只用 2025 `BACKGROUND` 图补充。
- 新硬件：5 张高分辨率官方产品图，覆盖 2026 Surface Pro/Laptop 与预发布 Surface RTX Spark Dev Box。

## 明确缺口

1. 未找到 2026 官方实机 UI 证明 Windows 本机的 agent 调度队列、正在运行数和用户 kill。Agent365 库存/Block 仅作治理补充。
2. 未找到 2026 消费者统一“应用×能力”权限总览；文件夹粒度的高分辨率真实 UI 只来自 2025 背景图。
3. Copilot 当前 2026 连续序列没有接管点击和退出；`Take control` 静态图为 2025 背景，不能当作已点击。
4. Copilot 键的当前行为有官方支持文字，但未找到 2026 高分辨率真实 remap 设置 UI；未发现 agent 专用触控板手势。

## 最终 QA

- 正式素材：25 张 PNG、4 段 MP4；三项特性图片数 20，硬件图片数 5。每个 assets 子目录均有 `source.md`。
- 全部 PNG 实测宽度 ≥1280；硬件主图从官方 2560×1440 JPEG 原尺寸无缩放转为 PNG，原 JPEG 留在 `_work`。
- 4 段 MP4 均为 H.264 1920×1080，时长 29.905–29.997 秒；`ffmpeg` 全解码无报错，`ffplay` 各连续播放 3 秒成功。
- `coverage.json` 通过 `jq`；文件系统计数与 JSON 一致；README、SOURCES、各 source.md 对全部正式素材都有记录；本地链接全部存在。
- `review.html` 已在真实浏览器中打开并目检：图片加载、三项 PARTIAL 标签、BACKGROUND 与不可拼接边界均可见。

完成含义：所有指定方向都已执行检索、抓取、目检和证据归类；不是把三项特性误判为完整闭环。后续如出现 Windows 实机或更新的 2026 官方 demo，应优先补本机运行数/kill、消费者权限总览、接管点击和退出。
