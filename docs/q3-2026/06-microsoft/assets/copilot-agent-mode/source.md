# Copilot agent 模式素材出处

抓取日期统一为 `2026-09-09`。`01–05` 是同一条 2026 官方连续视频；`06` 是单独的 2025 背景来源，不能拼成同一次任务。

| 文件 | 对应状态 | 来源 URL | 时间码 / 页面状态 | 官方 | 原始规格 | 证据边界 |
|---|---|---|---|---|---|---|
| `01-enter-browse-with-copilot.png` | 进入 | https://www.youtube.com/watch?v=mQv0EBvj2nI | `00:03`，模式菜单显示 Browse with Copilot / Chat only | 是，Microsoft Edge，上传 2026-05-12 | 1920×1080 | 连续视频起点 |
| `02-delegate-task.png` | 委托 | https://www.youtube.com/watch?v=mQv0EBvj2nI | `00:12`，输入“Go to my LinkedIn...” | 是 | 1920×1080 | 连续视频 |
| `03-working-on-linkedin.png` | 过程 | https://www.youtube.com/watch?v=mQv0EBvj2nI | `00:21`，LinkedIn 页面出现“Copilot is browsing / Copilot is working” | 是 | 1920×1080 | 连续视频 |
| `04-progress-draft-modal.png` | 过程 / 产物形成 | https://www.youtube.com/watch?v=mQv0EBvj2nI | `00:27`，LinkedIn 草稿弹窗已打开 | 是 | 1920×1080 | 连续视频 |
| `05-artifact-confirmation.png` | 产物 / 最终确认 | https://www.youtube.com/watch?v=mQv0EBvj2nI | `00:33`，`Reasoning completed in 6 steps`，等待用户确认 Post | 是 | 1920×1080 | 只看到等待确认，未看到点击发布与退出 |
| `06-take-control-background.png` | 接管补充 | https://blogs.windows.com/windowsexperience/2025/10/16/securing-ai-agents-on-windows/ | 页面状态：任务 Paused、`Take control`、要求用户选择 app；发布 2025-10-16 | 是，Windows Experience Blog | 1920×1236 | `BACKGROUND`，不是前五帧的后续 |
| `clip-edge-agentic-30s.mp4` | 进入→委托→过程→产物 | https://www.youtube.com/watch?v=mQv0EBvj2nI | 原视频 `00:06–00:35.9`，连续 29.90 秒 | 是 | 1920×1080，29.90 秒 | 不包含接管与退出 |

退出状态未观察到；接管只在 2025 背景产品图中有明确按钮。静态 `Take control` 只证明控件和 paused 状态可见，不证明本次采集执行过点击。
