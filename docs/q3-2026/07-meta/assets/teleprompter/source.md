# Teleprompter

抓取日期：2026-09-09（America/Toronto）。官方功能页发布日期：2026-01-06，早于 2026-03-09，记为 `BACKGROUND`。第三方上手视频发布日期：2026-02-04，同样为 `BACKGROUND`。

- Meta CES 官方页：https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/
- 第三方上手视频：VoodooDE VR English，`Meta Ray-Ban Update: Neural Handwriting & Teleprompter Hands-On`，https://www.youtube.com/watch?v=wKCAFUscTao 。视频描述含付费/联盟披露，不能替代官方产品承诺。

官方页面文字证实：可从 Notes、Google Docs 或 Meta AI 复制粘贴文本；眼镜显示可定制文字卡；用户用 Meta Neural Band 导航，并按自己的节奏推进。官方文字没有说明自动滚动或一个独立的“速度控制器”。

| 文件 | 时间码 | 来源 URL / 页面状态 | 实际画面与边界 |
|---|---:|---|---|
| `01-hud-card.png` | 静态 | https://about.fb.com/br/wp-content/uploads/sites/11/2026/01/download-_3_.jpg；官方静态图 | 官方合成/宣传 POV：镜片边缘内显示单张提词卡，顶部 10:41 PM 与 00:11 计时。源图仅 750×422。 |
| `02-setup-modes-and-text-size.png` | 00:01:47 | https://www.youtube.com/watch?v=wKCAFUscTao；第三方手机实拍 | 设置界面明确显示 `Scroll vertically`、已选 `Swipe horizontally`、`Text Size` 与 `Send to Meta RB Display`。这是滚动模式与字号设置，不是独立速度控制。1250×700，低于 1280px。 |
| `03-through-lens-card-state-a.png` | 00:03:39 | 同上；第三方相机透镜取景 | 镜内文字卡，页面指示为 `11 of 14`；腕带佩戴者手部也在画面中。不能从单帧确定触发动作。1250×700。 |
| `04-through-lens-card-state-b.png` | 00:03:44 | 同上；第三方相机透镜取景 | 另一镜内文字卡状态；页码无法可靠读取，因此只记 state-b。1250×700。 |
| `05-through-lens-card-state-c.png` | 00:03:49 | 同上；第三方相机透镜取景 | 镜内文字卡，页面指示为 `2 of 14`；腕带佩戴者手部也在画面中。1250×700。 |

三张透镜图来自同一公开视频的不同时点，但本地没有可逐帧审计的连续视频，因此不能称为相邻卡片或连续滚动序列。正式状态：`PARTIAL`；已满足三张镜内状态图，仍缺本地连续片、真实滚动速度证据和退出状态。
