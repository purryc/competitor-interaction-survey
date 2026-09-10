# Google 素材 QA

验收日期：2026-09-09

## 自动检查

- 32 个正式 PNG；所有**画布**宽度 ≥1280。
- 5 个 MP4；时长分别为 6.94、19.82、22.67、23.13、29.50 秒，全部 ≤30 秒。
- 5 个 MP4 均用 `ffmpeg -v error -i <file> -f null -` 完整解码通过。
- `coverage.json` 通过 JSON 解析；README 的本地图片/文档链接全部存在。
- 6 个素材目录均有 `source.md`；SOURCES.md 覆盖全部 37 个正式媒体文件。

复现命令：`_tools/verify_assets.sh`

## 有效源分辨率例外

- Chrome：7 个 PNG 的源视频为 1080×1920；左右补白后画布为 1920×1920。有效源宽仍为 1080。
- YouTube Shorts：2 个 PNG 的源视频为 1080×1080；左右补白后画布为 1280×1080。有效源宽仍为 1080。
- 共 9 个 PNG 不能按“有效源宽 ≥1280”验收；没有上采样，保留为真实竖屏证据并计入 PARTIAL。

## 人工目检

- Spark：入口、任务列表、委托、工具调用、Needs input、Docs 产物、主动通知/结果及整体关闭设置均为有效画面；Needs input 未被误写为批准动作，关闭按钮未点击。
- 用量：两张真实 UI 已遮挡个人导航/头像；只表述采集时账户状态。
- Chrome：已重做为入口、委托、计划确认、Task started、暂停控件、商家复核、Added to Cart；商家 Review 未被误写为 Gemini 审批，Task done 未被误写为付款。
- Omni：Gemini app 的 `Create with Omni` 和 Shorts 的 Remix/Reimagine 清晰；Flow 只证明项目画布 Agent 入口，模型选择器缺失。
- Android XR：正式素材只用完成解码的 `keynote2-*`；音频线的语音唤醒、导航、手机任务、确认、手表预览均可辨。显示线第二帧明确标为历史演示回顾。
- 产品图为 Google 官方 2026 静态图；没有 AI 生成图、文字页占位或来源不明图片。

## 验收结论

- COMPLETE：0
- PARTIAL：6
- MISSING：0

PARTIAL 原因逐项记录在 `coverage.json` 与各目录 `source.md`；当前已有公开候选均已审阅并作出收录、降级或缺口处置。
