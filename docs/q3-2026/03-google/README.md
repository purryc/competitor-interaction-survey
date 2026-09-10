# Google｜2026 Q3 官方素材包

采集日期：2026-09-09。只含 Google；事实、公开演示、自测、推断和素材缺口分开标注。

## §1 一句话结论

Spark 把显式委托延伸为后台任务与主动通知。

证据边界：未采用任务书草案“取消提示词”，因为 Spark 仍有 `Describe a task`，Chrome agent 仍需输入任务、复核计划并点击 `Start task`。

## §2 产品矩阵

| 产品 / 模式 | 能碰到什么 | 权限与执行边界 | 产物落在哪 | 当前证据 |
|---|---|---|---|---|
| Gemini app / Chat | 用户主动提供的文本、图片、文件及已连接服务 | 对话内显式委托；生成、搜索和应用连接受账户/地区/套餐限制 | 对话、生成媒体、链接到 Google 文件 | 官方产品页与 Gemini app Omni UI |
| Gemini Spark | 邮件、日历、Drive/Workspace 文件、网页与连接应用；按任务组织 | 在云端持续运行；首次网页浏览、外部通信、数据更改、购买等场景按帮助中心规则需要许可或确认；可停止、取消、接管或整体关闭 | Spark 任务列表、文件、计划、Google Docs/Sheets/Slides 等产物 | I/O Live Demo、官方 UI 短片、帮助中心；关键设置画面不全 |
| Gemini in Chrome | 当前网页、浏览上下文及代理新开的标签页 | 先展示任务计划并由用户 Start task；运行中有暂停/关闭控件；官方说明敏感操作需确认 | 网页状态、购物车等站内结果，及 Gemini 任务摘要 | Android Chrome 官方模拟演示 |
| Workspace 内嵌 Gemini | Gmail、Docs、Sheets、Slides 等当前工作对象 | 权限跟随 Workspace 账户、共享和文件权限；高影响修改仍受各产品确认机制约束 | 原文件、草稿、表格、幻灯片 | 本轮只核对官方说明，未单独采集特性帧 |
| Gemini 3.5 Flash / Gemini Omni Flash | 面向对话、理解和视频生成的模型能力；由上层产品暴露 | 不作为独立委托面；入口、配额和可用性由 Gemini app、Flow、YouTube 等产品决定 | 对话响应、图像/视频资产、Flow 项目或 Shorts | Gemini app、Flow、YouTube 三处官方素材；Flow 画布未显式显示模型选择器 |

名称与日期纠偏：Gemini Spark 于 Google I/O 2026（2026-05-19）发布；“Omni Flash”是 I/O 发布期名称。2026-08-27 的开发者更新为 Gemini Omni 1.1 Flash，不能倒写进 5 月的 UI 画面。

## §3 特性详解 ×N

### 3.1 Gemini Spark 常驻与主动任务｜PARTIAL

交互流程：

| 阶段 | 观察结果 |
|---|---|
| 进入 | **已见**：Gemini app 从 Chat 切到 Spark 的独立任务面。
| 委托 | **已见**：用户输入任务；也可从移动端以语音委托。
| 过程 | **已见**：任务列表、工具调用、跨设备同步和后台运行；官方短片展示主动通知。
| 接管 | **部分**：列表显示 `Needs input`；帮助中心说明可确认、停止、取消及接管远程浏览器，但实际批准/拒绝对话未见。
| 产物 | **已见**：任务详情、Google Docs/Sheets/Slides 与购物清单结果。
| 退出 | **已见**：当前 Gemini Spark Settings 有整体 `Turn off`，并说明关闭会删除远程浏览/代码执行数据、停止 schedules；本轮未点击。

一句差异点：任务以持续运行的任务队列存在，并能在设备锁定/离线于前台时继续处理；本轮只把该行为写为官方演示/说明，首次授权界面仍缺，整体 Turn off 设置已实际截取但未点击。

来源组 A｜I/O 2026 Live Demo（00:15 → 06:33）：

![Spark 入口](../../../media/q3-2026/03-google/assets/gemini-spark/01-entry.png)
![Spark 任务面](../../../media/q3-2026/03-google/assets/gemini-spark/02-task-dashboard.png)
![Spark 委托](../../../media/q3-2026/03-google/assets/gemini-spark/03-delegate.png)
![Spark 工具调用](../../../media/q3-2026/03-google/assets/gemini-spark/04-progress.png)
![Spark Needs input](../../../media/q3-2026/03-google/assets/gemini-spark/05-needs-input.png)
![Spark 文档产物](../../../media/q3-2026/03-google/assets/gemini-spark/06-artifact.png)

来源组 B｜Google 官方 6.94 秒 UI 短片：

![Spark 主动通知](../../../media/q3-2026/03-google/assets/gemini-spark/07-proactive-notification.png)
![Spark 主动任务结果](../../../media/q3-2026/03-google/assets/gemini-spark/08-proactive-result.png)

来源组 C｜当前账户只读自测（个人侧栏已遮挡）：

![Spark 整体关闭设置](../../../media/q3-2026/03-google/assets/gemini-spark/09-turn-off-settings.png)

缺口：首次授权屏、否决一次主动建议、批准/拒绝对话本体。

### 3.2 从条数到算力的用量表达｜PARTIAL

交互流程：

| 阶段 | 观察结果 |
|---|---|
| 进入 | **已见**：Gemini Usage limits 与 Google One AI credits activity 两个独立页面。
| 委托前 | **未见**：没有观察到单次任务的事前用量估价。
| 过程 | **规则已核**：Gemini 按提示复杂度、所用模型/功能及对话长度消耗；Flow 另有按生成类型计 credits 的固定表。
| 接近上限 | **规则已核、画面未见**：帮助中心说明会在接近/达到上限时提醒。
| 产物 | **已见**：当前五小时窗口、周窗口百分比，以及 credits 余额/活动页。
| 退出 | **不适用**：这是账户用量查看页，不是代理任务。

一句差异点：聚合用量用“当前窗口 + 周窗口”表达，而 Flow 等创作产品仍保留可计算的 credits；本轮没有证据证明 Gemini 会逐任务显示成本。

![Gemini 用量窗口](../../../media/q3-2026/03-google/assets/compute-billing/01-gemini-usage-limits.png)
![Google One AI credits activity](../../../media/q3-2026/03-google/assets/compute-billing/02-google-one-ai-credits.png)

自测边界：两图均为采集时账户状态，个人导航/头像已遮挡；0% 与空活动不能外推为产品默认。缺口为单次成本、事前估价和临近额度实际弹窗。

### 3.3 Gemini in Chrome agent｜PARTIAL

交互流程：

| 阶段 | 观察结果 |
|---|---|
| 进入 | **已见**：网页内打开 Gemini 面板。
| 委托 | **已见**：用户输入寻找并个性化狗碗的任务。
| 过程 | **已见**：先呈现任务计划，用户 Start task 后代理跨标签浏览；底部任务条持续显示范围。
| 接管 | **部分**：有暂停、关闭、Switch tabs 控件；未看到点击暂停/接管后的独立状态。
| 产物 | **已见**：个性化商品加入购物车，Gemini 给出任务摘要。
| 退出 | **已见到任务终止态**：`Task done` 只代表加购物车结束；未下单、未付款。

一句差异点：代理工作时，网页内容仍保持前台，底部任务条持续显示“正在做什么”及暂停/关闭控件；商家 Review 页面属于商家站内复核，不能当作 Gemini 的敏感操作批准。

来源组｜Google 官方 Android Chrome 模拟演示（00:02 → 00:45）：

![Chrome 入口](../../../media/q3-2026/03-google/assets/gemini-in-chrome/01-entry.png)
![Chrome 委托](../../../media/q3-2026/03-google/assets/gemini-in-chrome/02-delegate.png)
![Chrome 计划确认](../../../media/q3-2026/03-google/assets/gemini-in-chrome/03-plan-confirmation.png)
![Chrome 任务开始](../../../media/q3-2026/03-google/assets/gemini-in-chrome/04-task-started.png)
![Chrome 暂停控件](../../../media/q3-2026/03-google/assets/gemini-in-chrome/05-pause-control.png)
![Chewy 商家复核页](../../../media/q3-2026/03-google/assets/gemini-in-chrome/06-merchant-review.png)
![Chrome 加购物车结束](../../../media/q3-2026/03-google/assets/gemini-in-chrome/07-added-to-cart.png)

原片声明：结果用于示意、序列缩短且屏幕画面为模拟。缺口为点击接管后的状态、付款前代理审批及付款完成。

分辨率边界：原视频有效内容为 1080×1920 竖屏；正式 PNG 仅左右补白成 1920×1920 画布，没有上采样。画布宽达到 1280 不等于有效源宽达到 1280，此项记录为 resolution gap。

### 3.4 Gemini Omni 的三处 UI 暴露｜PARTIAL

| 入口 | 观察结果 |
|---|---|
| Gemini app | **已见**：视频生成输入面直接写 `Create with Omni`。
| Google Flow | **部分**：项目画布底部 Agent 输入面已见；当前产品页的 Models/定价区明确列 Gemini Omni / Omni Flash，但画布帧没有模型选择器。
| YouTube Shorts | **已见**：Short 右侧 `Remix` → `Reimagine`。

一句差异点：同一生成能力在三个产品中分别以对话生成器、项目画布 Agent 和内容 Remix 工具出现，入口名称随任务环境变化。

![Gemini app Omni 入口](../../../media/q3-2026/03-google/assets/omni-entries/01-gemini-app-entry.png)
![Flow Agent 入口](../../../media/q3-2026/03-google/assets/omni-entries/02-flow-entry.png)
![Shorts Remix 入口](../../../media/q3-2026/03-google/assets/omni-entries/03-youtube-shorts-remix-entry.png)
![Shorts Reimagine](../../../media/q3-2026/03-google/assets/omni-entries/04-youtube-shorts-reimagine.png)

缺口：Flow 项目画布内明确标注 Omni 的模型选择器。

分辨率边界：YouTube Shorts 原视频为 1080×1080，正式 PNG 仅左右补白成 1280×1080；有效源宽仍为 1080，记录为 resolution gap。Gemini app 与 Flow 原片为 1920×1080。

## §4 新硬件

### 4.1 Android XR 音频眼镜｜PARTIAL

官方状态：Google 在 2026-05-19 说明首批 audio glasses 于 2026 年秋季推出；合作框架涉及 Samsung、Qualcomm，镜框品牌包括 Gentle Monster 与 Warby Parker；支持配对 Android 与 iOS。

为什么要有：官方定义是把 Gemini 的帮助以私密音频放在耳边，用户不必拿出手机或把视线移到屏幕。可执行导航、通话、消息、音乐、拍摄与第三方任务。

新交互：官方文字说明可说 “Hey Google” 或轻触镜腿唤醒；Live Demo 展示语音导航、手机在口袋时启动任务、语音确认订单，以及在手表预览结果。

来源组 A｜I/O 2026 Live Demo（02:20 → 10:35）：

![音频眼镜发布](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/01-audio-launch.png)
![语音唤醒](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/02-wake.png)
![语音导航](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/03-navigation.png)
![手机侧任务联动](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/04-phone-link.png)
![任务过程](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/05-action-progress.png)
![语音确认](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/06-voice-confirmation.png)
![手表预览](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/07-watch-preview.png)

来源组 B｜2026 官方产品图：

![Android XR 智能眼镜官方图](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/08-official-hardware-hero.png)

证据边界：确认动作已见；取消动作、轻触镜腿画面和 Pixel 品牌专属联动未见。演示只证明“手机联动”，且官方写的是 Android/iOS，不应改写为 Pixel 独占。

### 4.2 Android XR 镜片内显示眼镜｜PARTIAL

官方状态纠偏：同一篇 2026 发布材料只对首批**音频眼镜**给出秋季推出承诺。Android XR 状态页对 fashion display glasses 仍写 `Stay tuned`。XREAL AURA 是另一个 2026 秋季推出的有线空间显示产品，不能拿来证明 Gentle Monster / Warby Parker 镜片内显示款已经定档。

为什么要有：官方定义是把导航、翻译、叫车状态等可扫视信息放在视野中，减少看手机；与只在耳边播报的音频眼镜承担不同反馈通道。

![两类眼镜](../../../media/q3-2026/03-google/assets/android-xr-display-glasses/01-two-types.png)
![镜片内显示历史参考](../../../media/q3-2026/03-google/assets/android-xr-display-glasses/02-in-lens-reference.png)

第二张是 2026 Keynote 对此前舞台演示的回顾，只能当方向参考。缺口为 2026 当前版本从唤醒、显示、确认/取消到退出的完整画面链。

## §5 拆分逻辑

| 归因 | 可观察的拆分边界 |
|---|---|
| 工具装载 | Chat 按对话调用工具；Spark 按长期任务连接 Workspace、网页和应用；Chrome agent 把工具范围收敛到浏览器标签；Omni 由 Gemini app、Flow、YouTube 各自包装。
| 产物形态 | Chat 产物留在对话；Spark 可生成任务、计划和 Workspace 文件；Chrome 改变网页/购物车状态并给摘要；Omni 产出视频资产或项目内容。
| 爆炸半径 | Gemini app Chat 以对话内容和用户选择的文件/连接服务为边界；Spark 和 Chrome 还可改变外部服务或网页状态，因此增加首次许可、任务计划、确认、暂停、取消或接管规则；眼镜把同类委托入口带到持续佩戴设备，高影响动作仍需确认。
| 反馈回路 | Chat 是同步来回；Spark 是任务队列 + 后台进度 + Needs input；Chrome 是网页前台 + 持续任务条；音频/显示眼镜分别用耳边播报和视野内 glanceable 信息闭环。
| 买单人 | Gemini app、Flow 与 Spark 的额度受个人订阅层级影响；Workspace 能力同时受组织账户/文件权限约束；眼镜由消费者购买硬件并通过 Android/iOS 手机连接。

## §6 三个必答问题

1. **它把能力拆成了几块，边界画在哪？** 本轮可核为四层：对话入口（Gemini app）、长期任务运行面（Spark）、当前网页操作面（Chrome agent）、模型/生成能力被嵌入的创作面（Omni in Gemini app / Flow / YouTube），另有 Workspace 文件面和 Android XR 佩戴载体。边界分别由可访问文件、外部动作权限和产物落点决定。
2. **它的委托面在往哪走——更显式还是更隐式？** 同时存在三档：Chat/Omni 仍需输入，Chrome 先显式写任务再执行，Spark 能从长期上下文和主动通知把入口推向“不用每次重新说”。本轮已取得整体 Turn off 设置与其数据清理、停止 schedules 说明，但未点击；首次授权与逐次批准/拒绝画面仍缺，不能据此判断用户是否能充分感知全部后台范围。
3. **它的硬件在补软件的哪块短板？** 音频眼镜补“必须拿出手机/看屏”的入口成本，以耳边私密语音承接即时任务；显示眼镜尝试补“语音不适合传达可扫视空间信息”的反馈短板。2026 年确定的秋季产品是音频线，display 线仍缺同等明确的当前出货与完整交互证据。

## §7 素材与出处表

以下逐文件表与 [SOURCES.md](SOURCES.md) 同步；同源重复参考不增加独立流程帧数。

抓取日期统一为 2026-09-09。时间码均指向未裁剪的官方源视频；`—` 表示网页自测或静态产品图。

### 来源登记

- **S1** Google Keynote｜Gemini Spark：https://www.youtube.com/watch?v=amnhF6BwzZQ
- **S2** Google 官方 CDN｜Gemini Spark UI：https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Gemini_Spark_UI.mp4 （页面：https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-omni-3-5-videos/）
- **S3** Gemini Usage limits 自测：https://gemini.google.com/usage
- **S4** Google One AI credits activity 自测：https://one.google.com/u/0/ai/activity?g1_landing_page=0
- **S5** Google 官方 CDN｜Chrome auto browse：https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4 （页面：https://blog.google/products-and-platforms/products/chrome/bringing-chrome-ai-to-android/）
- **S6** Google 官方 CDN｜Gemini Omni UI：https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Shorter-Demo_Gemini_Omni_v68_1_yuOg8je.mp4 （页面：https://blog.google/innovation-and-ai/products/gemini-app/next-evolution-gemini-app/）
- **S7** Google 官方 CDN｜Flow Agent：https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/GoogleFlow-Agent.mp4 （页面：https://blog.google/innovation-and-ai/models-and-research/google-labs/flow-updates/）
- **S8** YouTube 官方 CDN｜Omni in Shorts：https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Omni_Happy-Kelli_8Bit_Frank-Likeness_Gif_V15-compressed.mp4 （页面：https://blog.youtube/news-and-events/youtube-news-google-io-2026/）
- **S9** Google Keynote｜Intelligent Eyewear：https://www.youtube.com/watch?v=xxY0yuzxzLY
- **S10** Google 官方静态图：https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Hero_Image_ggl_xr_io.width-2200.format-webp.webp （页面：https://blog.google/products-and-platforms/platforms/android/android-xr-io-2026/）
- **S11** Gemini Spark Settings 自测：https://gemini.google.com/gemini-spark

### 逐文件表

| 文件 | 对应特性 | 来源 | 时间码 | 官方与否 / 说明 | 抓取日期 |
| --- | --- | --- | --- | --- | --- |
| [assets/gemini-spark/01-entry.png](../../../media/q3-2026/03-google/assets/gemini-spark/01-entry.png) | Spark 进入 | [S1](https://www.youtube.com/watch?v=amnhF6BwzZQ) | 00:15 | Google 官方 Live Demo | 2026-09-09 |
| [assets/gemini-spark/02-task-dashboard.png](../../../media/q3-2026/03-google/assets/gemini-spark/02-task-dashboard.png) | Spark 任务面 | [S1](https://www.youtube.com/watch?v=amnhF6BwzZQ) | 00:21 | Google 官方 Live Demo | 2026-09-09 |
| [assets/gemini-spark/03-delegate.png](../../../media/q3-2026/03-google/assets/gemini-spark/03-delegate.png) | Spark 委托 | [S1](https://www.youtube.com/watch?v=amnhF6BwzZQ) | 00:31 | Google 官方 Live Demo | 2026-09-09 |
| [assets/gemini-spark/04-progress.png](../../../media/q3-2026/03-google/assets/gemini-spark/04-progress.png) | Spark 工具调用 | [S1](https://www.youtube.com/watch?v=amnhF6BwzZQ) | 01:14 | Google 官方 Live Demo | 2026-09-09 |
| [assets/gemini-spark/05-needs-input.png](../../../media/q3-2026/03-google/assets/gemini-spark/05-needs-input.png) | Spark 接管提示 | [S1](https://www.youtube.com/watch?v=amnhF6BwzZQ) | 06:18 | 只证明 Needs input | 2026-09-09 |
| [assets/gemini-spark/06-artifact.png](../../../media/q3-2026/03-google/assets/gemini-spark/06-artifact.png) | Spark 产物 | [S1](https://www.youtube.com/watch?v=amnhF6BwzZQ) | 06:33 | Google Docs 产物 | 2026-09-09 |
| [assets/gemini-spark/07-proactive-notification.png](../../../media/q3-2026/03-google/assets/gemini-spark/07-proactive-notification.png) | Spark 主动通知 | [S2](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Gemini_Spark_UI.mp4) | 00:00.4 | Google 官方 UI 演示 | 2026-09-09 |
| [assets/gemini-spark/08-proactive-result.png](../../../media/q3-2026/03-google/assets/gemini-spark/08-proactive-result.png) | Spark 主动结果 | [S2](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Gemini_Spark_UI.mp4) | 00:05.7 | Google 官方 UI 演示 | 2026-09-09 |
| [assets/gemini-spark/clip.mp4](../../../media/q3-2026/03-google/assets/gemini-spark/clip.mp4) | Spark 主动任务 | [S2](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Gemini_Spark_UI.mp4) | 00:00–00:06.94 | 官方原片，未裁剪 | 2026-09-09 |
| [assets/gemini-spark/09-turn-off-settings.png](../../../media/q3-2026/03-google/assets/gemini-spark/09-turn-off-settings.png) | Spark 整体关闭 | [S11](https://gemini.google.com/gemini-spark) | — | 官方产品真实 UI 自测；未点击 Turn off；个人侧栏已遮挡 | 2026-09-09 |
| [assets/compute-billing/01-gemini-usage-limits.png](../../../media/q3-2026/03-google/assets/compute-billing/01-gemini-usage-limits.png) | 当前/周用量 | [S3](https://gemini.google.com/usage) | — | 官方产品真实 UI 自测；个人导航已遮挡 | 2026-09-09 |
| [assets/compute-billing/02-google-one-ai-credits.png](../../../media/q3-2026/03-google/assets/compute-billing/02-google-one-ai-credits.png) | Credits 余额/活动 | [S4](https://one.google.com/u/0/ai/activity?g1_landing_page=0) | — | 官方产品真实 UI 自测；账户头像已遮挡 | 2026-09-09 |
| [assets/gemini-in-chrome/01-entry.png](../../../media/q3-2026/03-google/assets/gemini-in-chrome/01-entry.png) | Chrome 进入 | [S5](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4) | 00:02 | Google 官方模拟演示 | 2026-09-09 |
| [assets/gemini-in-chrome/02-delegate.png](../../../media/q3-2026/03-google/assets/gemini-in-chrome/02-delegate.png) | Chrome 委托 | [S5](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4) | 00:08 | Google 官方模拟演示 | 2026-09-09 |
| [assets/gemini-in-chrome/03-plan-confirmation.png](../../../media/q3-2026/03-google/assets/gemini-in-chrome/03-plan-confirmation.png) | Chrome 计划确认 | [S5](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4) | 00:12 | Cancel / Start task | 2026-09-09 |
| [assets/gemini-in-chrome/04-task-started.png](../../../media/q3-2026/03-google/assets/gemini-in-chrome/04-task-started.png) | Chrome 任务开始 | [S5](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4) | 00:16 | 步骤列表 / Switch tabs | 2026-09-09 |
| [assets/gemini-in-chrome/05-pause-control.png](../../../media/q3-2026/03-google/assets/gemini-in-chrome/05-pause-control.png) | Chrome 运行控制 | [S5](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4) | 00:21 | 暂停 / 关闭控件可见，点击后状态未见 | 2026-09-09 |
| [assets/gemini-in-chrome/06-merchant-review.png](../../../media/q3-2026/03-google/assets/gemini-in-chrome/06-merchant-review.png) | 商家侧复核 | [S5](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4) | 00:38 | Chewy Review；不是 Gemini 审批 | 2026-09-09 |
| [assets/gemini-in-chrome/07-added-to-cart.png](../../../media/q3-2026/03-google/assets/gemini-in-chrome/07-added-to-cart.png) | Chrome 任务结果 | [S5](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4) | 00:45 | 只到 Added to Cart / Task done | 2026-09-09 |
| [assets/gemini-in-chrome/clip.mp4](../../../media/q3-2026/03-google/assets/gemini-in-chrome/clip.mp4) | Chrome 代理过程 | [S5](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/260511_Chewy_Bowl_with_disclaimer_zBaCcOC.mp4) | 原片 00:17–00:46.5 | 裁为 29.5 秒；H.264 重编码 | 2026-09-09 |
| [assets/omni-entries/01-gemini-app-entry.png](../../../media/q3-2026/03-google/assets/omni-entries/01-gemini-app-entry.png) | Gemini app 入口 | [S6](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Shorter-Demo_Gemini_Omni_v68_1_yuOg8je.mp4) | 00:01 | `Create with Omni` | 2026-09-09 |
| [assets/omni-entries/02-flow-entry.png](../../../media/q3-2026/03-google/assets/omni-entries/02-flow-entry.png) | Flow 入口 | [S7](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/GoogleFlow-Agent.mp4) | 00:02 | Flow Agent 输入面；帧内未标模型 | 2026-09-09 |
| [assets/omni-entries/03-youtube-shorts-remix-entry.png](../../../media/q3-2026/03-google/assets/omni-entries/03-youtube-shorts-remix-entry.png) | Shorts Remix | [S8](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Omni_Happy-Kelli_8Bit_Frank-Likeness_Gif_V15-compressed.mp4) | 00:08 | YouTube 官方演示 | 2026-09-09 |
| [assets/omni-entries/04-youtube-shorts-reimagine.png](../../../media/q3-2026/03-google/assets/omni-entries/04-youtube-shorts-reimagine.png) | Shorts Reimagine | [S8](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Omni_Happy-Kelli_8Bit_Frank-Likeness_Gif_V15-compressed.mp4) | 00:10.5 | YouTube 官方演示 | 2026-09-09 |
| [assets/omni-entries/clip-gemini-app.mp4](../../../media/q3-2026/03-google/assets/omni-entries/clip-gemini-app.mp4) | Gemini app Omni | [S6](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Shorter-Demo_Gemini_Omni_v68_1_yuOg8je.mp4) | 00:00–00:19.82 | 官方原片，未裁剪 | 2026-09-09 |
| [assets/omni-entries/clip-flow.mp4](../../../media/q3-2026/03-google/assets/omni-entries/clip-flow.mp4) | Flow Agent | [S7](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/GoogleFlow-Agent.mp4) | 00:00–00:22.67 | 官方原片，未裁剪 | 2026-09-09 |
| [assets/omni-entries/clip-youtube-shorts.mp4](../../../media/q3-2026/03-google/assets/omni-entries/clip-youtube-shorts.mp4) | Shorts Omni | [S8](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Omni_Happy-Kelli_8Bit_Frank-Likeness_Gif_V15-compressed.mp4) | 00:00–00:23.13 | 官方原片，未裁剪 | 2026-09-09 |
| [assets/android-xr-audio-glasses/01-audio-launch.png](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/01-audio-launch.png) | 音频线发布 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 02:20 | Google 官方 Keynote | 2026-09-09 |
| [assets/android-xr-audio-glasses/02-wake.png](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/02-wake.png) | 语音唤醒 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 06:20 | “Hey, Gemini” | 2026-09-09 |
| [assets/android-xr-audio-glasses/03-navigation.png](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/03-navigation.png) | 导航 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 07:20 | 语音委托 | 2026-09-09 |
| [assets/android-xr-audio-glasses/04-phone-link.png](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/04-phone-link.png) | 手机联动 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 08:15 | 手机在口袋；非 Pixel 专属证据 | 2026-09-09 |
| [assets/android-xr-audio-glasses/05-action-progress.png](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/05-action-progress.png) | 任务过程 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 08:40 | 手机侧 Task in progress | 2026-09-09 |
| [assets/android-xr-audio-glasses/06-voice-confirmation.png](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/06-voice-confirmation.png) | 语音确认 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 08:55 | Stop task / Take over 同屏 | 2026-09-09 |
| [assets/android-xr-audio-glasses/07-watch-preview.png](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/07-watch-preview.png) | 手表预览 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 10:35 | Wear OS 结果预览 | 2026-09-09 |
| [assets/android-xr-audio-glasses/08-official-hardware-hero.png](../../../media/q3-2026/03-google/assets/android-xr-audio-glasses/08-official-hardware-hero.png) | 硬件外观 | [S10](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/Hero_Image_ggl_xr_io.width-2200.format-webp.webp) | — | Google 官方 2026 产品图 | 2026-09-09 |
| [assets/android-xr-display-glasses/01-two-types.png](../../../media/q3-2026/03-google/assets/android-xr-display-glasses/01-two-types.png) | 音频/显示分类 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 00:45 | Google 官方 Keynote | 2026-09-09 |
| [assets/android-xr-display-glasses/02-in-lens-reference.png](../../../media/q3-2026/03-google/assets/android-xr-display-glasses/02-in-lens-reference.png) | 镜片内显示 | [S9](https://www.youtube.com/watch?v=xxY0yuzxzLY) | 01:05 | 讲者回顾此前演示；历史参考 | 2026-09-09 |

逐目录的变换、限制和未观察状态见对应 `source.md`。

## 待人填：观点 / 对我们的启发
