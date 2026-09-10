# Apple｜2026 Q3 交互素材包

核验日期：2026-09-09（America/Toronto）  
研究范围：仅 Apple；事实、官方演示、研究推断与素材缺口分开记录。  
验收结论：`COMPLETE 0 / PARTIAL 4 / MISSING 1`。这里的“完成”只指单项素材门槛，不等于产品能力优劣。

## §1 一句话结论

Apple 本季把“把活交出去”的载体扩到可折叠大屏、系统级 Siri AI、腕上与耳上界面；截至本次核验，官方发布清单未见传闻中的 7 英寸 Home Hub，“家庭常驻、趋近无界面的委托面”仍缺少本季官方新品证据。

这句话由三组可核事实支撑：iPhone Duo 把同一比例的外屏/内屏与 Split View 做成新任务空间；Siri AI 增加 Dynamic Island 下拉、系统上下文菜单、屏幕感知、跨 App 个人上下文和独立历史 App；Apple Watch 与 AirPods 5 承担随身、免手持入口。活动回放截至本次收口仍显示“available shortly”，所以任务书中的“John Ternus 首次主持”维持 `UNVERIFIED`。

## §2 产品矩阵

| 层级 | 2026 Q3 官方对象 | 交互位置 | 2026-09-09 状态 | 证据边界 |
|---|---|---|---|---|
| 智能能力层 | Apple Intelligence | Photos、Messages、Safari、Writing Tools 等系统/应用能力 | OS 27 随 9 月 14 日提供；功能受机型、语言、地区限制 | 不把后台模型能力算作独立入口 |
| 系统助理 | Siri AI | “Hey Siri”、侧键、Dynamic Island 下拉、Spotlight、系统上下文菜单、Camera Siri mode、Vision Pro 凝视后说话 | iOS/iPadOS/macOS/visionOS 开发者测试；面向用户的英语 beta 于 9 月 14 日开始滚动 | 已有官方 UI 与演示；可用性不是全球同步 |
| 会话容器 | 独立 Siri App | iPhone、iPad、Mac、Apple Watch、Apple Vision Pro | 官方宣布；会话历史通过 iCloud 私密同步 | 官方说法明确“Mac 开始、其他设备继续”，未找到连续真实接力演示 |
| 新形态手机 | iPhone Duo + iOS 27 | 5.4 英寸外屏、7.6 英寸内屏、双页主屏、Split View | 9 月 9 日发布；10 月 16 日预购、10 月 23 日开售 | 官方片段覆盖展开与分屏；键盘另有官方静态图，Pencil/hover 未见操作证据 |
| 常规旗舰 | iPhone 18 Pro / Pro Max | 常规单屏、Dynamic Island、Camera、Siri AI | 9 月 12 日预购、9 月 18 日开售 | 作为性能/相机与 Siri AI 主载体；不是新的形态入口 |
| 腕上载体 | Apple Watch Series 12 / Ultra 4 + watchOS 27 | 腕上语音、Smart Stack 建议 | 9 月 9 日发布；9 月 18 日开售 | Siri Watch 演示来自 6 月，不足以证明 Series 12 独有新手势 |
| 耳上载体 | AirPods 5 | 免手 Siri AI、头部响应、双柄按压发起翻译、柄部音量滑动 | 9 月 9 日发布；9 月 18 日开售 | Live Translation 与音量滑动有 2026 官方视频；头部动作只有文字确认与 2024 背景演示 |
| 家庭 | 现有 Home App / HomePod / Apple TV 4K home hub 角色 | 家居控制与自动化 | 现有产品/角色 | 与任务书所指 7 英寸 Home Hub 新品不同；截至核验未见该新品官方发布 |

## §3 特性详解 ×N

### 3.1 折叠形态对输入的连带改动 — PARTIAL

官方片连续展示外屏、展开、内屏主屏、宽屏网页、Split View、应用对换和双拇指游戏，已经超过任务书的 5 帧门槛。官方文字还确认两块屏幕同一纵横比、内容按比例连续缩放；Split View 可并排两 App、交换 App、开同 App 双窗口；竖持内屏有更宽键盘；Apple Pencil USB‑C 支持“今年稍后”到来。

但演示片没有拍到外屏上的具体任务在内屏中继续，也没有 Apple Pencil 操作或 hover 新手势。Newsroom 静态图可看清展开内屏的全宽 QWERTY 键盘、文档编辑区与 Siri 输入框，但不是键盘输入过程，也没有外/内屏前后对照，因此仍不能标 COMPLETE。

| 流程环节 | 是否看见 | 证据 |
|---|---|---|
| 进入 | 已看见 | [01 外屏](assets/foldable-input/01-outer-display.png)、[02 展开](assets/foldable-input/02-opening.png) |
| 委托 | 未看见 | 该片段是形态与多任务演示，没有 agent 委托 |
| 过程 | 已看见 | [03 内屏主屏](assets/foldable-input/03-inner-home.png) → [05 宽屏网页](assets/foldable-input/05-inner-web.png) → [06 分屏](assets/foldable-input/06-split-view.png) |
| 接管 | 部分看见 | 手指滚动、交换窗口和双拇指操作可见；没有 agent 执行后的人工接管节点 |
| 产物 | 已看见 | 分屏布局与并行 App 可见，[07 对换后分屏](assets/foldable-input/07-split-view-swapped.png) |
| 退出 | 未看见 | 没有关闭分屏、回到外屏或任务结束状态 |

键盘静态证据：[09 内屏全宽键盘 + Write with Siri](assets/foldable-input/09-inner-keyboard-write-with-siri.png)。下载片段：[00:08–00:38，29.997 秒](assets/foldable-input/clip.mp4)。逐帧时码见 [source.md](assets/foldable-input/source.md)。

### 3.2 Home Hub 的存在感知 — MISSING

Apple 9 月 9 日活动的官方发布清单只有 iPhone Duo、iPhone 18 Pro、Apple Watch Series 12、Apple Watch Ultra 4、AirPods 5；官方 Newsroom TV & Home 档案也没有 9 月新品。当前 Home App 页面中的 “home hub” 指 HomePod、HomePod mini 或 Apple TV 的既有系统角色，不能当作 7 英寸新品。

| 流程环节 | 是否看见 | 证据 |
|---|---|---|
| 进入 | 未看见 | 无新品、无人走近触发演示 |
| 委托 | 未看见 | 无无声/隐式委托演示 |
| 过程 | 未看见 | 无身份判断或任务过程 UI |
| 接管 | 未看见 | 无取消、覆盖或接管动作 |
| 产物 | 未看见 | 无 7 英寸 Home Hub 产物界面 |
| 退出 | 未看见 | 无离开、息屏或隐私退出反馈 |

目录只保留证据说明，不用既有 Home App 截图冒充新品：[source.md](assets/home-hub-presence/source.md)。

### 3.3 Siri 的委托面变化 — PARTIAL

委托面已经从“一句话”扩成多种指代：Dynamic Island 下拉进入；针对当前 Instagram 内容追问“这里具体是哪里”；从 Messages 中找 Jeff 的地址，再把它组合到路线请求；Mac 系统上下文菜单可对图像、文件、文字点选 “Ask Siri”；iPad/Camera/Vision Pro 提供视觉指代。

这组证据证明了语句、当前屏幕、选择对象与跨 App 个人上下文，但公开演示没有明确的执行前批准、撤回、人工接管和退出状态。

| 流程环节 | 是否看见 | 证据 |
|---|---|---|
| 进入 | 已看见 | [Dynamic Island](assets/siri-delegation/01-dynamic-island.png) → [下拉展开](assets/siri-delegation/02-swipe-down-entry.png) |
| 委托 | 已看见 | [当前屏幕追问](assets/siri-delegation/03-screen-aware-result.png)、[“Jeff 的新住址在哪？”](assets/siri-delegation/04-jeff-query.png) |
| 过程 | 部分看见 | [从消息取得地址](assets/siri-delegation/05-message-address.png)；没有完整工具调用或阶段反馈 |
| 接管 | 未看见 | 后续追问属于追加约束，不是明确暂停/批准/接管 |
| 产物 | 已看见 | [组合路线结果](assets/siri-delegation/06-route-result.png) |
| 退出 | 未看见 | 没有关闭 Siri 或清除上下文演示 |

选择/指向补充：[Mac 上下文菜单](assets/siri-delegation/07-selection-context-menu.png)、[iPad Visual Intelligence](assets/siri-delegation/08-visual-intelligence-ipad.png)。下载片段：[01:30–02:00，29.997 秒](assets/siri-delegation/clip.mp4)。详见 [source.md](assets/siri-delegation/source.md)。

### 3.4 跨设备接力 — PARTIAL

官方明确写明：Siri App 通过 iCloud 私密同步会话历史，可在 Mac 开始，再在 iPhone、iPad、Apple Watch 或 Apple Vision Pro 继续；Watch 的 Smart Stack 建议也能帮助继续最近会话。已收集四种设备上的真实官方 UI。

缺口是核心门槛：没有找到同一会话从设备 A 离开、在设备 B 出现并继续的连续演示。Android Authority 的开发者 beta 上手文字记录了 iPhone 17 Pro 开始旅行研究、在 iPad Air 等待短暂同步后看到原会话，但文章没有给出可逐帧核验的 A→B 连续视频；因此四张官方 UI 与这条第三方实测只支持“存在接力”，不能证明完整操作、具体延迟或上下文保真。[第三方 beta 上手](https://www.androidauthority.com/siri-ai-vs-gemini-hands-on-comparison-3677330/)

| 流程环节 | 是否看见 | 证据 |
|---|---|---|
| 进入 | 已看见（分立） | [iPhone Siri 会话](assets/cross-device-handoff/01-iphone-siri-app.png)、[iPad Siri App](assets/cross-device-handoff/02-ipad-siri-app.png) |
| 委托 | 部分看见 | 每台设备各有 Siri 查询/会话，但不是同一任务连续录屏 |
| 过程 | 未看见 | 未看到 iCloud 同步等待、跨设备提示或冲突处理 |
| 接管 | 未看见 | 未看到 B 设备接管同一任务的动作 |
| 产物 | 已看见（分立） | [Watch 回答](assets/cross-device-handoff/03-watch-siri-answer.png)、[Vision Pro Siri 空间界面](assets/cross-device-handoff/04-vision-pro-siri.png) |
| 退出 | 未看见 | 未看到 A 设备结束或 B 设备完成后的退出 |

详见 [source.md](assets/cross-device-handoff/source.md)。

### 3.5 Watch / AirPods 上的新交互 — PARTIAL

Watch 官方演示可见腕上语音提问与回答；AirPods 5 官方演示可见佩戴/触碰耳机、查看纸质信息与面对面交流，另有柄部音量滑动。Apple 官方文字确认 Live Translation 可由同时按压两侧耳机柄触发，也确认 AirPods 5 可用点头/摇头回应 Siri；短片没有翻译文字/音频 UI，00:03 单帧本身也不足以证明完成了“双柄同时按压”。

当前 2026 AirPods 5 视频没有清楚演示点头/摇头，故保留一张 2024 官方 Siri Interactions 帧作历史背景，不能用它证明 2026 新增。Watch 片也没有捏合或其他 Series 12 独有新手势。

| 流程环节 | 是否看见 | 证据 |
|---|---|---|
| 进入 | 已看见 | [Watch 语音查询](assets/watch-airpods-input/01-watch-query.png)、[AirPods 佩戴/触碰](assets/watch-airpods-input/03-airpods-press-to-translate.png)；双柄触发方式来自官方文字 |
| 委托 | 已看见 | Watch 语音问题；AirPods 发起翻译 |
| 过程 | 部分看见 | [Live Translation 场景](assets/watch-airpods-input/04-live-translation-conversation.png)；识别、翻译与播放状态不可见 |
| 接管 | 未看见 | 没有暂停、取消或人工改写翻译 |
| 产物 | 部分看见 | [Watch 回答](assets/watch-airpods-input/02-watch-answer.png)可见；AirPods 只见[交流继续](assets/watch-airpods-input/05-conversation-outcome.png)，没有翻译内容 UI |
| 退出 | 未看见 | 没有结束翻译/离开 Siri 的明确状态 |

补充动作：[柄部音量滑动](assets/watch-airpods-input/06-volume-swipe.png)；背景帧：[2024 头部动作](assets/watch-airpods-input/07-head-gesture-background-2024.png)。下载片段：[Live Translation，14.825 秒](assets/watch-airpods-input/clip.mp4)。详见 [source.md](assets/watch-airpods-input/source.md)。

## §4 新硬件

任务书列的是会前传闻；以下已逐条替换为截至 9 月 9 日核验到的 Apple 官方口径。发布硬件图见 [hardware-status](assets/hardware-status/source.md)。

| 会前预期 | 会后官方状态 | 时间 | 它解决了软件解决不了的什么（研究推断） | 新交互证据 |
|---|---|---|---|---|
| 折叠 iPhone（Ultra 或 Duo） | **已发布：iPhone Duo** | 10/16 预购，10/23 开售 | 把 7.6 英寸多任务画布折进口袋，同时保留单手外屏 | 外/内屏、转向、Split View、双拇指；键盘有官方静态图，Pencil/hover 未见操作证据 |
| iPhone 18 Pro | **已发布** | 9/12 预购，9/18 开售 | 为相机、持续性能与 Siri AI 提供主流旗舰载体 | 更小 Dynamic Island、Camera 与 Siri AI；形态入口仍是传统单屏 |
| iPhone 18 Pro Max | **已发布** | 9/12 预购，9/18 开售 | 用更大机身容纳续航与大屏，不引入折叠状态转换 | 同 Pro 家族，未单列新输入范式 |
| Watch Series 12 | **已发布** | 9/18 开售 | 腕上低摩擦访问与全天健康感知，不必掏手机 | Siri AI 腕上语音/Smart Stack；无 Series 12 独有新手势实录 |
| Watch Ultra 4 | **已发布** | 9/18 开售 | 让长时户外运动、定位和健康感知在手机不可用时仍持续 | 本次采集未发现新的委托手势 |
| AirPods 5 | **已发布** | 9/18 开售 | 把输入/反馈放到耳边，让视线和双手可被当前任务占用 | 免手 Siri、头部回应、按压翻译、柄部音量滑动 |
| 7 英寸 Home Hub | **截至核验未见本场官方发布 / MISSING** | 无 | 任务书推断的“家庭常驻入口”仍无新品承载 | 未找到本季官方接近感知/身份/隐私 UI |
| 新 Apple TV 4K | **截至核验未见本场官方发布 / UNVERIFIED** | 无 | 不对未核实产品写能力动机 | 当前产品页仍列 A15 Bionic 既有机型 |

额外边界：任务书写“新任 CEO John Ternus 首次主持”。John Ternus 的 CEO 身份可由当日 iPhone Duo 新闻稿确认；但活动回放尚不可用，无法确认“实际主持人”，故这一句是 `UNVERIFIED`。

## §5 拆分逻辑

对着任务书的五条归因，Apple 这样拆产品：

1. **工具装载**：用户不在 Siri 内手工安装“工具”。官方称 system orchestrator 调用 Spotlight index 与 App Toolbox；第三方 App 需要开发者接入，边界由系统能力、App 集成和设备支持共同决定。
2. **产物形态**：即时回答留在 Siri 浮层/独立 App；路线预览落到 Maps；日历、邮件、照片编辑等动作落回目标 App；长对话作为 Siri App 历史，经 iCloud 私密同步。形态不同，所以需要系统助理、会话容器和 App 内能力并存。
3. **爆炸半径**：从“回答当前屏幕问题”扩到读取消息、邮件、照片，并跨 App 组合或改写内容。越接近可变更的 App 动作，风险越大；但官方片很少展示权限确认、预览后执行、撤销和错误恢复，因此真实半径仍需 beta 自测。
4. **反馈回路**：Dynamic Island、Siri 回答、Maps 路线和 Watch/AirPods 结果提供即时反馈；本包公开画面没有展示完整的工具调用过程、长时等待、接管、拒绝和退出反馈，因而无法判断用户如何控制一次长任务。Apple Developer 的 App Intents 资料存在可取消意图与 Live Activity 进度能力，但这不是 Siri AI 端到端用户演示，不能补齐该缺口。
5. **买单人**：硬件购买者为不同载体买单；OS/Siri AI 随兼容设备提供。官方注明服务器侧功能可能有每日额度，未来扩大访问可能收费，但当前 UI 没有单次任务价格或面向团队/管理员的采购边界。

补充的交互观察轴是“载体位置 × 指代来源 × 执行边界”：口袋/内屏/腕/耳/空间决定入口，语句/屏幕/选择/相机/个人上下文决定指代，回答/检索/跨 App 动作决定风险。

任务书要求与 Cowork、Gemini Spark 并排比较，但本 goal 被限定为 Apple 单品牌证据包；跨品牌判断留给总览，避免拿其他品牌事实污染本目录。

## §6 三个必答问题

### 1. 它把能力拆成了几块，边界画在哪？

- **能碰到什么文件/内容**：当前屏幕、图像/文件/文字选择、Messages、Mail、Photos、Spotlight 索引和已接入 App 的内容；第三方 App 需要开发者集成。公开材料没有给出逐目录文件系统访问范围。
- **什么权限**：官方强调本机处理、Private Cloud Compute 和 iCloud 私密同步；功能还受兼容设备、Apple Account、语言、地区、beta 与 App 接入限制。公开 UI 未显示每次跨 App 读取的授权清单。
- **产物落在哪**：回答在 Siri 浮层/独立 App；路线在 Maps；写作、日历、照片等变更在目标 App；会话历史在 Siri App，并通过 iCloud 同步。

据此可分成系统助理、独立会话 App、系统级视觉/写作能力、App 内动作、跨设备载体五块。边界很宽；本包公开画面没有完整展示“调用了什么、是否已执行、能否撤销”，因此这些状态在本次证据中仍不可核验。

### 2. 它的委托面在往哪走——更显式还是更隐式？

目前仍以显式启动为主：说话、按键、下拉 Dynamic Island、点选上下文菜单、按压 AirPods。隐式成分主要是个人上下文检索、Watch Smart Stack 主动建议、Call Context 等系统主动露出。Home Hub 缺席意味着“人走近就触发”的家庭级隐式委托没有本季实证。

### 3. 它的硬件在补软件的哪块短板？没硬件的怎么绕过去？

iPhone Duo 补的是“更大的并行工作面仍能装进口袋”；Watch 补的是“手机不在手里时的腕上连续可达”；AirPods 补的是“手和眼被占用时的耳上输入/反馈”。iPhone 18 Pro/Max 提供算力、相机与续航基线。截至本次核验，官方发布清单未见传闻中的家庭屏和新 Apple TV，本包不能据此确认新的家庭常驻委托载体。

## §7 素材与出处表

以下逐文件表与 [SOURCES.md](SOURCES.md) 同步；同源重复参考不增加独立流程帧数。

核验日期：2026-09-09（America/Toronto）。主证据均为 Apple 官方公开页面或官方 CDN；2024 AirPods 片单列为背景。

### 发布会与硬件

1. [Apple Events](https://www.apple.com/apple-events/) — 2026-09-09 当日发布清单；收口时回放仍显示“available shortly”。
2. [Apple Developer｜Hello, September 2026](https://developer.apple.com/hello/september26/) — 活动日期与 10:00 PT。
3. [iPhone Duo Newsroom](https://www.apple.com/newsroom/2026/09/apple-unveils-iphone-duo/) — 屏幕、iOS 27、Split View、Pencil、上市日期。
4. [iPhone Duo 产品页](https://www.apple.com/iphone-duo/) — 外/内屏形态、键盘、Split View 与官方产品片。
5. [iPhone 18 Pro / Pro Max Newsroom](https://www.apple.com/newsroom/2026/09/apple-debuts-iphone-18-pro-and-iphone-18-pro-max/) — 两机型与上市日期。
6. [Apple Watch Series 12 Newsroom](https://www.apple.com/newsroom/2026/09/introducing-apple-watch-series-12-with-the-all-new-health-sensing-system/) — 2026-09-09。
7. [Apple Watch Ultra 4 Newsroom](https://www.apple.com/newsroom/2026/09/apple-unveils-apple-watch-ultra-4/) — 2026-09-09。
8. [AirPods 5 Newsroom](https://www.apple.com/newsroom/2026/09/apple-introduces-airpods-5-with-best-in-class-open-ear-active-noise-cancellation/) — 免手 Siri、头部回应、Live Translation、音量滑动与上市日期。
9. [OS 27 总览](https://www.apple.com/os/) — iOS/iPadOS/macOS/watchOS/visionOS 27 于 9 月 14 日提供，Siri AI 英语 beta 滚动推出。

### 交互与缺口核查

10. [Siri AI Newsroom](https://www.apple.com/newsroom/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/) — 入口、屏幕感知、跨 App 个人上下文、上下文菜单、Watch、Siri App 与 iCloud 同步。
11. [iOS 27](https://www.apple.com/os/ios/) — Siri App 与“iPhone 提问、iPad 继续”的官方说明/UI。
12. [iPadOS 27](https://www.apple.com/os/ipados/) — iPad Siri App 官方 UI。
13. [Home App](https://www.apple.com/home-app/) — 既有 HomePod/HomePod mini/Apple TV 可充当 home hub；不是 7 英寸新品。
14. [Apple TV 4K](https://www.apple.com/apple-tv-4k/) 与[技术规格](https://www.apple.com/apple-tv-4k/specs/) — 当前仍列 A15 Bionic。
15. [Newsroom TV & Home archive](https://www.apple.com/newsroom/archive/tv-home/) — 截至核验时没有 2026-09 Home Hub 或新 Apple TV 4K 发布稿。
16. [Android Authority｜Siri AI vs. Gemini hands-on](https://www.androidauthority.com/siri-ai-vs-gemini-hands-on-comparison-3677330/) — 记者称在 iPhone 17 Pro 开始旅行研究后，于 iPad Air 看到同一会话；为真实开发者 beta 文字实测，不是连续视频。
17. [Apple Developer｜CancellableIntent](https://developer.apple.com/documentation/appintents/cancellableintent) 与 [WWDC26 App Intents](https://developer.apple.com/videos/play/wwdc2026/345/) — 证明 App Intent 可取消、长任务可用 Live Activity 报进度的开发接口；不等同于 Siri AI 用户端暂停/批准/接管演示。

### 官方媒体直链

- Duo 产品片：`https://www.apple.com/105/media/us/iphone-duo/2026/9305e4b9-72d9-4c05-9381-b572adadd5e5/films/product/iphone-duo-product-tpl-us-2026_1920x1080l_avc_vid_segments/prog_index.m3u8`
- Siri Personal Assistant：`https://www.apple.com/newsroom/videos/2026/hls/06/apple-siri-ai-personal-assistant/US/US/Apple-Siri-AI-personal-assistant-260608_16x9.m3u8`
- Siri Dynamic Island：`https://www.apple.com/newsroom/videos/2026/autoplay/06/apple-siri-ai-dynamic-island-gesture/large_2x.mp4`
- Siri on Watch：`https://www.apple.com/newsroom/videos/2026/autoplay/06/apple-siri-ai-on-apple-watch/large_2x.mp4`
- AirPods 5 Live Translation：`https://www.apple.com/newsroom/videos/2026/hls/09/apple-airpods-5-live-translation/US/US/Apple-AirPods-5-Live-Translation-260909_16x9.m3u8`
- AirPods 5 volume swipe：`https://www.apple.com/newsroom/videos/2026/autoplay/09/apple-introduces-airpods-5-with-best-in-class-open-ear-active-noise-cancellation/apple-airpods-5-volume-swiping/large_2x.mp4`
- Mac “Ask Siri” 图：`https://www.apple.com/newsroom/images/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/article/Apple-Siri-AI-ask-about-images-260608_big.jpg.large_2x.jpg`
- iPad Visual Intelligence 图：`https://www.apple.com/newsroom/images/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/article/Apple-Siri-AI-Visual-Intelligence-on-iPad-260608_big.jpg.large_2x.jpg`
- iPhone Siri conversation 图：`https://www.apple.com/newsroom/images/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/article/Apple-Siri-app-chat-260608_inline.jpg.large_2x.jpg`
- iPad Siri App 图：`https://www.apple.com/v/os/g/images/shared/siri/siri_app__bf82k75xd8z6_large_2x.jpg`
- Vision Pro Siri 图：`https://www.apple.com/newsroom/images/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/article/Apple-Siri-AI-on-Apple-Vision-Pro-260608_big.jpg.large_2x.jpg`
- Duo 内屏键盘 + Write with Siri 图：`https://www.apple.com/newsroom/images/2026/09/apple-unveils-iphone-duo/article/Apple-iPhone-Duo-write-with-Siri-260909_big.jpg.large_2x.jpg`
- 2024 AirPods Siri Interactions（背景）：`https://www.apple.com/newsroom/videos/videos-2024/hls/2024/09/Apple_AirPods_SiriandVoiceIsolation/apple-airpods-siri-and-voice-isolation-240909_16x9.m3u8`

五张硬件总览图改用对应 Newsroom 的 1306–1960px 官方图；逐图直链见 [assets/hardware-status/source.md](assets/hardware-status/source.md)。Apple Events 的 2x 卡片实际仅 760px 宽，只用于核对发布清单，不作为正式图。

### 逐素材账本

以下与 `README.md` §7.1 同步；时间码为原始官方媒体位置，抓取日期均为 2026-09-09。

| 文件名 | 对应特性 | 来源 URL | 源时间码 | 官方性 | 抓取日期 |
| --- | --- | --- | ---: | --- | --- |
| [assets/foldable-input/01-outer-display.png](assets/foldable-input/01-outer-display.png) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 00:04 | Apple 官方演示 | 2026-09-09 |
| [assets/foldable-input/02-opening.png](assets/foldable-input/02-opening.png) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 00:08 | Apple 官方演示 | 2026-09-09 |
| [assets/foldable-input/03-inner-home.png](assets/foldable-input/03-inner-home.png) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 00:12 | Apple 官方演示 | 2026-09-09 |
| [assets/foldable-input/04-inner-photos.png](assets/foldable-input/04-inner-photos.png) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 00:16 | Apple 官方演示 | 2026-09-09 |
| [assets/foldable-input/05-inner-web.png](assets/foldable-input/05-inner-web.png) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 00:28 | Apple 官方演示 | 2026-09-09 |
| [assets/foldable-input/06-split-view.png](assets/foldable-input/06-split-view.png) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 00:34 | Apple 官方演示 | 2026-09-09 |
| [assets/foldable-input/07-split-view-swapped.png](assets/foldable-input/07-split-view-swapped.png) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 00:38 | Apple 官方演示 | 2026-09-09 |
| [assets/foldable-input/08-two-thumb-game.png](assets/foldable-input/08-two-thumb-game.png) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 01:52 | Apple 官方演示 | 2026-09-09 |
| [assets/foldable-input/09-inner-keyboard-write-with-siri.png](assets/foldable-input/09-inner-keyboard-write-with-siri.png) | 折叠输入 | [Duo Newsroom 图](https://www.apple.com/newsroom/images/2026/09/apple-unveils-iphone-duo/article/Apple-iPhone-Duo-write-with-Siri-260909_big.jpg.large_2x.jpg) | 静态 | Apple 官方 UI；非同源连续片 | 2026-09-09 |
| [assets/foldable-input/clip.mp4](assets/foldable-input/clip.mp4) | 折叠输入 | [Duo 产品片](https://www.apple.com/iphone-duo/) | 00:08–00:38 | Apple 官方演示剪段 | 2026-09-09 |
| [assets/siri-delegation/01-dynamic-island.png](assets/siri-delegation/01-dynamic-island.png) | Siri 委托 | [Dynamic Island 视频](https://www.apple.com/newsroom/videos/2026/autoplay/06/apple-siri-ai-dynamic-island-gesture/large_2x.mp4) | 00:00.3 | Apple 官方演示 | 2026-09-09 |
| [assets/siri-delegation/02-swipe-down-entry.png](assets/siri-delegation/02-swipe-down-entry.png) | Siri 委托 | [Dynamic Island 视频](https://www.apple.com/newsroom/videos/2026/autoplay/06/apple-siri-ai-dynamic-island-gesture/large_2x.mp4) | 00:01.3 | Apple 官方演示 | 2026-09-09 |
| [assets/siri-delegation/03-screen-aware-result.png](assets/siri-delegation/03-screen-aware-result.png) | Siri 委托 | [Personal Assistant](https://www.apple.com/newsroom/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/) | 01:20 | Apple 官方演示 | 2026-09-09 |
| [assets/siri-delegation/04-jeff-query.png](assets/siri-delegation/04-jeff-query.png) | Siri 委托 | [Personal Assistant](https://www.apple.com/newsroom/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/) | 01:30 | Apple 官方演示 | 2026-09-09 |
| [assets/siri-delegation/05-message-address.png](assets/siri-delegation/05-message-address.png) | Siri 委托 | [Personal Assistant](https://www.apple.com/newsroom/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/) | 01:40 | Apple 官方演示 | 2026-09-09 |
| [assets/siri-delegation/06-route-result.png](assets/siri-delegation/06-route-result.png) | Siri 委托 | [Personal Assistant](https://www.apple.com/newsroom/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/) | 01:58 | Apple 官方演示；GO 未点击 | 2026-09-09 |
| [assets/siri-delegation/07-selection-context-menu.png](assets/siri-delegation/07-selection-context-menu.png) | Siri 委托 | [Mac “Ask Siri” 图](https://www.apple.com/newsroom/images/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/article/Apple-Siri-AI-ask-about-images-260608_big.jpg.large_2x.jpg) | 静态 | Apple 官方 UI；独立场景 | 2026-09-09 |
| [assets/siri-delegation/08-visual-intelligence-ipad.png](assets/siri-delegation/08-visual-intelligence-ipad.png) | Siri 委托 | [iPad Visual Intelligence 图](https://www.apple.com/newsroom/images/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/article/Apple-Siri-AI-Visual-Intelligence-on-iPad-260608_big.jpg.large_2x.jpg) | 静态 | Apple 官方 UI；独立场景 | 2026-09-09 |
| [assets/siri-delegation/clip.mp4](assets/siri-delegation/clip.mp4) | Siri 委托 | [Personal Assistant](https://www.apple.com/newsroom/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/) | 01:30–02:00 | Apple 官方演示剪段 | 2026-09-09 |
| [assets/cross-device-handoff/01-iphone-siri-app.png](assets/cross-device-handoff/01-iphone-siri-app.png) | 跨设备 | [iPhone Siri 图](https://www.apple.com/newsroom/images/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/article/Apple-Siri-app-chat-260608_inline.jpg.large_2x.jpg) | 静态 | Apple 官方 UI；非连续接力 | 2026-09-09 |
| [assets/cross-device-handoff/02-ipad-siri-app.png](assets/cross-device-handoff/02-ipad-siri-app.png) | 跨设备 | [iPad Siri App 图](https://www.apple.com/v/os/g/images/shared/siri/siri_app__bf82k75xd8z6_large_2x.jpg) | 静态 | Apple 官方 UI；非连续接力 | 2026-09-09 |
| [assets/cross-device-handoff/03-watch-siri-answer.png](assets/cross-device-handoff/03-watch-siri-answer.png) | 跨设备 | [Watch Siri 视频](https://www.apple.com/newsroom/videos/2026/autoplay/06/apple-siri-ai-on-apple-watch/large_2x.mp4) | 00:07 | Apple 官方 UI；非连续接力 | 2026-09-09 |
| [assets/cross-device-handoff/04-vision-pro-siri.png](assets/cross-device-handoff/04-vision-pro-siri.png) | 跨设备 | [Vision Pro Siri 图](https://www.apple.com/newsroom/images/2026/06/apple-introduces-siri-ai-a-profoundly-more-capable-and-personal-assistant/article/Apple-Siri-AI-on-Apple-Vision-Pro-260608_big.jpg.large_2x.jpg) | 静态 | Apple 官方 UI；非连续接力 | 2026-09-09 |
| [assets/watch-airpods-input/01-watch-query.png](assets/watch-airpods-input/01-watch-query.png) | Watch/AirPods | [Watch Siri 视频](https://www.apple.com/newsroom/videos/2026/autoplay/06/apple-siri-ai-on-apple-watch/large_2x.mp4) | 00:00.5 | Apple 官方演示 | 2026-09-09 |
| [assets/watch-airpods-input/02-watch-answer.png](assets/watch-airpods-input/02-watch-answer.png) | Watch/AirPods | [Watch Siri 视频](https://www.apple.com/newsroom/videos/2026/autoplay/06/apple-siri-ai-on-apple-watch/large_2x.mp4) | 00:07 | Apple 官方演示 | 2026-09-09 |
| [assets/watch-airpods-input/03-airpods-press-to-translate.png](assets/watch-airpods-input/03-airpods-press-to-translate.png) | Watch/AirPods | [AirPods 5 Newsroom](https://www.apple.com/newsroom/2026/09/apple-introduces-airpods-5-with-best-in-class-open-ear-active-noise-cancellation/) | 00:03 | Apple 官方场景；单帧不证明双柄按压 | 2026-09-09 |
| [assets/watch-airpods-input/04-live-translation-conversation.png](assets/watch-airpods-input/04-live-translation-conversation.png) | Watch/AirPods | [AirPods 5 Newsroom](https://www.apple.com/newsroom/2026/09/apple-introduces-airpods-5-with-best-in-class-open-ear-active-noise-cancellation/) | 00:08 | Apple 官方场景；无翻译状态 UI | 2026-09-09 |
| [assets/watch-airpods-input/05-conversation-outcome.png](assets/watch-airpods-input/05-conversation-outcome.png) | Watch/AirPods | [AirPods 5 Newsroom](https://www.apple.com/newsroom/2026/09/apple-introduces-airpods-5-with-best-in-class-open-ear-active-noise-cancellation/) | 00:13 | Apple 官方场景；无翻译内容 UI | 2026-09-09 |
| [assets/watch-airpods-input/06-volume-swipe.png](assets/watch-airpods-input/06-volume-swipe.png) | Watch/AirPods | [Volume Swipe 视频](https://www.apple.com/newsroom/videos/2026/autoplay/09/apple-introduces-airpods-5-with-best-in-class-open-ear-active-noise-cancellation/apple-airpods-5-volume-swiping/large_2x.mp4) | 00:01.5 | Apple 官方演示 | 2026-09-09 |
| [assets/watch-airpods-input/07-head-gesture-background-2024.png](assets/watch-airpods-input/07-head-gesture-background-2024.png) | Watch/AirPods | [2024 Newsroom](https://www.apple.com/newsroom/2024/09/apple-introduces-airpods-4-and-a-hearing-health-experience-with-airpods-pro-2/) | 00:17 | Apple 官方背景；不计 2026 新证据 | 2026-09-09 |
| [assets/watch-airpods-input/clip.mp4](assets/watch-airpods-input/clip.mp4) | Watch/AirPods | [AirPods 5 Newsroom](https://www.apple.com/newsroom/2026/09/apple-introduces-airpods-5-with-best-in-class-open-ear-active-noise-cancellation/) | 00:00–00:14.825 | Apple 官方演示剪段 | 2026-09-09 |
| [assets/hardware-status/01-iphone-duo.png](assets/hardware-status/01-iphone-duo.png) | 新硬件 | [Duo Newsroom 图](https://www.apple.com/newsroom/images/2026/09/apple-unveils-iphone-duo/article/Apple-iPhone-Duo-colors-260909_big.jpg.large_2x.jpg) | 静态 | Apple 官方产品图 | 2026-09-09 |
| [assets/hardware-status/02-iphone-18-pro.png](assets/hardware-status/02-iphone-18-pro.png) | 新硬件 | [18 Pro/Max Newsroom 图](https://www.apple.com/newsroom/images/2026/09/apple-debuts-iphone-18-pro-and-iphone-18-pro-max/article/Apple-iPhone-18-Pro-2up-260909_inline.jpg.large_2x.jpg) | 静态 | Apple 官方产品图 | 2026-09-09 |
| [assets/hardware-status/03-watch-series-12.png](assets/hardware-status/03-watch-series-12.png) | 新硬件 | [Series 12 Newsroom 图](https://www.apple.com/newsroom/images/2026/09/introducing-apple-watch-series-12-with-the-all-new-health-sensing-system/article/Apple-Watch-Series-12-2up-260909_big.jpg.large_2x.jpg) | 静态 | Apple 官方产品图 | 2026-09-09 |
| [assets/hardware-status/04-watch-ultra-4.png](assets/hardware-status/04-watch-ultra-4.png) | 新硬件 | [Ultra 4 Newsroom 图](https://www.apple.com/newsroom/images/2026/09/apple-unveils-apple-watch-ultra-4/article/Apple-Watch-Ultra-4-hero-260909_big.jpg.large_2x.jpg) | 静态 | Apple 官方产品图 | 2026-09-09 |
| [assets/hardware-status/05-airpods-5.png](assets/hardware-status/05-airpods-5.png) | 新硬件 | [AirPods 5 Newsroom 图](https://www.apple.com/newsroom/images/2026/09/apple-introduces-airpods-5-with-best-in-class-open-ear-active-noise-cancellation/article/Apple-AirPods-5-hero-260909_big.jpg.large_2x.jpg) | 静态 | Apple 官方产品图 | 2026-09-09 |

### 证据等级

- `官方事实`：Apple 产品页、Newsroom、Events、Support/Developer 页面文字。
- `官方演示`：官方 CDN 视频、动画或 UI 图；不等于用户长时实测。
- `背景`：2026-03-09 之前材料，只说明先前交互形式。
- `研究推断`：基于形态与画面得出的 UX 解释，不冒充 Apple 原话。
- `MISSING / UNVERIFIED`：无有效公开证据，保留缺口。

## 待人填：观点 / 对我们的启发
