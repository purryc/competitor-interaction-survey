# Meta 检索日志

范围：仅 Meta。抓取日：2026-09-09（America/Toronto）。本日志记录真实尝试；搜索摘要不算已审阅画面。

| 日期 | 检索词 / 路径 | 站点 / 工具 | 结果与处置 |
|---|---|---|---|
| 2026-09-09 | `site:about.fb.com Meta Ray-Ban Display Neural Band handwriting teleprompter CES 2026` | Web / Meta Newsroom | 找到 2026-01-06 CES、2026-03-31 手写更新与 2026-05 无障碍研究官方页；逐页保存 HTML、提取媒体、核日期。 |
| 2026-09-09 | Meta CES 页 HTML 媒体 URL 与 regional `srcset` | Meta 巴西 / 拉美站 | 取得 1920×1080 手写视频、提词器和三类脱离眼镜静态图。各区域 `srcset` 的 CES 静态原图仍只有约 750px，没有找到官方更高分辨率替代。 |
| 2026-09-09 | Meta 2026-03 页 HTML 媒体 URL | Meta Newsroom | 取得 5.833 秒、1080×1920 Neural Handwriting display recording；完整下载、逐帧目检。源宽只有 1080px，保留规格缺口。 |
| 2026-09-09 | Meta 2025-09 发布页媒体 | Meta Newsroom | 取得 34.125 秒、3840×2160 官方合集；截取 12 秒 HUD 段。区域框具体功能无正文对应，使用中性命名；地图无路线线条。 |
| 2026-09-09 | `Meta Neural Band EMG wearable technology` | Meta 官方 EMG 页 | 下载页面 8 个嵌入视频并逐个 ffprobe/全解码。正式使用 pinch+EMG 片及一个旧 Orion/EMG wrist-roll 概念片，其余为重复/旧概念候选。页面无可核发布日期，标 `DATE_UNKNOWN`。 |
| 2026-09-09 | `What hand gestures can I use in a Web App with the Neural Band?` | Meta Developer FAQ | 正文核定 left/right/up/down swipe、index pinch enter、middle pinch cancel、无 custom gesture。没有找到误触阈值/误触率或走路边界。 |
| 2026-09-09 | `Meta Neural Band false activation walking accidental gesture` | Meta / Web search | 只找到一般产品表述和步行 HUD 宣传画面；没有受控实验或厂商数值。保留 `MISSING`，步行画面不作防误触证明。 |
| 2026-09-09 | `Meta Ray-Ban Display handwriting correction delete` | Meta Newsroom / Help / 官方视频候选 | CES 片、2026-03 更新片、帮助/新闻文本和 2026-06 官方频道候选均未发现可审计纠错/删除流程。保留 `MISSING`。 |
| 2026-09-09 | `Meta Ray-Ban Update Neural Handwriting Teleprompter Hands-On` | YouTube / VoodooDE VR English | 找到 2026-02-04 第三方实机。实际打开并在 01:47、03:39、03:44、03:49 目检；保存设置页与三个透镜取景状态。来源含 paid/affiliate 披露。 |
| 2026-09-09 | 下载第三方 YouTube 原视频 | `yt-dlp` / YouTube | 直接媒体请求返回 HTTP 403，未取得可本地逐帧审计的连续片。改用受控浏览器实际播放取证；最大截图只有 1250×700。尝试更大浏览窗口也受当前播放器/屏幕有效区域限制，没有以补边或放大冒充 1280px。 |
| 2026-09-09 | 提词器 `speed control`, `scroll speed`, `Neural Band` | 官方 CES 文本 + 第三方设置页 | 只核到 vertical scroll / horizontal swipe 模式、Text Size、Band 导航与“按自己的节奏”；没有独立速度控制器或速度数值。 |
| 2026-09-09 | `Garmin Meta Neural Band Unified Cabin` | Garmin Newsroom | 核到 2026-01-06 OEM proof-of-concept。Garmin 新闻图宽 512px，比 Meta CES 图更低，未替换正式图。 |
| 2026-09-09 | `University of Utah Meta Neural Band TetraSki smart home` | University of Utah | 取得 1488×1356 TetraSki 与 1000×656 智能家居合作图；TetraSki 静态图不显示腕带控制动作。 |
| 2026-09-09 | 2026-05 CMU / disability / two Neural Bands | Meta Newsroom | 下载 104.833 秒、1920×1080 官方研究片（129,033,809 bytes），全解码通过；目检核到双带、校准、输出标签、EMG 与游戏，截取 29 秒连续正式片。只标研究演示。 |
| 2026-09-09 | `Meta Ray-Ban Display available current United States retailers` | Meta 当前可用性页 | 当前页面明确 Display+Band 在美国通过选定授权零售商与 Meta flagship stores 可得。以它作为抓取日状态；CES 2026 的国际扩张暂停只作历史状态。 |
| 2026-09-09 / 10 | `Meta Ray-Ban Display Just Changed AI Glasses Forever… (New Features)`；https://www.youtube.com/watch?v=PetsyCQd7Ts | YouTube，`@raybanmeta` | 2026-09-09 连续看到 00:01:38；2026-09-10 按公开视频章节继续审 02:22 Spotify、02:55 Calendar、03:10 AI Reminders、03:20 Widgets、03:28 Games、03:51 Recap，并在 02:53、03:08、03:12、03:24、03:31、03:47、04:03 取屏核画面。YouTube 页面显示频道 verified badge、handle `@raybanmeta`，因此标品牌官方频道，不只按频道名判断。剩余章节内容是 Instagram Reels、display recording、Spotify、Calendar、提醒、widgets、games，没有出现本包缺失的手写纠错/删除、误触试验或提词器连续控制；不重复收录。 |

## 明确缺口

- Neural Handwriting：纠错、删除、完整入口、退出和未剪辑光学时延。
- 手势集：四向 swipe 的逐动作实际画面、每个手势对应的消费 HUD 结果、误触率/阈值、走路手势验证。
- HUD：透镜光学实拍、真实消失时机、区域框的官方功能名。
- Teleprompter：可下载连续实机、独立速度控制证据、三个状态的相邻性、退出画面、≥1280px 第三方源。
- 腕带脱离眼镜：已有研究/PoC 证据；没有消费可用性、通用配对或退出流程。
