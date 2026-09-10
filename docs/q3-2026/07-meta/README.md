# Meta｜AI 交互与 Neural Band 证据包

范围：仅 Meta。研究窗口：2026-03-09 至 2026-09-09；更早材料统一标 `BACKGROUND`。抓取时间：2026-09-09（America/Toronto）。总体交付状态：`PARTIAL`——证据包已完成，但五项功能中仍有任务要求无法被现有公开证据验证，缺口不以推断补齐。

## §1 一句话结论

Meta 把“看见、显示、轻量选择”放进眼镜，把“静默、低幅、连续控制”放进腕带；近半年公开更新包括 Neural Handwriting 扩大可用范围，而完整手势集、误触边界、提词器速度控制和真实 HUD 消失时机仍缺可审计证据。

## §2 产品矩阵

| 产品 / 能力 | 能访问的内容与权限边界 | 产物落点 | 状态 / 市场与时间 |
|---|---|---|---|
| Meta Ray-Ban Display | 眼镜相机与麦克风输入；单目侧边显示用于短交互。公开材料不支持把它写成任意文件系统入口 | HUD 卡片、消息、地图、字幕/提示；音频反馈 | 消费产品；2025-09-17 发布、2025-09-30 美国开售；抓取日现行官方页仍仅写美国选定授权零售商与 Meta flagship stores |
| Meta AI 眼镜助手 / chat | 通过眼镜相机、麦克风与 Meta AI 处理用户当前所见/所问；本包未发现可直接浏览手机全部文件的权限 | 语音回答或 Display 上的短视觉结果 | 消费软件层；具体能力随地区、语言与支持服务变化，本包只核发布页明确画面 |
| 手机配套（Meta AI app 与系统分享链） | 配对、设置与受支持应用内容；提词器文本可由 Notes、Google Docs 或 Meta AI 复制粘贴后发送 | 设置保留在手机；提词文本进入眼镜卡片；消息发送到相应消息应用 | 消费配套层；不等同于腕带直接读取任意手机文件 |
| Meta Neural Band | 读取腕部肌电并提供触觉确认；Web App 只接收预定义四向 swipe、食指 enter pinch、中指 cancel pinch，不能自定义手势 | 控制事件送往眼镜/Web App；本身不生成文档 | 与 Display 同期发布、每副眼镜随附；市场跟随美国 Display |
| Neural Handwriting | 将食指在表面的轨迹经腕带识别为文字；公开材料未证实纠错/删除流程 | 文本草稿及支持消息应用中的消息 | CES 2026 为美国 EAP/英语；2026-03-31 官方称数周内向全部 Display 用户推出并扩至多种消息应用 |
| Teleprompter | 手机导入文字；腕带导航预设卡片。未证实任意文件读取或独立速度控制器 | 眼镜侧提示卡；源文本仍来自手机 | 2026-01-06 官方发布，`BACKGROUND`；有第三方实机但连续片缺失 |
| Garmin Unified Cabin | PoC 中腕带动作控制车载界面 | 车内系统控制状态 | 2026-01-06 OEM PoC，不是消费功能 |
| Utah 智能家居 / TetraSki | 研究原型读取腕带动作 | 家居控制状态 / 辅助滑雪装置控制 | 2026-01-06 研究合作，不是已开放功能 |
| CMU 双腕带游戏控制 | 研究装置读取双臂肌电并解码为游戏控制 | 赛车游戏转向/加速状态与研究数据 | 2026-05-18 窗口内研究演示，不是产品承诺 |

## §3 特性详解 ×N

### 3.1 Neural Handwriting — `PARTIAL`

- 进入：公开片从已在聊天/演示状态开始，未展示完整入口。
- 委托：食指在书封或桌面书写，腕带接收肌电；无需专用书写板。
- 过程：官方合成 HUD/display recording 展示逐字识别中间态。
- 接管：没有找到纠错或删除的实际画面。
- 产物：CES 演示呈现完成草稿、Send 控件、`Sent` 勾号和对方回复；2026-03 更新片只到完成草稿。
- 退出：没有退出状态。CES 片是 `BACKGROUND`；2026-03-31 片在窗口内但宽度仅 1080px。
- 差异点：它把“打字”改成对任意表面的低幅手写，但公开证据还没有覆盖可逆编辑。

CES 官方演示的六个交互帧（均为 BACKGROUND；HUD 为官方合成；场景外拍不计入六帧）：

| 05.0s 手指在书封书写 | 06.0s `Co` | 06.8s `Com` |
|---|---|---|
| ![书封手写](assets/neural-handwriting/03-surface-hand.png) | ![识别早期](assets/neural-handwriting/04-partial-word-start.png) | ![识别后续](assets/neural-handwriting/05-partial-word-late.png) |

| 08.0s 草稿与 Send | 09.2s Sent | 12.0s 对方回复 |
|---|---|---|
| ![完整草稿](assets/neural-handwriting/06-draft-and-send-control.png) | ![发送完成](assets/neural-handwriting/07-sent-confirmation.png) | ![收到回复](assets/neural-handwriting/09-reply.png) |

[CES 逐帧来源](assets/neural-handwriting/source.md) · [3 月更新的六帧与短片](assets/neural-handwriting-update/source.md) · [全部素材审阅](review.html)

### 3.2 Neural Band 手势集 — `PARTIAL`

- 进入：未见完整消费功能入口，只有手势准备姿态。
- 委托：FAQ 明确四向 swipe、食指 pinch = enter、中指 pinch = cancel，不支持 custom gestures。
- 过程：官方视频显示 pinch 动作与 EMG 轨迹；没有消费 HUD 命令结果。
- 接管：middle-finger pinch 的 cancel 映射由官方文字核定，但缺视觉结果；wrist roll 只保存为 Orion/EMG 概念段。
- 产物：手势产生控制事件，不产生独立文档；公开片未展示事件日志。
- 退出：可用 cancel 作为退出/撤销意图的映射依据，具体 UI 退出画面缺失。官方页没有误触阈值或误触率；步行 HUD 不能证明走路不误触。
- 差异点：腕带依靠肌电而不是摄像头看手，但公开消费映射比动作研究素材更窄。

| 动作组 | 准备 | 接触 / 后续 |
|---|---|---|
| 食指 pinch：官方动作与 EMG，未见消费 UI 结果 | ![食指准备](assets/gesture-set/01-index-pinch-start.png) | ![食指接触](assets/gesture-set/02-index-pinch-contact.png) |
| 中指 pinch：官方动作与 EMG，未见消费 UI 结果 | ![中指准备](assets/gesture-set/03-middle-pinch-start.png) | ![中指接触](assets/gesture-set/04-middle-pinch-contact.png) |
| wrist roll：旧概念演示，非当前消费映射验证 | ![滚腕起始](assets/gesture-set/05-wrist-roll-start-concept.png) | ![滚腕后续](assets/gesture-set/06-wrist-roll-end-concept.png) |

[动作、映射与步行背景的来源边界](assets/gesture-set/source.md)。

### 3.3 镜内 HUD — `PARTIAL`

- 进入：官方剪辑从矩形区域框直接出现开始；实际触发动作未展示。
- 委托：区域框的具体命令没有官方文字核定，不能命名为拍照/搜索/录制。
- 过程：区域框、消息与地图被剪辑为多个 HUD 状态。
- 接管：消息有快捷回复 chips，地图有卡片/扩展态；没有失败、返回或取消画面。
- 产物：单条消息状态、地点卡与地图；扩展地图只有网格、蓝色位置和红色 pin，没有可见路线。
- 退出：官方剪辑转场不能当真实消失时机；没有未剪辑退出证据。
- 差异点：Meta 把视觉反馈压到视野侧边和短卡片，但目前证据主要是官方合成 POV，不是透镜光学实拍。

![中性区域选择状态](assets/hud/01-region-selection-start.png)
![消息与快捷回复](assets/hud/04-message-reply.png)
![扩展地图状态](assets/hud/06-map-expanded.png)

### 3.4 Teleprompter — `PARTIAL`

- 进入：手机设置页可见 `Send to Meta RB Display`，是可审计的发送入口。
- 委托：用户选择 `Scroll vertically` 或 `Swipe horizontally`，并设置 `Text Size`；没有独立速度控制器。
- 过程：三个相机透镜取景时点显示不同文字卡，两个页码可读为 `11 of 14` 与 `2 of 14`。
- 接管：官方文字只证实用户用 Neural Band 按自己的节奏导航；单帧不能核定具体腕带动作。
- 产物：手机文本进入眼镜提词卡；源文本仍留在 Notes、Google Docs 或 Meta AI。
- 退出：没有结束/关闭画面。本地没有连续第三方视频，三个状态不能声称相邻或构成连续滚动。
- 差异点：控制权集中在腕带翻页/导航，眼镜只承载低信息量提示卡；“滚动方式”不等于“速度控制”。

![提词器设置与模式](assets/teleprompter/02-setup-modes-and-text-size.png)
![透镜取景状态 A](assets/teleprompter/03-through-lens-card-state-a.png)
![透镜取景状态 B，页码未可靠辨认](assets/teleprompter/04-through-lens-card-state-b.png)
![透镜取景状态 C](assets/teleprompter/05-through-lens-card-state-c.png)

### 3.5 腕带脱离眼镜 — `COMPLETE（研究/PoC 证据）`

- 进入：Garmin、Utah 与 CMU 都要先进入合作方的 PoC/研究装置，不是消费入口。
- 委托：腕带手势/肌电被交给车载、家居、TetraSki 或游戏系统；CMU 画面明确每只手臂一条带。
- 过程：CMU 连续片同时显示参与者、对照玩家、游戏画面、解码输出和 EMG 轨迹。
- 接管：这些装置仍由研究人员校准；公开片未给消费者通用配对/接管流程。
- 产物：产物是车载/家居状态、辅助设备控制或游戏转向/加速结果，不落入眼镜 HUD。
- 退出：没有研究任务退出流程。
- 差异点：它证明 Neural Band 的载体潜力超过眼镜，但当前全部是 PoC/研究，不能写成已开放的跨设备平台。

![Garmin Unified Cabin PoC](assets/beyond-glasses/01-garmin-unified-cabin.png)
![CMU 双腕带研究](assets/beyond-glasses/05-cass-two-bands.png)
![CMU 校准界面](assets/beyond-glasses/06-cass-calibration.png)
![CMU 指令标签、EMG 轨迹与游戏](assets/beyond-glasses/09-cass-active-play.png)

## §4 新硬件

官方硬件名称为 `Meta Ray-Ban Display` 和 `Meta Neural Band`。2025-09-17 发布，2025-09-30 在美国选定零售点开售；2026-01-06 Meta 因库存与候补名单暂停原计划的英国、法国、意大利和加拿大扩张。抓取日现行官方可用性页仍指向美国选定授权零售商与 Meta flagship stores。

厂商给出的设计理由是：显示器位于视野侧边、用于短交互且不常亮；腕带把肌肉活动转为命令并提供低幅控制。组合销售本身不能推出“语音失败”。硬件本体三张官方图达 1920px 或 4096px；CES 静态研究图部分只有 750px，已明确保留分辨率缺口。

## §5 拆分逻辑

| 轴 | Meta 的边界 |
|---|---|
| 工具装载 | 眼镜装载相机、音频、单目显示与 Meta AI；腕带装载肌电输入与触觉确认。开发者 Web App 只得到预定义手势，不能自定义 Neural Band 手势。 |
| 产物形态 | 眼镜侧输出短消息、提示卡、地图与识别文字；手机负责提词文本准备与发送到眼镜；研究 PoC 的结果落到汽车、家居、游戏或辅助设备。 |
| 爆炸半径 | 消费版受限于预定义输入、Display UI 与支持的消息应用；跨设备控制当前只见 PoC/研究，未开放为通用控制权限。 |
| 反馈回路 | HUD 提供文字/卡片/状态；腕带提供触觉确认。公开材料没有误触阈值、端到端延迟或失败恢复统计。 |
| 买单人 | 消费端是购买 Display+Band 的美国用户；汽车侧是 OEM PoC；Utah/CMU 是研究参与者与合作机构，不能合并成同一商业产品。 |

## §6 三个必答问题

1. **它把能力拆成了几块，边界画在哪？按能碰什么文件/权限/产物落哪。** 分成感知与 AI（眼镜）、视觉反馈（侧边 HUD）、动作输入与触觉确认（Neural Band）、文本准备/应用连接（手机）。消费 Web App 只能接收预定义四向 swipe、enter/cancel，不能定义自有 Neural Band 手势；提词文本由手机 Notes、Google Docs 或 Meta AI 复制后发送到眼镜；跨设备汽车、家居和辅助控制仍停在 PoC/研究。
2. **委托面更显式或更隐式？从必须打字→选中就懂→不用说也会做，在哪一档，最近半年往哪挪。** 当前落在“低幅显式动作”：用户仍要写、pinch、swipe 或腕带翻页，但可避免手机键盘和持续语音。近半年 Neural Handwriting 从 EAP 走向面向全部 Display 用户及更多消息应用，委托入口变得更随手；没有证据证明系统已到“不用说也会做”。
3. **硬件补软件哪块短板？落在载体。** Display 补手机“需要低头看屏”的反馈载体短板；Neural Band 补眼镜“公开说话不合适、手势不在摄像头视野或需要低幅精确控制”的输入载体短板。厂商没有将其表述为语音失败，研究用双腕带也不能反推消费产品当前需要双带。

## §7 素材与出处表

以下逐文件表与 [SOURCES.md](SOURCES.md) 同步；同源重复参考不增加独立流程帧数。

范围：仅 Meta。抓取时间统一为 2026-09-09（America/Toronto）。发布日期与抓取时间分开记录；2026-03-09 以前为 `BACKGROUND`，无法核定发布日期的在线官方页面为 `DATE_UNKNOWN`。本账本与 README §7 均逐文件列出正式素材；状态解释以各组 `source.md` 为准。

### 来源级别

- Meta Newsroom、Meta 产品页、Meta Developer FAQ：厂商一手。
- Garmin Newsroom、University of Utah：合作方一手，证明合作/研究，不证明 Meta 消费功能已经开放。
- VoodooDE VR English：第三方实机；视频含付费/联盟披露，只用于观察设置页与透镜取景。
- 官方宣传 POV/Display Recording：可证明厂商展示的界面状态，但不等同于透镜光学实拍或未剪辑时延测试。

### 页面清单

| 来源 | 发布 / 更新日期 | 抓取时间 | 用途 |
|---|---|---|---|
| https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 / 2025-09-30 | 2026-09-09 | 发布、硬件、HUD 与厂商设计理由；`BACKGROUND` |
| https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 手写、提词器、Garmin、智能家居、TetraSki；`BACKGROUND` |
| https://about.fb.com/br/news/2026/03/apresentando-uma-nova-linha-de-oculos-ray-ban-meta-desenvolvida-para-lentes-de-grau-e-conforto-o-dia-todo-alem-de-mais-cores-lentes-e-atualizacoes-de-software-em-toda-a-colecao/ | 2026-03-31 | 2026-09-09 | 窗口内 Neural Handwriting 更新 |
| https://about.fb.com/news/2026/05/meta-ai-wearables-changing-the-game-for-disabled-people/ | 2026-05-18 / 2026-05-22 | 2026-09-09 | 窗口内 CMU 双腕带研究 |
| https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | EMG 原理、动作视频与触觉/本地处理；`DATE_UNKNOWN` |
| https://developers.meta.com/wearables/faq/ | 未提供 | 2026-09-09 | Web App 六种手势映射与不可自定义边界；`DATE_UNKNOWN` |
| https://www.meta.com/ai-glasses/learn/communicating-across-the-globe/ | 未提供 | 2026-09-09 | 抓取日当前美国可用性 |
| https://www.garmin.com/en-US/newsroom/press-release/automotive/garmin-and-meta-announce-automotive-oem-proof-of-concept-with-garmin-unified-cabin-and-meta-neural-band/ | 2026-01-06 | 2026-09-09 | Garmin OEM PoC 合作方核验 |
| https://www.price.utah.edu/2026/01/06/u-of-u-and-meta-launch-research-to-enable-tetraski-and-smart-home-control-via-accessible-emg-wristband | 2026-01-06 | 2026-09-09 | Utah 研究说明与较高分辨率图片 |
| https://www.youtube.com/watch?v=wKCAFUscTao | 2026-02-04 | 2026-09-09 | 第三方提词器设置/透镜取景，`BACKGROUND` |

### 逐文件账本

| 特性 | 文件 | 完整来源 URL | 发布日期 | 抓取时间 | 页面/时间码 | 官方性 |
| --- | --- | --- | --- | --- | --- | --- |
| 新硬件 | [assets/hardware/01-display-band-pair.png](assets/hardware/01-display-band-pair.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 静态官方产品图 | Meta 官方，`BACKGROUND` |
| 新硬件 | [assets/hardware/02-display-front.png](assets/hardware/02-display-front.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 静态官方产品图 | Meta 官方，`BACKGROUND` |
| 新硬件 | [assets/hardware/03-display-sand.png](assets/hardware/03-display-sand.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 静态官方产品图 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/clip.mp4](assets/neural-handwriting/clip.mp4) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:00–00:18.069 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/01-context.png](assets/neural-handwriting/01-context.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:00.500 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/02-wearer.png](assets/neural-handwriting/02-wearer.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:02.500 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/03-surface-hand.png](assets/neural-handwriting/03-surface-hand.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:05.000 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/04-partial-word-start.png](assets/neural-handwriting/04-partial-word-start.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:06.000 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/05-partial-word-late.png](assets/neural-handwriting/05-partial-word-late.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:06.800 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/06-draft-and-send-control.png](assets/neural-handwriting/06-draft-and-send-control.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:08.000 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/07-sent-confirmation.png](assets/neural-handwriting/07-sent-confirmation.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:09.200 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/08-wearer-after-send.png](assets/neural-handwriting/08-wearer-after-send.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:10.300 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting/09-reply.png](assets/neural-handwriting/09-reply.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 00:12.000 | Meta 官方，`BACKGROUND` |
| Neural Handwriting | [assets/neural-handwriting-update/clip.mp4](assets/neural-handwriting-update/clip.mp4) | https://about.fb.com/br/news/2026/03/apresentando-uma-nova-linha-de-oculos-ray-ban-meta-desenvolvida-para-lentes-de-grau-e-conforto-o-dia-todo-alem-de-mais-cores-lentes-e-atualizacoes-de-software-em-toda-a-colecao/ | 2026-03-31 | 2026-09-09 | 00:00–00:05.833 | Meta 官方，窗口内 |
| Neural Handwriting | [assets/neural-handwriting-update/01-writing-start.png](assets/neural-handwriting-update/01-writing-start.png) | https://about.fb.com/br/news/2026/03/apresentando-uma-nova-linha-de-oculos-ray-ban-meta-desenvolvida-para-lentes-de-grau-e-conforto-o-dia-todo-alem-de-mais-cores-lentes-e-atualizacoes-de-software-em-toda-a-colecao/ | 2026-03-31 | 2026-09-09 | 00:00.200 | Meta 官方，窗口内 |
| Neural Handwriting | [assets/neural-handwriting-update/02-writing-yes.png](assets/neural-handwriting-update/02-writing-yes.png) | https://about.fb.com/br/news/2026/03/apresentando-uma-nova-linha-de-oculos-ray-ban-meta-desenvolvida-para-lentes-de-grau-e-conforto-o-dia-todo-alem-de-mais-cores-lentes-e-atualizacoes-de-software-em-toda-a-colecao/ | 2026-03-31 | 2026-09-09 | 00:01.000 | Meta 官方，窗口内 |
| Neural Handwriting | [assets/neural-handwriting-update/03-writing-sou.png](assets/neural-handwriting-update/03-writing-sou.png) | https://about.fb.com/br/news/2026/03/apresentando-uma-nova-linha-de-oculos-ray-ban-meta-desenvolvida-para-lentes-de-grau-e-conforto-o-dia-todo-alem-de-mais-cores-lentes-e-atualizacoes-de-software-em-toda-a-colecao/ | 2026-03-31 | 2026-09-09 | 00:02.000 | Meta 官方，窗口内 |
| Neural Handwriting | [assets/neural-handwriting-update/04-writing-sounds.png](assets/neural-handwriting-update/04-writing-sounds.png) | https://about.fb.com/br/news/2026/03/apresentando-uma-nova-linha-de-oculos-ray-ban-meta-desenvolvida-para-lentes-de-grau-e-conforto-o-dia-todo-alem-de-mais-cores-lentes-e-atualizacoes-de-software-em-toda-a-colecao/ | 2026-03-31 | 2026-09-09 | 00:03.000 | Meta 官方，窗口内 |
| Neural Handwriting | [assets/neural-handwriting-update/05-writing-fun.png](assets/neural-handwriting-update/05-writing-fun.png) | https://about.fb.com/br/news/2026/03/apresentando-uma-nova-linha-de-oculos-ray-ban-meta-desenvolvida-para-lentes-de-grau-e-conforto-o-dia-todo-alem-de-mais-cores-lentes-e-atualizacoes-de-software-em-toda-a-colecao/ | 2026-03-31 | 2026-09-09 | 00:04.000 | Meta 官方，窗口内 |
| Neural Handwriting | [assets/neural-handwriting-update/06-complete-message.png](assets/neural-handwriting-update/06-complete-message.png) | https://about.fb.com/br/news/2026/03/apresentando-uma-nova-linha-de-oculos-ray-ban-meta-desenvolvida-para-lentes-de-grau-e-conforto-o-dia-todo-alem-de-mais-cores-lentes-e-atualizacoes-de-software-em-toda-a-colecao/ | 2026-03-31 | 2026-09-09 | 00:05.200 | Meta 官方，窗口内 |
| 手势集 | [assets/gesture-set/clip-emg-signals.mp4](assets/gesture-set/clip-emg-signals.mp4) | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | 00:00–00:09.727 | Meta 官方，`DATE_UNKNOWN` |
| 手势集 | [assets/gesture-set/01-index-pinch-start.png](assets/gesture-set/01-index-pinch-start.png) | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | 00:00.500 | Meta 官方，`DATE_UNKNOWN` |
| 手势集 | [assets/gesture-set/02-index-pinch-contact.png](assets/gesture-set/02-index-pinch-contact.png) | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | 00:01.500 | Meta 官方，`DATE_UNKNOWN` |
| 手势集 | [assets/gesture-set/03-middle-pinch-start.png](assets/gesture-set/03-middle-pinch-start.png) | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | 00:04.500 | Meta 官方，`DATE_UNKNOWN` |
| 手势集 | [assets/gesture-set/04-middle-pinch-contact.png](assets/gesture-set/04-middle-pinch-contact.png) | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | 00:05.500 | Meta 官方，`DATE_UNKNOWN` |
| 手势集 | [assets/gesture-set/clip-wrist-roll-concept.mp4](assets/gesture-set/clip-wrist-roll-concept.mp4) | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | 00:00–00:08.488 | Meta 官方概念片，`DATE_UNKNOWN` |
| 手势集 | [assets/gesture-set/05-wrist-roll-start-concept.png](assets/gesture-set/05-wrist-roll-start-concept.png) | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | 00:01.000 | Meta 官方概念片，`DATE_UNKNOWN` |
| 手势集 | [assets/gesture-set/06-wrist-roll-end-concept.png](assets/gesture-set/06-wrist-roll-end-concept.png) | https://www.meta.com/en-gb/emerging-tech/emg-wearable-technology/ | 未提供 | 2026-09-09 | 00:03.000 | Meta 官方概念片，`DATE_UNKNOWN` |
| 手势集 | [assets/gesture-set/07-walking-hud-context.png](assets/gesture-set/07-walking-hud-context.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 00:09.000 | Meta 官方合成，`BACKGROUND` |
| 镜内 HUD | [assets/hud/clip.mp4](assets/hud/clip.mp4) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 00:00–00:12.000 | Meta 官方合成，`BACKGROUND` |
| 镜内 HUD | [assets/hud/01-region-selection-start.png](assets/hud/01-region-selection-start.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 00:00.500 | Meta 官方合成，`BACKGROUND` |
| 镜内 HUD | [assets/hud/02-region-selection-progress.png](assets/hud/02-region-selection-progress.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 00:02.500 | Meta 官方合成，`BACKGROUND` |
| 镜内 HUD | [assets/hud/03-region-selection-later.png](assets/hud/03-region-selection-later.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 00:05.000 | Meta 官方合成，`BACKGROUND` |
| 镜内 HUD | [assets/hud/04-message-reply.png](assets/hud/04-message-reply.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 00:07.000 | Meta 官方合成，`BACKGROUND` |
| 镜内 HUD | [assets/hud/05-map-card.png](assets/hud/05-map-card.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 00:09.000 | Meta 官方合成，`BACKGROUND` |
| 镜内 HUD | [assets/hud/06-map-expanded.png](assets/hud/06-map-expanded.png) | https://about.fb.com/news/2025/09/meta-ray-ban-display-ai-glasses-emg-wristband/ | 2025-09-17 | 2026-09-09 | 00:11.000 | Meta 官方合成，`BACKGROUND` |
| 提词器 | [assets/teleprompter/01-hud-card.png](assets/teleprompter/01-hud-card.png) | https://about.fb.com/br/wp-content/uploads/sites/11/2026/01/download-_3_.jpg | 2026-01-06 | 2026-09-09 | 官方静态图 | Meta 官方合成，`BACKGROUND` |
| 提词器 | [assets/teleprompter/02-setup-modes-and-text-size.png](assets/teleprompter/02-setup-modes-and-text-size.png) | https://www.youtube.com/watch?v=wKCAFUscTao | 2026-02-04 | 2026-09-09 | 00:01:47 | 第三方实机，`BACKGROUND` |
| 提词器 | [assets/teleprompter/03-through-lens-card-state-a.png](assets/teleprompter/03-through-lens-card-state-a.png) | https://www.youtube.com/watch?v=wKCAFUscTao | 2026-02-04 | 2026-09-09 | 00:03:39 | 第三方透镜取景，`BACKGROUND` |
| 提词器 | [assets/teleprompter/04-through-lens-card-state-b.png](assets/teleprompter/04-through-lens-card-state-b.png) | https://www.youtube.com/watch?v=wKCAFUscTao | 2026-02-04 | 2026-09-09 | 00:03:44 | 第三方透镜取景，`BACKGROUND` |
| 提词器 | [assets/teleprompter/05-through-lens-card-state-c.png](assets/teleprompter/05-through-lens-card-state-c.png) | https://www.youtube.com/watch?v=wKCAFUscTao | 2026-02-04 | 2026-09-09 | 00:03:49 | 第三方透镜取景，`BACKGROUND` |
| 脱离眼镜用途 | [assets/beyond-glasses/01-garmin-unified-cabin.png](assets/beyond-glasses/01-garmin-unified-cabin.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 官方静态图 | Meta 官方 PoC，`BACKGROUND` |
| 脱离眼镜用途 | [assets/beyond-glasses/02-smart-home-research.png](assets/beyond-glasses/02-smart-home-research.png) | https://about.fb.com/br/news/2026/01/ces-2026-novidades-no-meta-ray-ban-display-colaboracoes-com-a-industria-e-pesquisa-e-mais/ | 2026-01-06 | 2026-09-09 | 官方静态图 | Meta 官方研究，`BACKGROUND` |
| 脱离眼镜用途 | [assets/beyond-glasses/03-tetraski-research.png](assets/beyond-glasses/03-tetraski-research.png) | https://www.price.utah.edu/2026/01/06/u-of-u-and-meta-launch-research-to-enable-tetraski-and-smart-home-control-via-accessible-emg-wristband | 2026-01-06 | 2026-09-09 | 官方合作页静态图 | Utah 官方研究，`BACKGROUND` |
| 脱离眼镜用途 | [assets/beyond-glasses/04-smart-home-utah.png](assets/beyond-glasses/04-smart-home-utah.png) | https://www.price.utah.edu/2026/01/06/u-of-u-and-meta-launch-research-to-enable-tetraski-and-smart-home-control-via-accessible-emg-wristband | 2026-01-06 | 2026-09-09 | 官方合作页静态图 | Utah 官方研究，`BACKGROUND` |
| 脱离眼镜用途 | [assets/beyond-glasses/clip-cmu-two-band-research.mp4](assets/beyond-glasses/clip-cmu-two-band-research.mp4) | https://about.fb.com/news/2026/05/meta-ai-wearables-changing-the-game-for-disabled-people/ | 2026-05-18（05-22 更新） | 2026-09-09 | 原片 00:38–01:07；本地 29 秒 | Meta 官方研究，窗口内 |
| 脱离眼镜用途 | [assets/beyond-glasses/05-cass-two-bands.png](assets/beyond-glasses/05-cass-two-bands.png) | https://about.fb.com/news/2026/05/meta-ai-wearables-changing-the-game-for-disabled-people/ | 2026-05-18（05-22 更新） | 2026-09-09 | 原片 00:24.000 | Meta 官方研究，窗口内 |
| 脱离眼镜用途 | [assets/beyond-glasses/06-cass-calibration.png](assets/beyond-glasses/06-cass-calibration.png) | https://about.fb.com/news/2026/05/meta-ai-wearables-changing-the-game-for-disabled-people/ | 2026-05-18（05-22 更新） | 2026-09-09 | 原片 00:32.000 | Meta 官方研究，窗口内 |
| 脱离眼镜用途 | [assets/beyond-glasses/07-cass-game-comparison.png](assets/beyond-glasses/07-cass-game-comparison.png) | https://about.fb.com/news/2026/05/meta-ai-wearables-changing-the-game-for-disabled-people/ | 2026-05-18（05-22 更新） | 2026-09-09 | 原片 00:40.000 | Meta 官方研究，窗口内 |
| 脱离眼镜用途 | [assets/beyond-glasses/08-cass-decoded-output.png](assets/beyond-glasses/08-cass-decoded-output.png) | https://about.fb.com/news/2026/05/meta-ai-wearables-changing-the-game-for-disabled-people/ | 2026-05-18（05-22 更新） | 2026-09-09 | 原片 00:48.000 | Meta 官方研究，窗口内 |
| 脱离眼镜用途 | [assets/beyond-glasses/09-cass-active-play.png](assets/beyond-glasses/09-cass-active-play.png) | https://about.fb.com/news/2026/05/meta-ai-wearables-changing-the-game-for-disabled-people/ | 2026-05-18（05-22 更新） | 2026-09-09 | 原片 01:00.000 | Meta 官方研究，窗口内 |
| 脱离眼镜用途 | [assets/beyond-glasses/10-cass-hand-muscle-closeup.png](assets/beyond-glasses/10-cass-hand-muscle-closeup.png) | https://about.fb.com/news/2026/05/meta-ai-wearables-changing-the-game-for-disabled-people/ | 2026-05-18（05-22 更新） | 2026-09-09 | 原片 01:04.000 | Meta 官方研究，窗口内 |

### 未转化为正式证据的候选

- https://www.youtube.com/watch?v=PetsyCQd7Ts — 2026-06-01；YouTube 页面显示频道 verified badge 与 handle `@raybanmeta`，据此标品牌官方频道，不只依赖频道名。2026-09-09 连续看到 00:01:38；2026-09-10 按公开视频章节补审 Spotify、Calendar、AI Reminders、Widgets、Games、Recap，在 02:53、03:08、03:12、03:24、03:31、03:47、04:03 核对画面。相关剩余段没有补齐手写纠错/删除、提词器连续控制或误触边界，故不重复抽入正式素材。
- https://www.youtube.com/watch?v=gZ9IsB72nVk — Ray-Ban｜Meta 官方频道，2025-09-18，`BACKGROUND`；与发布页内容重叠。
- https://www.youtube.com/watch?v=X4T1r4lv7DY — Ray-Ban｜Meta 官方频道，2025-10-01，`BACKGROUND`；字幕已保存用于检索，未发现能补齐当前缺口的必要片段。
- https://www.youtube.com/watch?v=oEuzNcDAcTA — 联合推广视频，含 paid promotion；仅做候选检索，不作为正式一手事实。

### 待人填：观点 / 对我们的启发
