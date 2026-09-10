# 最终验收｜2026-09-10

## 验收口径

七家独立 goal 的本轮公开素材调查与交付已完成。**素材并非全部达标：35 项中 3 COMPLETE、31 PARTIAL、1 MISSING。** 任务书允许实际尝试替代来源后保留素材缺口；本次按这一约定逐项处置，没有把检查脚本通过作为研究完成依据。

COMPLETE 仅对应指定素材范围。例如 Work 产物四类图已取得、社区三条 issue 已取得、腕带脱离眼镜的官方研究/PoC 图与连续片已取得；它不表示所有产品状态或消费可用性得到验证。未找到的审批、接管、退出和未发布设备仍明确留空。

证据采用顺序：官方视频/动画及 UI、可用产品自测、可靠第三方上手。2026-03-09 前只作 BACKGROUND；未知发布日期不以抓取日替代。原始任务书决定 35 项范围，原始 PPT 的进入/使用/退出结构作为参考；PPT 未被改写。

## 独立任务与素材数量

| 品牌 | 指定特性 | COMPLETE / PARTIAL / MISSING | PNG / MP4 文件 | 处置及视觉审阅证据 |
|---|---:|---|---|---|
| OpenAI | 6 | 1 / 5 / 0 | 58 / 6 | [逐项处置](../01-openai/EVIDENCE-DISPOSITION.md)、[父任务审阅](openai-review-notes.md) |
| Anthropic | 6 | 0 / 6 / 0 | 53 / 7 | [检索日志](../02-anthropic/SEARCH-LOG.md)、[父任务审阅](anthropic-review-notes.md) |
| Google | 4 | 0 / 4 / 0 | 32 / 5 | [QA](../03-google/QA.md)、[父任务审阅](google-review-notes.md) |
| Apple | 5 | 0 / 4 / 1 | 33 / 3 | [QA](../04-apple/QA.md)、[父任务审阅](apple-review-notes.md) |
| 开源阵营 | 6 | 1 / 5 / 0 | 22 / 1 | [检索与自测](../05-opensource/SEARCH-LOG.md)、[父任务审阅](opensource-review-notes.md) |
| Microsoft | 3 | 0 / 3 / 0 | 25 / 4 | [状态与验证](../06-microsoft/STATUS.md)、[父任务审阅](microsoft-review-notes.md) |
| Meta | 5 | 1 / 4 / 0 | 46 / 6 | [状态与验证](../07-meta/STATUS.md)、[父任务审阅](meta-review-notes.md) |
| 合计 | 35 | 3 / 31 / 1 | 269 / 32 | 301 个正式媒体文件 |

2026-09-10 重新读取实际任务状态：前六家 turn 均 completed；Meta 的恢复 turn `01a08995-17b6-76f2-b98f-d63960ea1a29` 也为 completed、任务 idle。准确 ID、完成游标与处置理由见 [queue.json](queue.json)。本页依据实际任务状态与文件/内容复核，不依赖 STATUS 自报。

## 35 项逐项核对

每行的品牌包都包含六态说明、真实媒体、逐图 URL/时间码/日期、替代尝试和下一步；下表只提炼决定验收状态的内容。缺失的状态未伪造为图。

| 指定项 | 状态 | 已取得的关键证据 | 明确保留的缺口 / 限制 |
|---|---|---|---|
| [OpenAI @ 提及](../01-openai/README.md) | PARTIAL | @cal 候选、Calendar 标签、完整请求、执行状态 | 一句话并列多个应用、教学媒体独立发布日期 |
| OpenAI 人工审批 | PARTIAL | 官方权限/访问与可用控件材料 | 同一次动作批准、拒绝后继续/终止的完整链；商家按钮不当 agent 审批 |
| OpenAI 浏览器 / Computer Use | PARTIAL | 运行画面、过程、输入与浏览器状态 | 用户实际收回控制后的连续结果；Keynote 画中画不冒充浏览器 |
| OpenAI 产物落地 | COMPLETE | spreadsheet、演示、dashboard、web app 四类实际产物图及来源 | 图像要求完整，不外推所有格式与写入权限均实测 |
| GPT-Live 语音 | PARTIAL | 视觉卡片、语音状态等多个官方片段 | 用户打断、模型接话、后台委派的同任务连续证据；波形不证明全双工 |
| Atlas agent | PARTIAL | 历史授权、运行条、Take control / Stop、购物车与结账询问 | 2025 背景；未实测停服和实际接管 |
| [Cowork 文件夹授权](../02-anthropic/README.md) | PARTIAL | 文件夹选择、范围警告、Allow / Always allow | 永久删除的动作审批、撤销持久授权；清空文件内容不等于删除文件 |
| Cowork 跨设备 | PARTIAL | 手机委托、桌面计划/产物、手机结果/追问 | 任务书指定“桌面起→手机→桌面”方向与每阶段两帧未完整出现 |
| Cowork 过程 | PARTIAL | 计划/checklist/Progress、中途插话 | 清晰完整组为 2 月背景；当季同链产物/退出仍缺 |
| Design 三种收敛 | PARTIAL | 批注、参数面板、文字选择/编辑、真实滑杆静态图 | 三种方式各自三帧完整操作尚不齐；数值字段不称实际拖动 |
| Design → Code | PARTIAL | Export、handoff 对话、Copy command | 接收端实际运行与接收结果 |
| Claude Code 抽象 | PARTIAL | Skills 命令/面板、Subagents 与 Agent Teams 官方讲义/终端图 | 多 agent 完整运行、管理与退出链；讲义结构图不当实测 |
| [Spark 后台任务](../03-google/README.md) | PARTIAL | 任务、进度、Needs input、产物、主动通知、Turn off 设置 | 首次授权、否决建议、批准/拒绝本体；关闭控件未点击 |
| Google 算力计费 | PARTIAL | 当前/周用量与 credits 页面 | 单次任务费用、事前估价与接近额度提示 |
| Chrome agent | PARTIAL | 输入、计划、Start task、运行控件、商家结果 | 实际暂停/接管后状态与支付审批；7 张原始宽1080 |
| Google 生成入口 | PARTIAL | Gemini app、Flow、Shorts 三处实际入口图 | Flow 未显式显示 Omni 选择器；2 张 Shorts 原始宽1080 |
| [Apple 折叠输入](../04-apple/README.md) | PARTIAL | Duo 展开、内屏/分屏及官方键盘图 | 外内屏同任务接续、笔/hover 等未证实新手势 |
| Apple Home Hub 存在感知 | MISSING | 官方活动/Newsroom 与替代来源核验记录 | 未找到任务书所指本季新品官方发布，无法取得真实交互图 |
| Siri 委托面 | PARTIAL | 屏幕/个人上下文、应用引用、Maps 路线预览 | 完整审批、执行/撤销、接管与退出；GO 未点击 |
| Apple 跨设备 | PARTIAL | 分立 Siri 设备 UI、官方 iCloud 同步说明、第三方 beta 文字 | 同一 conversation 的连续设备接力录像 |
| Watch / AirPods | PARTIAL | Watch 回答、AirPods 翻译/音量演示 | 新手势的完整输入结果链；人物触耳不当“双柄按压”证据，头部动作图属背景 |
| [OpenWork Desktop](../05-opensource/README.md) | PARTIAL | 实际三行文件任务，Wrote/Read、预览、新会话、另一次 Resume 失败 | 原生连续录屏、人工修改后成功恢复链 |
| 跨 agent 技能复用 | PARTIAL | Codex / Claude Code / Cursor 配置 dry-run | 三个 agent 实际加载同一技能并完成任务 |
| Open Design CLI | PARTIAL | 本地 daemon/project、真实手工 HTML fixture 登记、补充 CLI 视频 | 原生终端录屏失败；手工产物不当 AI 生成产物 |
| 设计系统 token | PARTIAL | 151 项接口与 Apple picker 实测 | 四条通道均未产出同任务前后 artifact；不可用 picker 替代应用效果 |
| 插件与自扩展 | PARTIAL | 实际 scaffold、validate warning、pack 文件 | 未发布插件；打包不等于市场上架 |
| 社区三条 issue | COMPLETE | 登录、BYOK/private IP、summary loop 三条实际 issue 图与链接 | 按讨论量与交互影响选取，不宣称是全仓数学意义前三 |
| [Windows runtime](../06-microsoft/README.md) | PARTIAL | 会话/进程、MXC 策略、实际拒绝、Agent365 库存/Block 入口 | 本机统一调度、当前运行数和 kill；库存与未执行 Block 不能代替 |
| Windows 权限 | PARTIAL | 文件路径、写入拒绝、CLI Filesystem / Network 设置 | 消费者统一应用×能力权限总览、接管、退出；开发配置与用户审批分开 |
| Copilot agent | PARTIAL | Browse with Copilot 进入、委托、working、草稿、最终确认 | 当前版本实际接管与退出；2025 Take control 图仅背景 |
| [Meta 神经手写](../07-meta/README.md) | PARTIAL | CES 六个不同交互帧；3 月六帧更新与两段片 | 纠错/删除、入口/退出、未剪辑时延；CES 背景，更新图源宽1080 |
| Meta 手势集 | PARTIAL | 两种 pinch 的动作起止/EMG，另有概念 wrist roll；官方 Web App 映射 | 四向 swipe 实拍、消费 HUD 结果、误触阈值与走路验证 |
| Meta HUD | PARTIAL | 六张官方 POV 和短片；第三方提词器透镜图单列另一组 | 官方合成不当光学实拍；真实消失时机与区域框功能名未核定 |
| Meta 提词器 | PARTIAL | 设置页、三个不同透镜文字卡、官方 Band 导航说明 | 连续翻页/速度/退出、页码相邻性；全部图原始宽不足1280 |
| Meta 腕带外用 | COMPLETE | Garmin/Utah PoC/研究图，5 月 CMU 双带校准/EMG/游戏连续片 | 研究/PoC 证据完整；不声称消费通用控制、配对或退出已可用 |

## 新硬件逐家核对

| 品牌 | 本轮结论与证据边界 |
|---|---|
| OpenAI | 官方合作声明可核；具体设备、规格/交互及时间未核实，保持观察清单，未展开传闻 |
| Anthropic | 未找到自有终端；桌面/手机/Slack/IDE/云平台载体与 MHS 研究接口分别记录，不替公司编造不做硬件的理由 |
| Google | 音频与显示线分开；音频秋季口径和实际 keynote 任务图已采，显示线当前完整交互与确定出货仍缺；XREAL 有线空间设备不混成时尚眼镜 |
| Apple | 9 月 9 日官方发布逐机核验；Duo、18 Pro/Max、Watch 12/Ultra 4、AirPods 5 已有官方图；Home Hub、新 Apple TV 与主持事实保留未核边界 |
| 开源阵营 | 当前仓库/官网范围未发现自有硬件；已有电脑与 agent/CLI/MCP 为可核载体，不外推长期战略 |
| Microsoft | 2026 Surface 图、RTX Spark 预发布页面与 Copilot 键官方说明；普通 NPU 设备和持续 GPU 负载设备分开；旧按键不冒充今年新增 |
| Meta | 官方 Display+Band 配套、历史发布及当前美国市场已核；研究外用和双带装置另列；以有接触表面的手写替换草案“无表面输入” |

## 文档、来源与媒体

- 七家 README 均保留原样 §1–§7，包含文件/权限/产物矩阵、五条拆分归因、同样三个问题和空白人填标题。最终将全部逐文件表同步到各 README §7，未只留代表图或来源链接。
- 七家 SOURCES 与根总表共覆盖 301 个正式媒体文件；每行有文件、特性、URL、时间码/页面状态、抓取日期与官方性。各媒体目录有 source.md。抓取日期与发布日期不混用。
- 269 个 PNG 文件中存在 6 对字节相同的跨特性/全局参考复用，即 263 个不同图像哈希；它们在来源与覆盖统计中不增加独立交互状态数。269 是文件数，不是 269 个独立状态。
- 源分辨率缺口 23 张：Google 9 张原始1080、Meta 14 张原始750/1000/1080/1250。Google 的补白不提升有效宽度；Meta 未放大。低清文件仍为 PARTIAL 证据。
- 32 段正式短片均不超过30秒；原始长视频放在各 _work，不混入正式短片清单。连续片的内部剪辑、官方合成、第三方相机取景和自测转录分别标注。
- 目检实际纠正了字幕/画面时间错位、未经操作的按钮、清空与删除混淆、人物外拍凑帧、视角误认、原图低清和不同任务拼接等问题；细节见逐品牌父任务审阅记录。媒体解码和链接检查不能替代这些判断。

## 汇总要求与原始材料

[趋势总览](../00-趋势总览.md)包含七行三个问题，以及 Chrome/Atlas、Apple/Cowork、OpenWork/Cowork、Open Design/Claude Design、Windows/Cowork、Home Hub/Spark 的并排材料。开源/Apple/Google 的载体结构和 Anthropic/Google/Meta/Apple 的输入输出对照也已保留。未用功能数量或素材数量推断体验质量。

[99-华为推荐动作.md](../99-华为推荐动作.md)严格只有“现象 / 我们的缺口 / 具体动作 / 怎么验证”四个标题。未填写用户观点、品牌评分或华为建议。根目录原始 PPT、PDF、任务书未覆盖、未删除；[原稿采用边界](original-demand.md)说明了可提取正文与无法定位个人署名的限制。

本次可交付的是有明确缺口的公开素材包。各项再采条件已留在品牌 coverage.json / SEARCH-LOG.md；这些条件不应在后续引用时被压缩成“素材全部齐全”。
