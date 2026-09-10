# Meta Neural Band 手势集

抓取日期：2026-09-09（America/Toronto）。主来源官方性：Meta 官方。官方 EMG 技术页未提供可核的发布日期，因此窗口归属记为 `DATE_UNKNOWN`；开发者 FAQ 为抓取日在线页面。

- 官方 EMG 技术页：https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/
- 官方 Wearables Developer FAQ：https://developers.meta.com/wearables/faq/
- 步行 HUD 背景片来源页（2025-09-17，`BACKGROUND`）：https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/

官方 FAQ 对 Web App 的可用映射写得最明确：left/right/up/down swipes；食指 pinch 为 enter；中指 pinch 为 cancel；不支持 custom gestures。官方 EMG 页另以通用产品语言列出 finger taps、thumb swipes、wrist rolls，可用于 click/select 或 scroll，并称机器学习把肌肉信号转成命令、触觉反馈确认手势、可在手离开摄像头视野时工作、信号在本地处理。

这两层不能混为一层：FAQ 是 Web App 的消费版映射；EMG 页视频是动作与传感概念展示。页面没有给出误触阈值、误触率或走路场景边界。

| 文件 | 时间码 | 来源 URL / 页面状态 | 实际画面与证据边界 |
|---|---:|---|---|
| `clip-emg-signals.mp4` | 00:00.000–00:09.727 | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/；官方嵌入视频 | 连续展示手部动作与 EMG 轨迹；没有消费 HUD 命令结果。 |
| `01-index-pinch-start.png` | 00:00.500 | 同上；官方嵌入视频 | 拇指与食指接近，动作尚未接触。 |
| `02-index-pinch-contact.png` | 00:01.500 | 同上；官方嵌入视频 | 拇指与食指接触并伴随 EMG 轨迹。映射由 FAQ 的 index pinch = enter 核定，单帧本身不显示 enter 结果。 |
| `03-middle-pinch-start.png` | 00:04.500 | 同上；官方嵌入视频 | 食指伸出，中指接近拇指，动作尚未接触。 |
| `04-middle-pinch-contact.png` | 00:05.500 | 同上；官方嵌入视频 | 中指与拇指接触并伴随 EMG 轨迹。映射由 FAQ 的 middle pinch = cancel 核定，单帧本身不显示 cancel 结果。 |
| `clip-wrist-roll-concept.mp4` | 00:00.000–00:08.488 | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/；官方嵌入视频 | 旧 Orion/EMG 概念段，展示腕部滚转；不能当作当前消费版 Display 的完整操作验证。 |
| `05-wrist-roll-start-concept.png` | 00:01.000 | 同上；官方概念视频 | 腕部滚转起始姿态。 |
| `06-wrist-roll-end-concept.png` | 00:03.000 | 同上；官方概念视频 | 腕部滚转结束姿态；页面只给通用 click/select/scroll 例子，未把该帧唯一映射到某一消费命令。 |
| `07-walking-hud-context.png` | 00:09.000 | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/；2025-09 官方合成演示，`BACKGROUND` | 行走中的地图 HUD 宣传画面；没有同时展示手势，更没有受控误触试验，不能作为“走路不误触”证据。 |

正式状态：`PARTIAL`。缺口为四向滑动各自的实际动作组、消费 HUD 命令结果、误触阈值/误触率和行走手势边界。
