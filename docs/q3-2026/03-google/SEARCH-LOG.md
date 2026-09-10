# Google 搜索与采集日志

日期：2026-09-09

## 范围与时间窗

- 只研究 Google，不检索其他品牌、不产出趋势总览。证据先查 Google 官方；官方缺指定 UI 状态后，再定向核查可靠媒体的第一手上手，不把二手描述当成正式截图。
- 主要事实窗口为 2026-03-09 之后；优先采用 2026-06-11 之后的更新。I/O 2026 的 5 月材料属于本节指定事件，保留为发布与 UI 主证据。

## 实际检索路径

| 目的 | 查询 / 站点 | 结果与处置 |
|---|---|---|
| Spark 发布与 UI | `site:blog.google Gemini Spark I/O 2026`、Google I/O Keynote | 找到 2026-05-19 发布页、官方 Keynote、6.94 秒 UI MP4；保存 8 帧 + 1 短片 |
| Spark 权限、停止、关闭 | `support.google.com/gemini Gemini Spark permissions turn off take over` | 找到帮助中心规则；无首次权限屏、否决建议或关闭设置截图，保留缺口 |
| Spark 后续状态 | `site:blog.google Gemini Spark June 2026 update`、Gemini Drop July 2026 | 核对 macOS/连接应用/地区可用性；作为文字状态，不混入 UI 证据 |
| Gemini 用量 | `support.google.com/gemini compute based usage limits 2026` | 核到复杂度、模型/功能、对话长度、五小时/周窗口规则 |
| Credits | `support.google.com/googleone AI credits activity`、`support.google.com/flow AI credits` | 核到 activity 页面与 Flow 固定 credits 表；没有单次 Gemini 任务估价截图 |
| 用量界面自测 | `gemini.google.com/usage`、`one.google.com/ai/activity` | 只读打开并截图；未提交提示词、未购买 credits；个人导航/头像已遮挡 |
| Chrome agent | `site:blog.google Chrome Android auto browse 2026` | 找到 46.67 秒官方模拟演示；保存 7 帧并裁 29.5 秒短片 |
| Omni 三入口 | Google Gemini app、Flow、YouTube I/O 2026 官方页面 | 找到 Gemini app、Flow、Shorts 三条官方 MP4；Flow 当前页确认模型清单，但画布帧无模型选择器 |
| Flow 当前状态 | `https://labs.google/fx/tools/flow` 只读核查 | Models 区列 Gemini Omni，免费/订阅清单列 Gemini Omni Flash；未进入生成任务、未消耗 credits |
| Android XR 眼镜 | `site:blog.google Android XR intelligent eyewear I/O 2026`、官方 Keynote | 核对 audio/display 分类、Android/iOS、唤醒、任务和合作方；保存音频线 8 图、显示线 2 图 |
| Android XR 发售状态 | Android XR 状态页、AWE 2026、Galaxy Unpacked 2026 | 纠偏：明确 2026 秋季推出的是 audio glasses；display glasses 为 Stay tuned；XREAL AURA 是单独的有线空间显示产品 |
| Spark 首次许可替代路径 | Google Spark 帮助中心；TechRadar 2026-08-05 第一手上手 `I tried Gemini Spark in Chrome...` | 官方与上手文字均说明首次连接浏览器会请求许可；文章没有可作为 UI 序列的首次许可截图，缺口保留 |
| Spark 整体关闭只读自测 | 当前账户 `gemini.google.com` → Settings → Gemini Spark Settings | 成功取得真实设置页，显示 `Turn off Gemini Spark` 及数据/计划影响；未点击关闭，个人侧栏遮挡后收入正式素材 |
| Chrome 暂停后状态替代路径 | Gemini Apps Help `answer/16821166`；定向搜索 2026 上手 | 官方帮助明确 Pause→Resume、Take over→Resume/Give back task；没有取得点击后的完整 UI 帧，正式素材保留暂停控件并维持缺口 |

## 失败与排除

- 两个 YouTube Keynote 使用 `yt-dlp` 下载时均返回 “Sign in to confirm you’re not a bot”。处理：浏览器播放、等待解码、导出转录并按时间码截帧；不伪造本地长视频。
- Android XR Keynote 第一轮跳转后立即截图，得到多个重复封面。处理：重做并在每次跳转后等待约 600 ms 完成解码；正式目录只使用 `keynote2-*`，旧图留在 `_work/` 作为失败记录。
- Spark Keynote 中的 `Needs input` 只证明任务待用户输入；未把它标成批准/拒绝对话。当前账户可见整体关闭设置，但首次连接许可仍只有文字规则与第一手上手描述。
- Chrome 的 Chewy `Review / Edit / Add To Cart` 是商家复核页；未标成 Gemini 敏感操作审批。`Task done` 只到加入购物车，不代表付款。
- Flow Agent 画面虽来自 Gemini Omni for Google Flow 的官方发布页，画布本身未显示模型选择器；保留 PARTIAL。
- 正式 PNG 均为真实官方 UI/Keynote/产品图或真实账户 UI 自测；没有 AI 生成图、文字页替代图、无来源截图或上采样图。

## 明确停止继续泛搜的缺口

- Spark：首次权限屏、否决建议、整体关闭、批准/拒绝对话。
- 用量：单次任务消耗、提交前估价、低余额/临近上限实拍。
- Chrome：暂停/接管点击后的状态、付款审批、付款完成。
- Omni：Flow 画布中的明确 Omni 模型选择器。
- Android XR：轻触镜腿实拍、取消动作、Pixel 专属联动；2026 display glasses 完整交互链与明确出货日期。

这些状态在本轮已查阅官方发布、帮助中心、当前产品页和官方视频；继续无目标泛搜的预期收益低，按采集手册以证据缺口收口。
