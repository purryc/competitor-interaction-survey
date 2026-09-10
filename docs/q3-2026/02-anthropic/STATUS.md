# Anthropic 执行状态

状态：COMPLETE_WITH_GAPS（本轮采集处置已完成；六项特性均有有效 UI，但仍是 PARTIAL，不能声称素材全部达标）

- 独立 goal：`01a0874a-af14-72e1-89bc-78829483e63b`
- 独立 goal 合同：`../_control/02-anthropic-goal.md`
- 最后更新：2026-09-09
- 六项特性：`COMPLETE 0 / PARTIAL 6 / MISSING 0`
- 正式媒体：60 个（53 张 PNG + 7 个 MP4）；另有 8 个逐目录 `source.md`
- 补充：Claude Tag 6 帧 + 1 个 clip，用于产品矩阵与 Slack 载体，不计六项特性完成度
- 新硬件：完成本轮公开资料处置；未找到自有硬件发布；MHS（2026-08-27）为共享设备控制规范 research preview，不是 Anthropic 自有设备；未找到“为什么不做硬件”的官方说明

## 已完成

- 已核实 Claude Design（2026-04-17，research preview）、Claude Tag（2026-06-23，Slack beta）、Cowork Desktop GA（2026-04-09）、Cowork Web/Mobile（2026-07-07）及当前 surface 限制。
- 已取得并实际审阅 Design、Dispatch、Tag、Cowork webinar、Cowork permissions、Claude Code Skills 五条视频；Claude Code 官方高级模式 PDF 20 页已全文提取并逐页渲染审阅；MHS 官方页原图已审阅。
- 已为六项特性按进入→委托→过程→接管→产物→退出逐项标记“看见/未看见”。
- 所有正式图片宽度 ≥1280px；7 个 clip 均 ≤30 秒、H.264/AAC，并已 `ffprobe` 与全量解码。
- README 已按固定七段组织，观点标题保持空白；逐文件来源 60/60 对齐，coverage.json 可被 `jq` 解析且所有登记路径存在。

## 仍有缺口

1. Cowork 文件夹授权：缺永久删除动作发生时的专门审批弹窗、持续权限撤销路径；当前第三方范围警告不能替代动作审批。同片 `03:45–04:44` 已复核，操作是清空文件内容并保留文件，执行时没有再次审批。
2. Cowork 跨设备：官方 Dispatch 实际是手机→桌面→手机，缺任务书指定的桌面→手机→桌面顺序与各阶段 2 帧。
3. Cowork 过程可见性：清晰官方 UI 来源是 2026-02-09 背景；缺本季完整文件变更、产物、退出。
4. Design 三种收敛：Comment、直接文字编辑有连续帧；滑杆只有静态控件，缺拖动前/中/后与画面响应。
5. Design→Code：缺 Claude Code 接收、运行、结果界面。
6. Claude Code Skills/Subagents/Agent Teams：来源混合第三方实录与官方讲义；缺同一任务里的 live 管理、接管、产物、结束。

## 补采条件

- Cowork：可登录的受控测试账号、空白临时文件夹、桌面与移动端同一 session；需允许录制，但不触碰真实用户文件。
- Design→Code / 滑杆：可访问的 Design 测试项目与 Claude Code 接收端；用无敏感内容的临时项目录制。
- Claude Code Agent Teams：Claude Code v2.1.32+ 且可启用 experimental Agent Teams 的安全测试 repo，或 Anthropic 官方长版 live demo。
- 当前本机 Claude Desktop 被 Cloudflare Turnstile 挡住，未点击或代做验证码；这是本轮自测未能补齐的单点条件。

## 交付入口

- `README.md`：固定七段与直接可读的关键帧序列
- `SOURCES.md`：60 个正式媒体逐文件出处
- `coverage.json`：逐特性验收、阶段可见性、缺口与下一步
- `SEARCH-LOG.md`：检索、候选审阅、失败与媒体 QA
- `assets/*/source.md`：逐目录素材状态、时间码与证据边界
