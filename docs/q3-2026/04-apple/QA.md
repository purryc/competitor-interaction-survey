# Apple 2026 Q3 素材包｜最终 QA

执行时间：2026-09-09 17:15 EDT（America/Toronto）  
结论：`PASS_WITH_DOCUMENTED_GAPS`。文件与媒体验收通过；产品证据缺口仍按 `COMPLETE 0 / PARTIAL 4 / MISSING 1` 保留。

## 结构与可追溯性

- `coverage.json`：`jq empty` 通过。
- `README.md`：§1–§7 共 7 个必需二级标题；最后一行是空的 `## 待人填：观点 / 对我们的启发`。
- `README.md` 与 `SOURCES.md`：各 36 行逐素材账本，覆盖 33 张 PNG 与 3 个 MP4。
- `review.html`：HTML 解析通过；33 个 `<img>` 的本地文件全部存在，并按同源/特性分组。
- 正式 Markdown 与 HTML 本地链接：全部存在。外部来源的关键事实页在收口时重新打开；这不等于对所有 CDN URL 做长期可用性保证。

## 图片

- 数量：33 张 PNG。
- 门槛：宽度 ≥1280px。
- 实测：最小 1306px，最大 3840px；全部通过。
- 逐图尺寸、源时间码、URL 和证据边界见各 `assets/*/source.md`，总账见 `README.md` §7.1 与 `SOURCES.md`。

## 视频

| 文件 | 编码 | 像素格式 | 时长 | 音频 | 全量解码 |
|---|---|---|---:|---|---|
| `assets/foldable-input/clip.mp4` | H.264 | yuv420p | 29.996633s | 无 | PASS |
| `assets/siri-delegation/clip.mp4` | H.264 | yuv420p | 29.996633s | 无 | PASS |
| `assets/watch-airpods-input/clip.mp4` | H.264 | yuv420p | 14.825000s | AAC | PASS |

三段均满足 ≤30 秒；`ffmpeg -v error -i … -f null -` 无解码错误。

## 代表帧目检

- Duo：外屏、展开、内屏、网页、Split View、窗口对换与双拇指场景可辨；键盘图是独立官方静态图，未当作连续输入过程。
- Siri：Dynamic Island 入口、当前屏幕问答、Messages 地址检索与 Maps 路线预览可辨；路线的 `GO` 未点击，未写成已执行导航。
- 跨设备：iPhone、iPad、Watch、Vision Pro 均为分立官方 UI；第三方 beta 文字实测支持 iPhone→iPad 会话出现，但没有 A→B 连续视频。
- Watch/AirPods：Watch 查询与回答可辨；AirPods 00:03 只见佩戴/触碰，整段无翻译文字/音频 UI。双柄触发来自官方文字，交流继续只是场景结果。
- Home Hub：截至核验未见本场官方新品发布，故有意不放既有 Home App 图片；状态保持 MISSING。
- 硬件：5 张 Newsroom 官方产品图覆盖 6 个已发布型号（Pro/Pro Max 共用一图）。

## 未被 QA “洗白”的缺口

- 0 项 COMPLETE：素材门槛不仅看数量，还要求关键流程与接管/退出证据。
- Siri 长任务暂停/取消/批准：定向 beta 上手检索未命中可靠端到端演示；开发框架的可取消意图与 Live Activity 不能替代用户界面证据。
- 活动主持人：回放仍未可用，继续 `UNVERIFIED`。
- 新 Apple TV 4K：只能说截至核验未见本场官方发布，不能推断永久取消。
