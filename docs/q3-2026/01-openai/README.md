# OpenAI｜2026 Q3 交互素材包

采集日：2026-09-09。正式素材为 **58 张 PNG、6 段 MP4**。**当前验收：1 项素材完整、5 项部分、0 项完全无图；硬件产品未核实。本品牌公开素材采集已逐项处置，保留有来源与尝试记录的缺口。**

[可视化审阅入口](review.html) · [逐图出处](SOURCES.md) · [逐特性覆盖](coverage.json) · [检索与失败日志](SEARCH-LOG.md) · [最终状态](STATUS.md) · [逐项处置与补采条件](EVIDENCE-DISPOSITION.md)

## §1 一句话结论

**进入 Work 后，用 @ 把外部应用带入任务，并在对话中查看过程与产物。**

草案中的“不切模式”未采用：官方图明确显示 Chat / Work 选择；@ 教学帧证明的是进入任务后的应用引用。不能据此声称无需选择 Work。[官方发布页](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) · [真实 @ 教学](https://learn.chatgpt.com/training/walkthroughs/plugins-and-skills)

## §2 产品矩阵

| 产品/模式 | 能碰到什么 | 权限边界 | 产物落点与状态 |
|---|---|---|---|
| ChatGPT Chat | 用户输入、上传资料、可用连接源 | 账号与工作区设置适用 | 主要在对话内回答；不据名称推断全部工具边界 |
| ChatGPT Work | 上传/连接的文件、授权应用；桌面支持本地文件、浏览器与 Computer Use | 应用授权、网站访问、动作批准、管理员策略分别适用 | 文件、原生 Google Workspace 文件、Sites；2026-07-09 官方发布 |
| Codex | 项目代码和相关本地/远程环境；能力随工具和连接而定 | 环境访问与动作审批适用 | 工作目录、代码变更、应用等；和 Work 同处新桌面应用，不把两者所有权限视为相同 |
| GPT-Live / ChatGPT Voice | 语音与支持的图片/文件；复杂工作可委派后台模型 | 语音使用额度、账号与具体能力限制适用 | 语音对话与视觉回答卡片；2026-07-08 发布，页面说明全球 iOS、Android、Web 推出 |
| ChatGPT Atlas | 历史浏览器页面、标签上下文与 agent 操作 | 历史页面确认、接管/停止控件 | **已弃用**；官方计划 2026-08-09 停止工作。采集的 2025-10-21 视频只作背景；未实测停服 |

矩阵依据：[Work 与 Codex](https://help.openai.com/en/articles/20001275)、[浏览器边界](https://learn.chatgpt.com/docs/browser?surface=app)、[文件创建](https://help.openai.com/en/articles/20001278-creating-and-editing-documents-spreadsheets-and-presentations-with-chatgpt-work)、[GPT-Live](https://openai.com/index/introducing-gpt-live/)、[Atlas 弃用说明](https://help.openai.com/en/articles/20001371)。具体可用性依套餐、市场、设备和工作区设置，不能用官方演示推断用户账号均可用。

时间口径：Work 发布演示显示 GPT-5.6；当前帮助文档已列 GPT-6 Astra。语音发布页说启动时后台为 GPT-5.5；不将该启动快照当作 9 月所有账号的后台配置。

## §3 特性详解 ×N

N=6。每条流程均区分“看见界面”“官方文字说明”“未展示”。PNG 保留原画幅；源宣传片本身有特写与剪辑。画面中的演示数据、任务耗时和结果不属于本次实测。

### Work 的 @ 提及调用 · PARTIAL

一句差异点（描述已见交互）：应用以带图标的输入标签被引用。

| 阶段 | 素材实际覆盖 |
|---|---|
| 进入 | 模式菜单已见 |
| 委托 | @cal 列表、内联标签、请求已见 |
| 过程 | 日历时段与运行状态已见 |
| 接管 | 未见接管 |
| 产物 | 候选时段已见，仍 Working |
| 退出 | 未见退出 |

**素材缺口：**一句话多个应用标签并列的 UI；教学视频独立发布日

![输入 @cal 后出现候选列表；Google Calendar 与文档/任务同列；源镜头局部放大。](assets/work-mention/01-at-candidates.png)

01:06 — 输入 @cal 后出现候选列表；Google Calendar 与文档/任务同列；源镜头局部放大。

![选中 Google Calendar 后出现带图标的内联标签；源镜头局部放大。](assets/work-mention/02-inline-app.png)

01:07 — 选中 Google Calendar 后出现带图标的内联标签；源镜头局部放大。

![完整请求包含一个 Google Calendar 标签；未见多个应用。](assets/work-mention/03-delegate.png)

01:08 — 完整请求包含一个 Google Calendar 标签；未见多个应用。

![任务已开始，过程界面可见。](assets/work-mention/04-progress.png)

01:09 — 任务已开始，过程界面可见。

![已列出候选日历时段，顶部仍 Working for 15s；不是完成或退出。](assets/work-mention/05-calendar-slots-still-working.png)

01:13 — 已列出候选日历时段，顶部仍 Working for 15s；不是完成或退出。

![插件目录，不是 @ 弹出菜单](assets/work-mention/global-plugin-directory.png)

插件目录，不是 @ 弹出菜单 · 2026-07-09 · PRIORITY

![桌面 Work 模式菜单](assets/work-mention/desktop-mode-picker.png)

桌面 Work 模式菜单 · 2026-07-09 · PRIORITY

[逐图来源和时间码](assets/work-mention/source.md) · [本地短片](assets/work-mention/clip.mp4)

补采条件：官方业务运营回放恢复可播，或提供隔离演示账号；本轮已尝试公开播放器和下载，文字资源页双应用示例未当作 UI。

### Work 的人工审批门 · PARTIAL

一句差异点（描述已见交互）：具体网站访问前暂停，权限卡列出目标网站、单次允许、拒绝和扩大权限选项。

**补充证据来自第三方第一手上手，非本次实测。**两篇文章、两个任务独立展示，不合并成一条连续审批流程。官方文档用于权限解释交叉核对。

| 阶段 | 已见 / 未见 |
|---|---|
| 进入与委托 | Windows Work 中调研任务开始运行 |
| 过程 | 承认待ち与目标 help.openai.com 权限卡 |
| 人工决定 | 一度だけ許可、拒否；另一案例展示所有网站许可二次确认 |
| 结果与退出 | 没有拒绝后的继续或终止画面；同一流程只有两张 |

![Windows Work 调研委托开始运行，尚未出现审批卡。](assets/work-approval/thirdparty-windows-01-running.png)

Windows Work 调研委托开始运行，尚未出现审批卡。 作者原有灰色遮挡保留。 文章原图去除1200缩图参数取得原尺寸；未放大、补绘或本次实测。

![任务停在承认待ち；Browser 卡列出 help.openai.com，按钮含拒否、一度だけ許可及所有网站授权。](assets/work-approval/thirdparty-windows-02-access-approval.png)

任务停在承认待ち；Browser 卡列出 help.openai.com，按钮含拒否、一度だけ許可及所有网站授权。 作者原有灰色遮挡和红框保留；没有点击拒绝后的图。 文章原图去除1200缩图参数取得原尺寸；未放大、补绘或本次实测。

![另一案例：note.com 访问卡在下方，前景为允许任意网站且无需再次确认的二次弹窗，含取消和所有网站允许。](assets/work-approval/thirdparty-note-broad-approval-confirm.png)

另一案例：note.com 访问卡在下方，前景为允许任意网站且无需再次确认的二次弹窗，含取消和所有网站允许。 图片来自文章免费可见区。正文称选择单次，但图中实际为扩大权限确认，以图为准；其范围不同于单一动作Always allow。 文章原图去除1200缩图参数取得原尺寸；未放大、补绘或本次实测。

**素材缺口：**同一审批流程四帧、拒绝后的任务状态、官方动作审批原片。所有网站许可与单个动作的持续授权范围不同。

[逐图出处与官方性](assets/work-approval/source.md) · [官方应用权限说明](https://help.openai.com/en/articles/20001495-managing-app-permissions-in-chatgpt)

### 内置浏览器 + Computer Use · PARTIAL

一句差异点（描述已见交互）：Computer Use 展示文字过程与应用画中画。

| 阶段 | 素材实际覆盖 |
|---|---|
| 进入 | Computer 标签与 Browser 内联标签已见 |
| 委托 | Notes→Keynote 委托已见 |
| 过程 | 文字过程与应用画中画已见 |
| 接管 | 未见点击；Cloud browser 登录交接另图 |
| 产物 | Keynote 编辑过程已见 |
| 退出 | 停止按钮已见，按下后未见 |

**素材缺口：**点击接管及之后状态；录像回放入口是否存在；停止结果。浏览器委托/搜索/过程/回答/批注五帧与全局已取得。

![Computer 标签与 Notes 附件；委托修改 Keynote；Approve for me 只是模式标签。](assets/work-browser/01-computer-delegate.png)

00:15 — Computer 标签与 Notes 附件；委托修改 Keynote；Approve for me 只是模式标签。

![Computer Use 运行，过程文字与停止控件可见；未点击停止。](assets/work-browser/02-computer-progress.png)

00:18 — Computer Use 运行，过程文字与停止控件可见；未点击停止。

![Keynote 画中画预览；不是浏览器页面。](assets/work-browser/03-pip-preview.png)

00:24 — Keynote 画中画预览；不是浏览器页面。

![Keynote 画中画继续显示文稿；不是浏览器页面。](assets/work-browser/04-pip-keynote.png)

00:27 — Keynote 画中画继续显示文稿；不是浏览器页面。

![画中画内编辑 Keynote；没有接管动作。](assets/work-browser/05-keynote-edit.png)

00:30 — 画中画内编辑 Keynote；没有接管动作。

![Cloud browser 移动端登录交接，有手动登录和 Skip；不是桌面内置浏览器接管。](assets/work-browser/official-sign-in.png)

Cloud browser 移动端登录交接，有手动登录和 Skip；不是桌面内置浏览器接管。 · 独立发布日期未标 · UNVERIFIED_DATE

![Cloud browser 网站权限设置：Always ask / Auto approve / Always allow；不是单次动作审批卡。](assets/work-browser/official-website-permissions.png)

Cloud browser 网站权限设置：Always ask / Auto approve / Always allow；不是单次动作审批卡。 · 独立发布日期未标 · UNVERIFIED_DATE

[逐图来源和时间码](assets/work-browser/source.md) · [本地短片](assets/work-browser/clip.mp4)

补采条件：需要接管、停止、回放的专项演示或隔离账号；现有官方浏览器片段已审至转场。

#### 补采：内置浏览器独立演示

官方 dB6pOolO7io 已在浏览器以1080p播放并保存真实截图。此组与上述 Keynote Computer Use 独立。

![Browser 内联标签出现在委托输入框；请求尚在输入。](assets/work-browser/browser-01-delegate.png)

00:15 — Browser 内联标签出现在委托输入框；请求尚在输入。

![内置浏览器显示社区搜索结果；官方源片放大到浏览器局部。](assets/work-browser/browser-02-search.png)

00:20 — 内置浏览器显示社区搜索结果；官方源片放大到浏览器局部。

![Worked for 4m49s 已出现，回答开始输出；该时间为演示内记录，不是本次实测。](assets/work-browser/browser-03-answer-start.png)

00:25 — Worked for 4m49s 已出现，回答开始输出；该时间为演示内记录，不是本次实测。

![浏览器右上有网页批注按钮；页面文章已打开。](assets/work-browser/browser-04-annotation-entry.png)

00:30 — 浏览器右上有网页批注按钮；页面文章已打开。

![Annotating 状态与蓝色选区可见；批注输入请求，尚未显示提交后结果。](assets/work-browser/browser-05-annotation-request.png)

00:35 — Annotating 状态与蓝色选区可见；批注输入请求，尚未显示提交后结果。

![全局 Work 窗口：委托、Working、工具过程、Browser 搜索结果入口和停止控件同时可见；未点击停止。](assets/work-browser/browser-global-task.png)

00:17 — 全局 Work 窗口：委托、Working、工具过程、Browser 搜索结果入口和停止控件同时可见；未点击停止。

![运行中 Loaded a tool / Used the browser；任务仍 Working。源镜头放大，非全局。](assets/work-browser/browser-process-tools.png)

00:23.75 — 运行中 Loaded a tool / Used the browser；任务仍 Working。源镜头放大，非全局。

### Work 的产物落地 · COMPLETE

一句差异点（描述已见交互）：产物可呈现为文件、连接应用内文件和托管 Site。

| 阶段 | 素材实际覆盖 |
|---|---|
| 进入 | 已有上下文，完整新建入口未见 |
| 委托 | 演示文稿请求已见 |
| 过程 | 预览和内联批注已见 |
| 接管 | 用户提交修改已见 |
| 产物 | PPTX、Google Sheets、dashboard、交互 Site 各有图 |
| 退出 | 未见关窗或全部保存回执 |

**图像门槛已达：**四类成品各一图、PPT 修改序列与全局 UI。

![输入按品牌模板生成演示文稿的请求；尚未展示完成。](assets/work-artifacts/01-deck-request.png)

00:55 — 输入按品牌模板生成演示文稿的请求；尚未展示完成。

![PPTX 封面预览；源镜头特写，不是全局 UI。](assets/work-artifacts/02-deck-preview.png)

01:00 — PPTX 封面预览；源镜头特写，不是全局 UI。

![图表位置添加内联批注，要求柱状图；源镜头特写。](assets/work-artifacts/03-inline-edit.png)

01:05 — 图表位置添加内联批注，要求柱状图；源镜头特写。

![批注进入对话，右侧仍为折线图；修改尚未完成。](assets/work-artifacts/04-edit-request-submitted.png)

01:10 — 批注进入对话，右侧仍为折线图；修改尚未完成。

![回复说明更新完成，右侧变为柱状图并修改标题；全局界面。](assets/work-artifacts/05-edited-deck.png)

01:12 — 回复说明更新完成，右侧变为柱状图并修改标题；全局界面。

![官方 Google Sheets 工作区与对话](assets/work-artifacts/spreadsheet-global.png)

官方 Google Sheets 工作区与对话 · 2026-07-09 · PRIORITY

![官方演示的演示文稿产物](assets/work-artifacts/slides-global.png)

官方演示的演示文稿产物 · 2026-07-09 · PRIORITY

![官方 Event operations dashboard](assets/work-artifacts/dashboard-global.png)

官方 Event operations dashboard · 2026-07-09 · PRIORITY

![官方 Revenue forecast planner Site](assets/work-artifacts/site-forecast.png)

官方 Revenue forecast planner Site · 2026-07-09 · PRIORITY

[逐图来源和时间码](assets/work-artifacts/source.md) · [本地短片](assets/work-artifacts/clip.mp4)

下一步：四类成品和编辑序列达到图像门槛；SharePoint 落盘仍未直接证明，保留目的地边界。

落点证据：Google Sheets 原生界面与 docs.google.com 可见；PPTX 文件卡和对话侧预览可见；Sites 有独立成品 UI。官方文件文档要求创建时指定目标，并在 Google Workspace 检查位置与共享设置。本包没有 SharePoint 文件落盘回执，也没有把“生成 PPTX”写成“已在本地 PowerPoint 原生编辑”。当前帮助页对 Work 桌面原生 Office 流程有独立限制，不能与宣传片中的文件预览混同。

### GPT-Live 全双工语音 · PARTIAL

一句差异点（描述已见交互）：语音界面显示视觉回答并允许选择推理档位。

| 阶段 | 素材实际覆盖 |
|---|---|
| 进入 | 入口→加载→球体已见 |
| 委托 | 已审官方图片对话和行程问答，未取得可确认打断的 UI 序列 |
| 过程 | 球体和推理设置已见 |
| 接管 | 打断反馈未取得 |
| 产物 | 天气/体育/地图各一图 |
| 退出 | 关闭按钮已见，退出结果未见 |

**素材缺口：**打断前后 UI 与音频对应；倾听/接话状态区分；后台委派是否可感知；实际结束后的界面

**独立演示分组：**以下01–03来自startup原片0–2秒；04–05来自picker原片3–4秒。两组不能拼成连续5帧全双工流程。image-*是另一个独立的图片对话序列。

![完整手机界面，右下语音入口；官方 UI 动画。](assets/gpt-live/01-voice-entry.png)

00:00 — 完整手机界面，右下语音入口；官方 UI 动画。

![进入语音的加载圈与关闭按钮；不标为正在倾听。](assets/gpt-live/02-voice-loading.png)

00:01 — 进入语音的加载圈与关闭按钮；不标为正在倾听。

![语音球体和关闭按钮；不能仅按球体形状判断谁在说话。](assets/gpt-live/03-orb-visible.png)

00:02 — 语音球体和关闭按钮；不能仅按球体形状判断谁在说话。

![语音设置面板显示 Language / Intelligence，当前 Medium。](assets/gpt-live/04-reasoning-picker.png)

00:03 — 语音设置面板显示 Language / Intelligence，当前 Medium。

![Intelligence 显示 Instant / Medium / High；不是后台工作进度。](assets/gpt-live/05-reasoning-options.png)

00:04 — Intelligence 显示 Instant / Medium / High；不是后台工作进度。

![语音天气视觉卡片](assets/gpt-live/weather-global.png)

语音天气视觉卡片 · 2026-07-08 · PRIORITY

![语音体育视觉卡片](assets/gpt-live/sports-global.png)

语音体育视觉卡片 · 2026-07-08 · PRIORITY

![语音地图视觉卡片](assets/gpt-live/maps-global.png)

语音地图视觉卡片 · 2026-07-08 · PRIORITY

[逐图来源和时间码](assets/gpt-live/source.md) · [本地短片](assets/gpt-live/clip.mp4)

补采条件：需同时清晰记录音轨与手机 UI 的打断专项演示；本轮已审三段官方对话原片、入口和菜单动画。

#### 补采：图片对话与行程问答

图片对话按同一原片顺序排列，证明语音中两次选图及返回。打断与后台状态仍未完整核实。Whisper转写仅用于定位，不能证明重叠发声。

![独立图片对话演示：完整手机聊天界面，右下语音入口。](assets/gpt-live/image-01-entry.png)

00:00 — 独立图片对话演示：完整手机聊天界面，右下语音入口。

![对话中打开照片选择界面，选取服装照片；图像加入语音上下文。](assets/gpt-live/image-02-photo-picker.png)

00:12 — 对话中打开照片选择界面，选取服装照片；图像加入语音上下文。

![选图后回到球体语音界面；按音轨转写位置为模型开始评价服装，不根据球体形状定义说话状态。](assets/gpt-live/image-03-voice-return.png)

00:18 — 选图后回到球体语音界面；按音轨转写位置为模型开始评价服装，不根据球体形状定义说话状态。

![同一演示再次打开照片界面选择另一套服装；不表示用户打断。](assets/gpt-live/image-04-second-photo.png)

00:35 — 同一演示再次打开照片界面选择另一套服装；不表示用户打断。

![第二张照片后回到语音球体；手机无明确后台任务卡或倾听/接话文字。](assets/gpt-live/image-05-voice-again.png)

00:42 — 第二张照片后回到语音球体；手机无明确后台任务卡或倾听/接话文字。

![独立行程问答演示的手机全局近景：仍显示球体和底部控件，未见后台任务卡。](assets/gpt-live/intelligence-orb-global.png)

01:43 — 独立行程问答演示的手机全局近景：仍显示球体和底部控件，未见后台任务卡。

[图片对话29.82秒原声片段](assets/gpt-live/image-clip.mp4)

### Atlas 浏览器 agent 模式 · PARTIAL

一句差异点（描述已见交互）：历史 Atlas 底部条集中显示任务、接管和停止。

| 阶段 | 素材实际覆盖 |
|---|---|
| 进入 | 浏览器确认已见（历史） |
| 委托 | 购物委托已见（历史） |
| 过程 | 光标、状态条已见（历史） |
| 接管 | Take control / Stop 可见，未见点击 |
| 产物 | 购物车和结账询问已见（历史） |
| 退出 | 停止后界面未见 |

**素材缺口：**本季独立 Atlas 交互素材；Take control 点击前后；停止/退出结果

![Atlas 使用浏览器确认，Continue / No thanks；不是 Work 应用审批。](assets/atlas/01-background-browser-permission.png)

01:10 — Atlas 使用浏览器确认，Continue / No thanks；不是 Work 应用审批。

![Atlas 操作 Instacart，底部黑色状态条、Take control 与 Stop 可见。](assets/atlas/02-background-agent-running.png)

01:13 — Atlas 操作 Instacart，底部黑色状态条、Take control 与 Stop 可见。

![Atlas 光标在商店页行动；用户接管未展示。](assets/atlas/03-background-agent-click.png)

01:15 — Atlas 光标在商店页行动；用户接管未展示。

![Atlas 点击 Add，提示 Adding sunscreen to cart；局部镜头。](assets/atlas/04-background-add-to-cart.png)

01:21 — Atlas 点击 Add，提示 Adding sunscreen to cart；局部镜头。

![Atlas 回复购物车准备好并询问结账；未展示付款。](assets/atlas/05-background-checkout-question.png)

01:23 — Atlas 回复购物车准备好并询问结账；未展示付款。

![历史背景：Atlas Instacart agent 官方 UI，非本季新增](assets/atlas/background-agent-global.png)

历史背景：Atlas Instacart agent 官方 UI，非本季新增 · 2025-10-21 · BACKGROUND

[逐图来源和时间码](assets/atlas/source.md) · [本地短片](assets/atlas/clip.mp4)

补采条件：历史专项接管演示。现有宣传片有控件，旧直播字幕定位的是交给 agent 的 Continue；均未得到用户收回后的状态。本季独立 Atlas 不计完整。

## §4 新硬件

**悬念：未核实已发布的消费级设备，也未取得设备交互图。**不能把合作成立写成硬件已经上市。

已知可验证信息：2025-05-21 官方公开合作信；2025-07-09 更新说明 io 团队已并入 OpenAI，Jony Ive / LoveFrom 保持独立并承担设计职责。官方给出的出发点是 AI 能力发展后，使用体验仍受传统产品和界面影响。这是合作动机，尚不能证明具体设备解决了哪项软件短板。[官方合作信](https://openai.com/sam-and-jony/)

官方合作照片仅1000×750，低于素材门槛，已移至原始缓存并排除正式计数。[出处与边界](assets/hardware/source.md)

据 2026-02 媒体转述，首款设备推迟至 2027 年且不再叫 io。**未证实**；该报道在本轮时间窗前，仅保留为待核背景，不扩写规格。[报道](https://www.macrumors.com/2026/02/10/openais-jony-ive-designed-device-delayed-to-2027/)

需要盯的信号：官方产品名称与上市声明、可辨设备实物、唤醒/确认/取消的真实演示、与手机的关系。新交互形式：留空，待官方证据。

## §5 拆分逻辑

以下仅放可供人工判断的事实；不替公司推导战略归因。

| 归因标题 | 已取得事实材料 | 尚无证据的部分 |
|---|---|---|
| 工具装载 | Work 插件目录与 @ 内联应用；Computer 引用；浏览器权限文档 | 这些边界为何这样设计 |
| 产物形态 | Google Sheets、PPTX、dashboard、Site 成品 | 产品拆分是否由形态驱动 |
| 爆炸半径 | 网站访问、应用批准、任务模式存在不同层级 | 各层是否覆盖同一风险、拒绝后如何收敛 |
| 反馈回路 | 过程文字、画中画、图表批注、Voice 视觉卡片 | 完整接管/退出效果和效率 |
| 买单人 | 官方区分个人套餐与受管理员约束的工作区 | 实际采购者、决策权和支付动机 |

## §6 三个必答问题

1. **它把能力拆成了几块，边界画在哪？** 本包记录 5 个命名产品/模式，其中 Atlas 已弃用。文件/权限/落点见 §2；不同表面权限不能仅由名称等同。五个名称不能用于推断底层能力彼此独立。
2. **它的委托面在往哪走——更显式还是更隐式？** 已见显式文字、@ 应用标签、上下文附件、产物局部批注和语音入口。本轮没有同任务、跨版本纵向实测，方向判断留给人填。
3. **它的硬件在补软件的哪块短板？没硬件的怎么绕过去？** 官方合作信提出重新思考传统界面的动机；具体设备载体与交互尚未核实。本轮可验证软件载体为手机、桌面和网页，不能将它们写成官方“不做硬件”的替代战略。

## §7 素材与出处表

以下逐文件表与 [SOURCES.md](SOURCES.md) 同步；同源重复参考不增加独立流程帧数。

抓取：2026-09-09。BACKGROUND 不计本季；UNVERIFIED_DATE 不能按抓取日当发布日。原片及失败日志保留在 `_work/`。

| 文件 | 特性 | 页面 | 原媒体 | 时间码 | 发布日 / 时间窗 | 抓取日 | 官方性 | 实际状态与边界 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| [assets/work-browser/browser-01-delegate.png](assets/work-browser/browser-01-delegate.png) | work-browser | [页面](https://www.youtube.com/watch?v=dB6pOolO7io) | [原媒体](https://www.youtube.com/watch?v=dB6pOolO7io) | 00:15 | 2026-07-16 / PRIORITY | 2026-09-09 | 官方 | Browser 内联标签出现在委托输入框；请求尚在输入。 Chrome 播放原生 1920×1080 流，CUA 读取 currentTime；OS Retina 录屏截图裁去外部浏览器控件后缩小至 1920 宽，无补绘。源片自带演示者小窗和局部镜头；未证明接管或停止。 |
| [assets/work-browser/browser-02-search.png](assets/work-browser/browser-02-search.png) | work-browser | [页面](https://www.youtube.com/watch?v=dB6pOolO7io) | [原媒体](https://www.youtube.com/watch?v=dB6pOolO7io) | 00:20 | 2026-07-16 / PRIORITY | 2026-09-09 | 官方 | 内置浏览器显示社区搜索结果；官方源片放大到浏览器局部。 Chrome 播放原生 1920×1080 流，CUA 读取 currentTime；OS Retina 录屏截图裁去外部浏览器控件后缩小至 1920 宽，无补绘。源片自带演示者小窗和局部镜头；未证明接管或停止。 |
| [assets/work-browser/browser-03-answer-start.png](assets/work-browser/browser-03-answer-start.png) | work-browser | [页面](https://www.youtube.com/watch?v=dB6pOolO7io) | [原媒体](https://www.youtube.com/watch?v=dB6pOolO7io) | 00:25 | 2026-07-16 / PRIORITY | 2026-09-09 | 官方 | Worked for 4m49s 已出现，回答开始输出；该时间为演示内记录，不是本次实测。 Chrome 播放原生 1920×1080 流，CUA 读取 currentTime；OS Retina 录屏截图裁去外部浏览器控件后缩小至 1920 宽，无补绘。源片自带演示者小窗和局部镜头；未证明接管或停止。 |
| [assets/work-browser/browser-04-annotation-entry.png](assets/work-browser/browser-04-annotation-entry.png) | work-browser | [页面](https://www.youtube.com/watch?v=dB6pOolO7io) | [原媒体](https://www.youtube.com/watch?v=dB6pOolO7io) | 00:30 | 2026-07-16 / PRIORITY | 2026-09-09 | 官方 | 浏览器右上有网页批注按钮；页面文章已打开。 Chrome 播放原生 1920×1080 流，CUA 读取 currentTime；OS Retina 录屏截图裁去外部浏览器控件后缩小至 1920 宽，无补绘。源片自带演示者小窗和局部镜头；未证明接管或停止。 |
| [assets/work-browser/browser-05-annotation-request.png](assets/work-browser/browser-05-annotation-request.png) | work-browser | [页面](https://www.youtube.com/watch?v=dB6pOolO7io) | [原媒体](https://www.youtube.com/watch?v=dB6pOolO7io) | 00:35 | 2026-07-16 / PRIORITY | 2026-09-09 | 官方 | Annotating 状态与蓝色选区可见；批注输入请求，尚未显示提交后结果。 Chrome 播放原生 1920×1080 流，CUA 读取 currentTime；OS Retina 录屏截图裁去外部浏览器控件后缩小至 1920 宽，无补绘。源片自带演示者小窗和局部镜头；未证明接管或停止。 |
| [assets/work-browser/browser-global-task.png](assets/work-browser/browser-global-task.png) | work-browser | [页面](https://www.youtube.com/watch?v=dB6pOolO7io) | [原媒体](https://www.youtube.com/watch?v=dB6pOolO7io) | 00:17 | 2026-07-16 / PRIORITY | 2026-09-09 | 官方 | 全局 Work 窗口：委托、Working、工具过程、Browser 搜索结果入口和停止控件同时可见；未点击停止。 Chrome 播放原生 1920×1080 流，CUA 读取 currentTime；OS Retina 录屏截图裁去外部浏览器控件后缩小至 1920 宽，无补绘。源片自带演示者小窗和局部镜头；未证明接管或停止。 |
| [assets/work-browser/browser-process-tools.png](assets/work-browser/browser-process-tools.png) | work-browser | [页面](https://www.youtube.com/watch?v=dB6pOolO7io) | [原媒体](https://www.youtube.com/watch?v=dB6pOolO7io) | 00:23.75 | 2026-07-16 / PRIORITY | 2026-09-09 | 官方 | 运行中 Loaded a tool / Used the browser；任务仍 Working。源镜头放大，非全局。 Chrome 播放原生 1920×1080 流，CUA 读取 currentTime；OS Retina 录屏截图裁去外部浏览器控件后缩小至 1920 宽，无补绘。源片自带演示者小窗和局部镜头；未证明接管或停止。 |
| [assets/gpt-live/image-01-entry.png](assets/gpt-live/image-01-entry.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1207915527?h=fb4a16a947) | 00:00 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 独立图片对话演示：完整手机聊天界面，右下语音入口。 官方发布页所嵌入的真实手机演示，原视频1920×1080；页日期不保证独立视频日期。与startup/picker分组；没有将选图或球体变化视为打断反馈。 |
| [assets/gpt-live/image-02-photo-picker.png](assets/gpt-live/image-02-photo-picker.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1207915527?h=fb4a16a947) | 00:12 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 对话中打开照片选择界面，选取服装照片；图像加入语音上下文。 官方发布页所嵌入的真实手机演示，原视频1920×1080；页日期不保证独立视频日期。与startup/picker分组；没有将选图或球体变化视为打断反馈。 |
| [assets/gpt-live/image-03-voice-return.png](assets/gpt-live/image-03-voice-return.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1207915527?h=fb4a16a947) | 00:18 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 选图后回到球体语音界面；按音轨转写位置为模型开始评价服装，不根据球体形状定义说话状态。 官方发布页所嵌入的真实手机演示，原视频1920×1080；页日期不保证独立视频日期。与startup/picker分组；没有将选图或球体变化视为打断反馈。 |
| [assets/gpt-live/image-04-second-photo.png](assets/gpt-live/image-04-second-photo.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1207915527?h=fb4a16a947) | 00:35 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 同一演示再次打开照片界面选择另一套服装；不表示用户打断。 官方发布页所嵌入的真实手机演示，原视频1920×1080；页日期不保证独立视频日期。与startup/picker分组；没有将选图或球体变化视为打断反馈。 |
| [assets/gpt-live/image-05-voice-again.png](assets/gpt-live/image-05-voice-again.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1207915527?h=fb4a16a947) | 00:42 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 第二张照片后回到语音球体；手机无明确后台任务卡或倾听/接话文字。 官方发布页所嵌入的真实手机演示，原视频1920×1080；页日期不保证独立视频日期。与startup/picker分组；没有将选图或球体变化视为打断反馈。 |
| [assets/gpt-live/image-clip.mp4](assets/gpt-live/image-clip.mp4) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1207915527?h=fb4a16a947) | 00:10–00:39.80 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 图片对话原片10–39.8秒，保留原声；包含第一次选图、回答和第二次选图。 官方发布页所嵌入的真实手机演示，原视频1920×1080；页日期不保证独立视频日期。与startup/picker分组；没有将选图或球体变化视为打断反馈。 |
| [assets/gpt-live/intelligence-orb-global.png](assets/gpt-live/intelligence-orb-global.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1209991962?h=932d97ada3) | 01:43 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 独立行程问答演示的手机全局近景：仍显示球体和底部控件，未见后台任务卡。 官方GPT-Live页嵌入，页面含后续更新而独立视频日期未核实；53–100秒音轨转写出现行程核查与餐饮问答交替，不能仅用此单图证明全双工打断。 |
| [assets/work-approval/thirdparty-windows-01-running.png](assets/work-approval/thirdparty-windows-01-running.png) | work-approval | [页面](https://note.com/calm_gerbil315/n/nfc4ed8ccd363) | [原媒体](https://assets.st-note.com/img/1786762999-3YGtQ2iTC9quPLUJoHwayIh0.png) | 静态 | 2026-08-15 / PRIORITY | 2026-09-09 | 第三方第一手上手 | Windows Work 调研委托开始运行，尚未出现审批卡。 作者原有灰色遮挡保留。 文章原图去除1200缩图参数取得原尺寸；未放大、补绘或本次实测。 |
| [assets/work-approval/thirdparty-windows-02-access-approval.png](assets/work-approval/thirdparty-windows-02-access-approval.png) | work-approval | [页面](https://note.com/calm_gerbil315/n/nfc4ed8ccd363) | [原媒体](https://assets.st-note.com/img/1786763112-rFakw61IfGiWxC3NR097opBL.png) | 静态 | 2026-08-15 / PRIORITY | 2026-09-09 | 第三方第一手上手 | 任务停在承认待ち；Browser 卡列出 help.openai.com，按钮含拒否、一度だけ許可及所有网站授权。 作者原有灰色遮挡和红框保留；没有点击拒绝后的图。 文章原图去除1200缩图参数取得原尺寸；未放大、补绘或本次实测。 |
| [assets/work-approval/thirdparty-note-broad-approval-confirm.png](assets/work-approval/thirdparty-note-broad-approval-confirm.png) | work-approval | [页面](https://note.com/kyu_hontoko/n/n53517ef7e02d) | [原媒体](https://assets.st-note.com/img/1788075841-BReUfQmpl85a0Y1d2CsuZVtN.png) | 静态 | 2026-08-31 / PRIORITY | 2026-09-09 | 第三方第一手上手 | 另一案例：note.com 访问卡在下方，前景为允许任意网站且无需再次确认的二次弹窗，含取消和所有网站允许。 图片来自文章免费可见区。正文称选择单次，但图中实际为扩大权限确认，以图为准；其范围不同于单一动作Always allow。 文章原图去除1200缩图参数取得原尺寸；未放大、补绘或本次实测。 |
| [assets/work-mention/global-plugin-directory.png](assets/work-mention/global-plugin-directory.png) | work-mention | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/3340Q2XYfbsirvvYoKTrMY/12887973ea8709d9dd2a25c0d11d0abe/OAI_ChatGPTWork_PressBlog_PluginDirectory_16x9_260708.png) | 静态 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 插件目录，不是 @ 弹出菜单 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/work-mention/desktop-mode-picker.png](assets/work-mention/desktop-mode-picker.png) | work-mention | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/2T3eFCXl7i3DxCl3E7jXiC/95e52f4f44f85827a8844cc5051cd4e1/OAI_ChatGPTWork_PressBlog_DesktopPicker-Work_16x9_260708.png) | 静态 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 桌面 Work 模式菜单 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/work-artifacts/slides-global.png](assets/work-artifacts/slides-global.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/3MIh1eHZlPjuw1fWoMA76X/cd0c40136803d49299d61eb48944314b/OAI_ChatGPTWork_PressBlog_WebArtifact_16x9_260708.png) | 静态 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 官方演示的演示文稿产物 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/work-artifacts/spreadsheet-global.png](assets/work-artifacts/spreadsheet-global.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/2q1hcq6tWZ7FawSYE5CP9J/c71384d63f82b6aec870dc768f7e3a46/OAI_ChatGPTWork_PressBlog_DesktopArtifact_16x9_260708.png) | 静态 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 官方 Google Sheets 工作区与对话 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/work-artifacts/site-forecast.png](assets/work-artifacts/site-forecast.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/5G0zHEnIZRLg0EWpZV602t/47c3851dd1f1cfbdf42d5f630fd36241/blossom-bank-forecasting-light-4k.png) | 静态 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 官方 Revenue forecast planner Site 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/gpt-live/weather-global.png](assets/gpt-live/weather-global.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/38TRAE6B8AS3hNkoQuKSOl/729b7c415ed4c1b62027449799cead86/gpt-live-visual-answer-weather.png) | 静态 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 语音天气视觉卡片 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/gpt-live/sports-global.png](assets/gpt-live/sports-global.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/7IWfPZwH8SaJVikq4PScQP/f327d0d73d35b3989b8d504d5e9fa782/gpt-live-visual-answer-sports.png) | 静态 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 语音体育视觉卡片 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/gpt-live/maps-global.png](assets/gpt-live/maps-global.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/GLkTfEhJSFJZ77FHnN1f6/b1ab29d652268636a226246f5b1766cc/gpt-live-visual-answer-maps.png) | 静态 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 语音地图视觉卡片 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/work-artifacts/dashboard-global.png](assets/work-artifacts/dashboard-global.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/3xXbAmTubtBQ7u2OJThryt/58a900197cfd7430c1040f56c4c86a5d/blossom-widgets-enterprise-summit-photo-floorplan-alt-4k.png) | 静态 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 官方 Event operations dashboard 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/work-artifacts/web-app-global.png](assets/work-artifacts/web-app-global.png) | work-artifacts | [页面](https://openai.com/chatgpt-work/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/57WzZDA3mSsFa1BPAyyUSH/0f6c891bfd20cee2240869e69a07c4b8/Card_5_-_opt_8.png) | 静态 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 官方 Site 构建与内置浏览器预览；页面未列原图发布日期 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/atlas/background-agent-global.png](assets/atlas/background-agent-global.png) | atlas | [页面](https://openai.com/index/introducing-chatgpt-atlas/) | [原媒体](https://images.ctfassets.net/kftzwdyauwt9/7vBVya3XA6w2Sbq74ENNIi/b65385435d060532d89225d937942e77/Agent__5_.png) | 静态 | 2025-10-21 / BACKGROUND | 2026-09-09 | 官方 | 历史背景：Atlas Instacart agent 官方 UI，非本季新增 官方素材，未在用户账号复现；按钮出现不证明动作已执行。 |
| [assets/work-mention/01-at-candidates.png](assets/work-mention/01-at-candidates.png) | work-mention | [页面](https://learn.chatgpt.com/training/walkthroughs/plugins-and-skills) | [原媒体](https://cdn.openai.com/devhub/videos-learn/work-101/plugins-and-skills.mp4) | 01:06 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 输入 @cal 后出现候选列表；Google Calendar 与文档/任务同列；源镜头局部放大。 官方教学；发布日未标；有剪辑和局部放大。 |
| [assets/work-mention/02-inline-app.png](assets/work-mention/02-inline-app.png) | work-mention | [页面](https://learn.chatgpt.com/training/walkthroughs/plugins-and-skills) | [原媒体](https://cdn.openai.com/devhub/videos-learn/work-101/plugins-and-skills.mp4) | 01:07 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 选中 Google Calendar 后出现带图标的内联标签；源镜头局部放大。 官方教学；发布日未标；有剪辑和局部放大。 |
| [assets/work-mention/03-delegate.png](assets/work-mention/03-delegate.png) | work-mention | [页面](https://learn.chatgpt.com/training/walkthroughs/plugins-and-skills) | [原媒体](https://cdn.openai.com/devhub/videos-learn/work-101/plugins-and-skills.mp4) | 01:08 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 完整请求包含一个 Google Calendar 标签；未见多个应用。 官方教学；发布日未标；有剪辑和局部放大。 |
| [assets/work-mention/04-progress.png](assets/work-mention/04-progress.png) | work-mention | [页面](https://learn.chatgpt.com/training/walkthroughs/plugins-and-skills) | [原媒体](https://cdn.openai.com/devhub/videos-learn/work-101/plugins-and-skills.mp4) | 01:09 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 任务已开始，过程界面可见。 官方教学；发布日未标；有剪辑和局部放大。 |
| [assets/work-mention/05-calendar-slots-still-working.png](assets/work-mention/05-calendar-slots-still-working.png) | work-mention | [页面](https://learn.chatgpt.com/training/walkthroughs/plugins-and-skills) | [原媒体](https://cdn.openai.com/devhub/videos-learn/work-101/plugins-and-skills.mp4) | 01:13 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 已列出候选日历时段，顶部仍 Working for 15s；不是完成或退出。 官方教学；发布日未标；有剪辑和局部放大。 |
| [assets/work-mention/global-video-ui.png](assets/work-mention/global-video-ui.png) | work-mention | [页面](https://learn.chatgpt.com/training/walkthroughs/plugins-and-skills) | [原媒体](https://cdn.openai.com/devhub/videos-learn/work-101/plugins-and-skills.mp4) | 01:05 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 同源全局参考；与序列同时间码重复，不计额外流程帧。 官方教学；发布日未标；有剪辑和局部放大。 |
| [assets/work-mention/clip.mp4](assets/work-mention/clip.mp4) | work-mention | [页面](https://learn.chatgpt.com/training/walkthroughs/plugins-and-skills) | [原媒体](https://cdn.openai.com/devhub/videos-learn/work-101/plugins-and-skills.mp4) | 01:05–01:15 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | 原视频片段；含剪辑，状态以 PNG 说明为准。 官方教学；发布日未标；有剪辑和局部放大。 |
| [assets/work-browser/01-computer-delegate.png](assets/work-browser/01-computer-delegate.png) | work-browser | [页面](https://www.youtube.com/watch?v=IYYTI73J7Rg) | [原媒体](https://www.youtube.com/watch?v=IYYTI73J7Rg) | 00:15 | 2026-07-10 / PRIORITY | 2026-09-09 | 官方 | Computer 标签与 Notes 附件；委托修改 Keynote；Approve for me 只是模式标签。 已核对 OpenAI 频道和上传日期；桌面 Computer Use，非内置浏览器专项流程。 |
| [assets/work-browser/02-computer-progress.png](assets/work-browser/02-computer-progress.png) | work-browser | [页面](https://www.youtube.com/watch?v=IYYTI73J7Rg) | [原媒体](https://www.youtube.com/watch?v=IYYTI73J7Rg) | 00:18 | 2026-07-10 / PRIORITY | 2026-09-09 | 官方 | Computer Use 运行，过程文字与停止控件可见；未点击停止。 已核对 OpenAI 频道和上传日期；桌面 Computer Use，非内置浏览器专项流程。 |
| [assets/work-browser/03-pip-preview.png](assets/work-browser/03-pip-preview.png) | work-browser | [页面](https://www.youtube.com/watch?v=IYYTI73J7Rg) | [原媒体](https://www.youtube.com/watch?v=IYYTI73J7Rg) | 00:24 | 2026-07-10 / PRIORITY | 2026-09-09 | 官方 | Keynote 画中画预览；不是浏览器页面。 已核对 OpenAI 频道和上传日期；桌面 Computer Use，非内置浏览器专项流程。 |
| [assets/work-browser/04-pip-keynote.png](assets/work-browser/04-pip-keynote.png) | work-browser | [页面](https://www.youtube.com/watch?v=IYYTI73J7Rg) | [原媒体](https://www.youtube.com/watch?v=IYYTI73J7Rg) | 00:27 | 2026-07-10 / PRIORITY | 2026-09-09 | 官方 | Keynote 画中画继续显示文稿；不是浏览器页面。 已核对 OpenAI 频道和上传日期；桌面 Computer Use，非内置浏览器专项流程。 |
| [assets/work-browser/05-keynote-edit.png](assets/work-browser/05-keynote-edit.png) | work-browser | [页面](https://www.youtube.com/watch?v=IYYTI73J7Rg) | [原媒体](https://www.youtube.com/watch?v=IYYTI73J7Rg) | 00:30 | 2026-07-10 / PRIORITY | 2026-09-09 | 官方 | 画中画内编辑 Keynote；没有接管动作。 已核对 OpenAI 频道和上传日期；桌面 Computer Use，非内置浏览器专项流程。 |
| [assets/work-browser/global-video-ui.png](assets/work-browser/global-video-ui.png) | work-browser | [页面](https://www.youtube.com/watch?v=IYYTI73J7Rg) | [原媒体](https://www.youtube.com/watch?v=IYYTI73J7Rg) | 00:18 | 2026-07-10 / PRIORITY | 2026-09-09 | 官方 | 同源全局参考；与序列同时间码重复，不计额外流程帧。 已核对 OpenAI 频道和上传日期；桌面 Computer Use，非内置浏览器专项流程。 |
| [assets/work-browser/clip.mp4](assets/work-browser/clip.mp4) | work-browser | [页面](https://www.youtube.com/watch?v=IYYTI73J7Rg) | [原媒体](https://www.youtube.com/watch?v=IYYTI73J7Rg) | 00:12–00:32 | 2026-07-10 / PRIORITY | 2026-09-09 | 官方 | 原视频片段；含剪辑，状态以 PNG 说明为准。 已核对 OpenAI 频道和上传日期；桌面 Computer Use，非内置浏览器专项流程。 |
| [assets/work-artifacts/01-deck-request.png](assets/work-artifacts/01-deck-request.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://player.vimeo.com/video/1208302106?h=9acac9bbfd) | 00:55 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 输入按品牌模板生成演示文稿的请求；尚未展示完成。 官方发布页宣传演示；日期取自页面；剪辑压缩过程，不能测操作耗时。 |
| [assets/work-artifacts/02-deck-preview.png](assets/work-artifacts/02-deck-preview.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://player.vimeo.com/video/1208302106?h=9acac9bbfd) | 01:00 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | PPTX 封面预览；源镜头特写，不是全局 UI。 官方发布页宣传演示；日期取自页面；剪辑压缩过程，不能测操作耗时。 |
| [assets/work-artifacts/03-inline-edit.png](assets/work-artifacts/03-inline-edit.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://player.vimeo.com/video/1208302106?h=9acac9bbfd) | 01:05 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 图表位置添加内联批注，要求柱状图；源镜头特写。 官方发布页宣传演示；日期取自页面；剪辑压缩过程，不能测操作耗时。 |
| [assets/work-artifacts/04-edit-request-submitted.png](assets/work-artifacts/04-edit-request-submitted.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://player.vimeo.com/video/1208302106?h=9acac9bbfd) | 01:10 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 批注进入对话，右侧仍为折线图；修改尚未完成。 官方发布页宣传演示；日期取自页面；剪辑压缩过程，不能测操作耗时。 |
| [assets/work-artifacts/clip.mp4](assets/work-artifacts/clip.mp4) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://player.vimeo.com/video/1208302106?h=9acac9bbfd) | 00:52–01:14 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 原视频片段；含剪辑，状态以 PNG 说明为准。 官方发布页宣传演示；日期取自页面；剪辑压缩过程，不能测操作耗时。 |
| [assets/atlas/01-background-browser-permission.png](assets/atlas/01-background-browser-permission.png) | atlas | [页面](https://openai.com/index/introducing-chatgpt-atlas/) | [原媒体](https://player.vimeo.com/video/1129227761?h=94755e8733) | 01:10 | 2025-10-21 / BACKGROUND | 2026-09-09 | 官方 | Atlas 使用浏览器确认，Continue / No thanks；不是 Work 应用审批。 BACKGROUND 历史宣传片；已弃用产品，非本季新增或当前实测。 |
| [assets/atlas/02-background-agent-running.png](assets/atlas/02-background-agent-running.png) | atlas | [页面](https://openai.com/index/introducing-chatgpt-atlas/) | [原媒体](https://player.vimeo.com/video/1129227761?h=94755e8733) | 01:13 | 2025-10-21 / BACKGROUND | 2026-09-09 | 官方 | Atlas 操作 Instacart，底部黑色状态条、Take control 与 Stop 可见。 BACKGROUND 历史宣传片；已弃用产品，非本季新增或当前实测。 |
| [assets/atlas/03-background-agent-click.png](assets/atlas/03-background-agent-click.png) | atlas | [页面](https://openai.com/index/introducing-chatgpt-atlas/) | [原媒体](https://player.vimeo.com/video/1129227761?h=94755e8733) | 01:15 | 2025-10-21 / BACKGROUND | 2026-09-09 | 官方 | Atlas 光标在商店页行动；用户接管未展示。 BACKGROUND 历史宣传片；已弃用产品，非本季新增或当前实测。 |
| [assets/atlas/04-background-add-to-cart.png](assets/atlas/04-background-add-to-cart.png) | atlas | [页面](https://openai.com/index/introducing-chatgpt-atlas/) | [原媒体](https://player.vimeo.com/video/1129227761?h=94755e8733) | 01:21 | 2025-10-21 / BACKGROUND | 2026-09-09 | 官方 | Atlas 点击 Add，提示 Adding sunscreen to cart；局部镜头。 BACKGROUND 历史宣传片；已弃用产品，非本季新增或当前实测。 |
| [assets/atlas/global-video-ui.png](assets/atlas/global-video-ui.png) | atlas | [页面](https://openai.com/index/introducing-chatgpt-atlas/) | [原媒体](https://player.vimeo.com/video/1129227761?h=94755e8733) | 01:13 | 2025-10-21 / BACKGROUND | 2026-09-09 | 官方 | 同源全局参考；与序列同时间码重复，不计额外流程帧。 BACKGROUND 历史宣传片；已弃用产品，非本季新增或当前实测。 |
| [assets/atlas/clip.mp4](assets/atlas/clip.mp4) | atlas | [页面](https://openai.com/index/introducing-chatgpt-atlas/) | [原媒体](https://player.vimeo.com/video/1129227761?h=94755e8733) | 01:05–01:25 | 2025-10-21 / BACKGROUND | 2026-09-09 | 官方 | 原视频片段；含剪辑，状态以 PNG 说明为准。 BACKGROUND 历史宣传片；已弃用产品，非本季新增或当前实测。 |
| [assets/gpt-live/01-voice-entry.png](assets/gpt-live/01-voice-entry.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1208103428?h=3a310e668a) | 00:00 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 完整手机界面，右下语音入口；官方 UI 动画。 官方发布页 UI 动画；日期取自页面，非独立视频日期；不证明打断效果。 |
| [assets/gpt-live/02-voice-loading.png](assets/gpt-live/02-voice-loading.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1208103428?h=3a310e668a) | 00:01 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 进入语音的加载圈与关闭按钮；不标为正在倾听。 官方发布页 UI 动画；日期取自页面，非独立视频日期；不证明打断效果。 |
| [assets/gpt-live/03-orb-visible.png](assets/gpt-live/03-orb-visible.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1208103428?h=3a310e668a) | 00:02 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 语音球体和关闭按钮；不能仅按球体形状判断谁在说话。 官方发布页 UI 动画；日期取自页面，非独立视频日期；不证明打断效果。 |
| [assets/gpt-live/04-reasoning-picker.png](assets/gpt-live/04-reasoning-picker.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1208104269?h=d3a5cfc799) | 00:03 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 语音设置面板显示 Language / Intelligence，当前 Medium。 官方发布页 UI 动画；日期取自页面；推理设置不代表后台委派状态。 |
| [assets/gpt-live/clip.mp4](assets/gpt-live/clip.mp4) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1208103428?h=3a310e668a) | 00:00–00:08 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | 原视频片段；含剪辑，状态以 PNG 说明为准。 官方发布页 UI 动画；日期取自页面，非独立视频日期；不证明打断效果。 |
| [assets/work-artifacts/05-edited-deck.png](assets/work-artifacts/05-edited-deck.png) | work-artifacts | [页面](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) | [原媒体](https://player.vimeo.com/video/1208302106?h=9acac9bbfd) | 01:12 | 2026-07-09 / PRIORITY | 2026-09-09 | 官方 | 回复说明更新完成，右侧变为柱状图并修改标题；全局界面。 官方发布页宣传演示；日期取自页面；剪辑压缩过程，不能测操作耗时。 |
| [assets/atlas/05-background-checkout-question.png](assets/atlas/05-background-checkout-question.png) | atlas | [页面](https://openai.com/index/introducing-chatgpt-atlas/) | [原媒体](https://player.vimeo.com/video/1129227761?h=94755e8733) | 01:23 | 2025-10-21 / BACKGROUND | 2026-09-09 | 官方 | Atlas 回复购物车准备好并询问结账；未展示付款。 BACKGROUND 历史宣传片；已弃用产品，非本季新增或当前实测。 |
| [assets/gpt-live/05-reasoning-options.png](assets/gpt-live/05-reasoning-options.png) | gpt-live | [页面](https://openai.com/index/introducing-gpt-live/) | [原媒体](https://player.vimeo.com/video/1208104269?h=d3a5cfc799) | 00:04 | 2026-07-08 / PRIORITY | 2026-09-09 | 官方 | Intelligence 显示 Instant / Medium / High；不是后台工作进度。 官方发布页 UI 动画；日期取自页面；推理设置不代表后台委派状态。 |
| [assets/work-browser/official-sign-in.png](assets/work-browser/official-sign-in.png) | work-browser | [页面](https://learn.chatgpt.com/docs/browser?surface=app) | [原媒体](https://developers.openai.com/images/codex/cloud-browser-auth/sign-in.webp) | 静态 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | Cloud browser 移动端登录交接，有手动登录和 Skip；不是桌面内置浏览器接管。 原图发布日未标；WebP 无缩放转 PNG。 |
| [assets/work-browser/official-website-permissions.png](assets/work-browser/official-website-permissions.png) | work-browser | [页面](https://learn.chatgpt.com/docs/browser?surface=app) | [原媒体](https://developers.openai.com/images/codex/cloud-browser-auth/website-permissions.webp) | 静态 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | Cloud browser 网站权限设置：Always ask / Auto approve / Always allow；不是单次动作审批卡。 原图发布日未标；WebP 无缩放转 PNG。 |
| [assets/work-browser/official-browser-data.png](assets/work-browser/official-browser-data.png) | work-browser | [页面](https://learn.chatgpt.com/docs/browser?surface=app) | [原媒体](https://developers.openai.com/images/codex/cloud-browser-auth/browser-data.webp) | 静态 | 未标 / UNVERIFIED_DATE | 2026-09-09 | 官方 | Cloud browser 网站权限和 Cookies 设置全局；不是代理运行或退出。 原图发布日未标；WebP 无缩放转 PNG。 |

## 待人填：观点 / 对我们的启发
