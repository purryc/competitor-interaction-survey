# Siri 的委托面变化｜来源与逐帧说明

状态：`PARTIAL`｜发布：2026-06-08；可用性核验至 2026-09-09  
来源：[Siri AI Newsroom](https://www.apple.com/newsroom/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/)  
主片：`https://www.apple.com/newsroom/videos/2026/hls/06/apple-siri-ai-personal-assistant/US/US/Apple-Siri-AI-personal-assistant-260608_16x9.m3u8`  
入口：`https://www.apple.com/newsroom/videos/2026/autoplay/06/apple-siri-ai-dynamic-island-gesture/large_2x.mp4`

| 文件 | 源/时码 | 尺寸 | 实际画面 | 边界 |
|---|---:|---:|---|---|
| `01-dynamic-island.png` | 00:00.3 | 1542×2160 | Dynamic Island | 系统入口；无任务 |
| `02-swipe-down-entry.png` | 00:01.3 | 1542×2160 | 下拉展开 Siri | 手势进入；无执行 |
| `03-screen-aware-result.png` | 01:20 | 1920×1080 | 当前 Instagram 地点回答 | 屏幕指代；问题约 01:13 |
| `04-jeff-query.png` | 01:30 | 1920×1080 | “Where’s Jeff’s new place?” | 语句 + 个人上下文 |
| `05-message-address.png` | 01:40 | 1920×1080 | 从消息找到地址 | 跨 App；工具步骤未展开 |
| `06-route-result.png` | 01:58 | 1920×1080 | 组合路线预览 | 有产物；GO 尚待点击，无确认/撤回 |
| `07-selection-context-menu.png` | 静态 | 1960×1307 | Mac “Ask Siri” 菜单 | 选择对象；不是手机同流程 |
| `08-visual-intelligence-ipad.png` | 静态 | 1960×1307 | iPad Visual Intelligence | 视觉指代；不是手机同流程 |
| `clip.mp4` | 01:30–02:00 | 1920×1080 | 找地址→路线预览 | 连续主链；源 variant 无音轨，VTT 在 `_work/media` |

六段状态：进入已看见；委托已看见；过程部分看见；接管未看见；产物已看见；退出未看见。  
下一步：iOS 27 beta 真机录制 Calendar/发送类动作，检查批准、取消、撤销、接管和退出。
