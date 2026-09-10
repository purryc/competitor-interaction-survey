# Apple 检索与采集日志

日期：2026-09-09（America/Toronto）

## 发布会与硬件

- 打开 Apple Events 与 Developer 邀请页，核对 9 月 9 日、10:00 PT 和发布清单。
- 打开当日 Newsroom/产品页，确认 iPhone Duo、iPhone 18 Pro/Max、Watch Series 12、Watch Ultra 4、AirPods 5 的正式名称与日期。
- 活动回放仍未上线：John Ternus 的 CEO 身份有当日稿件，实际主持人没有视频证据，记 `UNVERIFIED`。
- 解析 Events 页面，下载五张 2x 发布卡片图；Pro 与 Pro Max 共用 Pro 家族卡片。

## iPhone Duo

- 查询 `Split View`、`keyboard`、`Apple Pencil`、`hover`、`multitasking`、`same aspect ratio`。
- 下载 1920×1080 官方产品片 181.581 秒及 VTT；以 10/4/2 秒接触表审阅，再精查 4–46、104–124、23–27 秒。
- 找到外屏、展开、内屏、Safari、Split View、交换分屏、双拇指游戏；Newsroom 另有展开内屏全宽 QWERTY 键盘 + Write with Siri 静态图；文字确认同纵横比和 Pencil 今年稍后。
- 缺口：没有具体同一任务外→内接续；23–27 秒只是 Safari 滚动；键盘只有静态布局、没有输入过程；没有 Pencil、hover 或退出实录。
- 输出 9 张 PNG 与 00:08–00:38 的 30 秒 H.264 无声片；源 variant 本身无音轨。

## Home Hub / Apple TV

- 定向查询 `site:apple.com/newsroom/2026/09 Apple Home Hub`、`7-inch Home Hub`、`site:apple.com/apple-events Home Hub`、`new Apple TV 4K September 2026`。
- 查 Events、Home App、Apple TV 产品/规格页、Newsroom TV & Home archive。
- 没有 7 英寸 Home Hub 或新 Apple TV 4K 的本场发布；当前 Apple TV 4K 仍列 A15 Bionic。
- Apple 官方既有 “home hub” 是 HomePod/HomePod mini/Apple TV 的系统角色。为避免误报，不用既有 Home App 图凑帧。

## Siri 委托面

- 下载 Personal Assistant 1080p HLS、VTT、Dynamic Island 动画；审阅 0–162 秒。
- 关键段：约 01:13 对当前 Instagram 内容追问；01:29 问 Jeff 地址；01:30–01:44 从消息找到；01:45 组合路线；01:58 出结果。
- 输出 01:30–02:00 主片、入口与主流程帧；补充 Mac 上下文菜单 “Ask Siri” 和 iPad Visual Intelligence 静态 UI。
- 缺口：没有批准、拒绝、暂停、撤销、人工接管和退出。

## 跨设备接力

- 核查 Siri AI Newsroom 与 iOS/iPadOS 27 的 `start ... on Mac and continue ...`、`iCloud sync`、`pick up where you left off`。
- 下载 iPhone、iPad、Watch、Vision Pro 四种设备官方 UI。
- 没有同一会话 A→B 的连续视频，也没有同步提示、延迟或冲突证据；无 clip，记 `PARTIAL`。
- 2026-09-09 定向检索 `"Siri AI" beta hands-on cross-device handoff same conversation iPhone Mac video`、`site:youtube.com "Siri AI" beta cross device conversation handoff`。实际打开 Android Authority 的 48 小时开发者 beta 上手：作者写明在 iPhone 17 Pro 开始旅行研究后，于 iPad Air 等待短暂同步看到同一会话。这是可信文字实测，但页面未提供可核验的 A→B 连续视频，故只加入来源，不伪造 clip。

## Siri 长任务控制补查

- 2026-09-09 定向检索 `"Siri AI" beta pause cancel approve long task hands-on video`、`Siri AI beta confirmation before action hands-on message send iOS 27`、`Siri AI agentic task progress cancel approval UI video iOS 27 beta`。
- 搜到的真实 beta 上手覆盖提问、跨 App 取数、相机与消息动作，但未发现同时展示长任务进度、暂停/取消、执行前批准和人工接管的可靠端到端视频。
- Apple Developer 的 `CancellableIntent` 与 WWDC26 App Intents 资料说明开发者可让意图被取消，长任务可通过 Live Activity 管理进度；这是框架能力，不是 Siri AI 面向用户的实际控制界面，未作为缺口替代素材。

## Watch / AirPods

- 下载 2026 Watch Siri 9.009 秒片、AirPods Live Translation 14.825 秒片、volume swipe 3 秒动画。
- AirPods 5 Newsroom 文字确认免手 Siri、点头/摇头、翻译触发和柄部滑动。
- 2026 片没有清楚头部动作；回查 2024 Siri Interactions，17 秒帧只作背景且画面仍有歧义。
- Watch 片是腕上语音/回答，没有 Series 12 独有捏合或新手势。

## 失败与未采用

- 猜测的 Watch 新闻稿 URL曾返回 404，随后从 Apple 实际链接纠正。
- OS Siri 抽象渐变球没有具体交互状态，不纳入主证据。
- AirPods 5 产品片是氛围混剪，头部动作不清，主证据改用翻译与音量滑动。
- 既有 Home App/HomePod/Apple TV 图不能证明 7 英寸新品，未采用。

## 媒体方法

- `ffmpeg` 取帧与 H.264/yuv420p/faststart 重编码；AirPods clip 保留 AAC。
- 官方 JPG 转 PNG，不改变画面含义；正式 PNG 目标宽度 ≥1280。
- `ffprobe` 检查 codec/时长/分辨率，`ffmpeg -v error -f null -` 全量解码，代表帧直接目检。
