# Gemini Spark 素材来源

采集日期：2026-09-09

## 来源 A：Google I/O 2026 Keynote

- 页面：https://www.youtube.com/watch?v=amnhF6BwzZQ
- 标题：Gemini Spark | I/O 2026 Keynote
- 发布方：Google（官方）
- 画面性质：发布会现场 Live Demo；浏览器播放后等待解码，再按播放器时间码截帧。页面播放器与字幕保留，以便复核。
- 文件与时间码：
  - `01-entry.png`：00:15，Gemini app 的 Chat 入口。
  - `02-task-dashboard.png`：00:21，切入 Spark 任务列表。
  - `03-delegate.png`：00:31，输入并提交任务。
  - `04-progress.png`：01:14，工具调用过程。
  - `05-needs-input.png`：06:18，任务列表出现 `Needs input`；只证明需要用户输入，不证明批准或拒绝动作已展示。
  - `06-artifact.png`：06:33，已完成任务及 Google Docs 产物。
- 下载边界：`yt-dlp` 在 2026-09-09 被 YouTube 的 “Sign in to confirm you’re not a bot” 阻断，因此未保存该长视频；保留官方 URL、逐帧时间码及浏览器解码截图。

## 来源 B：Google 官方文章内嵌 MP4

- 页面：https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni-3-5-videos/
- 直链：https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Gemini_Spark_UI.mp4
- 发布方：Google（官方）
- `07-proactive-notification.png`：00:00.4，系统通知主动提出准备任务。
- `08-proactive-result.png`：00:05.7，任务结果回到 Gemini/Spark 详情。
- `clip.mp4`：官方 6.94 秒原片，未裁剪。

## 文字规则来源

- Spark 设置、首次网页浏览许可、任务确认、停止、取消、接管远程浏览器、整体关闭：https://support.google.com/gemini/answer/17094507?hl=en
- 2026-06-30 更新：https://blog.google/innovation-and-ai/products/gemini-app/gemini-spark-updates-june-2026/
- 2026-07 全球可用性边界：https://blog.google/products-and-platforms/products/gemini/gemini-drop-july-2026/

## 来源 C：当前 Gemini Spark Settings 自测

- 页面：https://gemini.google.com/gemini-spark
- `09-turn-off-settings.png`：当前账户只读打开设置页，显示整体 `Turn off Gemini Spark`、删除远程浏览数据、删除远程代码执行数据。没有点击任何关闭或删除按钮。
- 隐私处理：原始 1280×720 截图的左侧个人导航区以纯白遮挡；主设置卡片未裁切、未放大。

未观察状态：首次权限屏、否决一次主动建议的实际控件、批准/拒绝对话本体。
