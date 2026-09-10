# OpenAI 实际检索记录

抓取日期：2026-09-09。仅记录已执行动作；可访问不等于已完成视觉验收。

| 检索/访问 | 站点/路径 | 实际结果 |
|---|---|---|
| `site:openai.com "ChatGPT Work" "2026"` | 官方搜索 | 找到 7 月 9 日发布页和发布说明 |
| `site:openai.com "GPT-Live"` | 官方搜索 | 找到 7 月 8 日发布页及 System Card |
| `site:openai.com "Atlas" agent mode` | 官方搜索 | 找到 Atlas 帮助说明 |
| `site:openai.com "Atlas" "August 9, 2026"` | 官方搜索 | 找到弃用迁移公告，计划 8 月 9 日停用 |
| `site:openai.com Jony Ive devices 2026`；`site:openai.com "Jony" "2026" "Sam"` | 官方搜索 | 本轮结果未给出可确认的新硬件发布信息，继续追查 |
| curl GPT-Live 官方发布页 | `_work/gpt-live.html` | 返回 9761 字节，需检查是否为访问挑战；浏览器替代路径继续 |
| 浏览器 Work 官方发布页 | https://openai.com/index/chatgpt-for-your-most-ambitious-work/ | 成功读取真实页面 DOM，含官方 PNG 和 Vimeo 1208302106 演示 |


| 官方 Learn 文档 get-started-with-work、browser、permission-modes、app | learn.chatgpt.com | 成功读取 Markdown；取得三个 CDN 视频与浏览器帮助图 |
| 官方 Work 101 教学 getting-started、plugins-and-skills | learn.chatgpt.com/training/walkthroughs/ | 视频下载成功；页面时长标签分别 8 / 9 min，媒体实际为 233.152 / 165.119 秒，按实际媒体时间码记录 |
| YouTube Work yRc5HcGJ-Cs | yt-dlp | 字幕返回 429，中断下载；Vimeo 替代宣传片已取得 |
| YouTube Atlas 8UWKxJbjriY | yt-dlp | 字幕和元数据成功，1080p 视频 403；换默认单流格式仍 403；继续官方 Vimeo 替代 |
| GPT-Live Vimeo 1208152658 | yt-dlp | 单片段 503 重试后整片取得；需完整解码校验 |
| GPT-Live Vimeo 1209991962 | 官方发布页 carousel | 详细 Improved Intelligence 演示取得；视觉初查为访谈和手持手机 |
| Work 产品页 Vimeo 1208185418 | openai.com/chatgpt-work/ | 成功下载；视觉上与发布页宣传片重复，不能作为第二套独立流程 |
| OpenAI Sam & Jony + MacRumors 2026-02-10 | 公开搜索 | 找到 2025 官方合作声明和 2027 延期报道；均早于时间窗，单列背景 |

## 补采：浏览器播放与语音原片审阅（2026-09-09）

- 官方 YouTube dB6pOolO7io、29SyCndnMZs 下载：yt-dlp 返回登录/机器人验证，日志 work-browser-demo-download.log / work-admin-download.log；这只证明下载路径失败。
- dB6pOolO7io 在 IAB 与 Chrome 均成功播放；Chrome 4K 曾出现 Unable to play media，改为1080p成功，读取原生1920×1080。已保存15、20、25、30、35秒实际视频图，进入任务、搜索、回答、批注入口、批注输入均直接查看；无接管点击证据。
- GPT-Live 官方 Vimeo image/startup/picker 已全部下载成功，不再重复下载。Whisper base 对 intelligence/launch/image 完成转写；逐段内容用于定位，不把自动文本当精确原话。intelligence54–103秒显示边规划边问答，但多数为人物镜头；image0–58秒显示两次选图与语音界面，待将有差异的状态独立出包。
- 官方云浏览器文档3张1600×900图已保存：登录交接、网站权限设置、浏览器数据。均未标独立日期；权限设置不是真正动作审批。
- GitHub官方仓库issues35860、43211无可用审批截图；35860明确未贴图，43211为用户个案文字报告，不充当产品实测。
- 硬件官方合作人像即使请求3840仍返回1000×750；原文件移至_work，不计正式素材，未放大冒充合格图。

- 官方管理员29SyCndnMZs已通过浏览器查看110/115/120/122/124/125秒附近：展示额度请求分析、语音指令和Approved and verified回执，未取得Allow once/Always allow/Deny动作卡；不计审批素材。
- Academy资源页浏览器可开，页面无视频iframe；站内搜索找到30:24官方回放（Posted Aug25），URL为 /public/clubs/work-users-ynjqu/videos/chatgpt-work-for-business-operations-teams-recording-2026-08-25。播放器iframe显示“抱歉，我们遇到了一点麻烦”；其实际Vimeo1221350415已尝试带官方referer下载，日志work-bizops-download.log。不是凭猜测构造视频地址。
- 浏览器17秒取得完整全局窗口；23.75秒工具过程仍Working。37秒为模糊缩放过渡，37.75秒已剪切至新任务，不能当批注提交回执或退出证据，均只留缓存。

- 定向搜索 ChatGPT Work Allow once screenshot / Always allow approval screenshot 找到两篇日本第一手上手，日期2026-08-15和08-31。三张公开原图宽1936或1920，实际显示任务暂停、目标网站、单次许可、拒绝，以及扩大网站许可二次确认。未访问付费段。Windows运行和待批准为同组2图，note为另一组1图，不凑同流程4帧。
- Windows完成回执与VS Code截图亦查看，回执含作者个人账户路径，未收正式包；未从作者描述推断拒绝后结果。
- 业务运营回放以实际官方嵌入页精确Referer重试，仍报TLS fingerprint错误，work-bizops-exact-referer.log保留。另一Activator课程已下载完毕，接续审阅实际演示。

## 最终候选处置

- Activator Labs 101 Vimeo1212158182全片3254.805秒下载完成，完整解码exit0；查看0–53分钟索引和33:00高清帧，实践章节为流程设计幻灯片，未充当产品UI。
- Work keynote Wq45rvPGNHs完整字幕导出为work-keynote-transcript.txt；6:40/6:45委托和处理中界面，6:50切回人物，无审批卡。
- Atlas旧直播8UWKxJbjriY字幕16:14–16:25为点击Continue把任务交给agent，未定位用户收回控制。视频此前403，官方Vimeo替代已取得对应交接背景图。
- Sarah文章原HTML403，浏览器可读；iframe延迟地址0xSAedqRT88，直接embed153，主播放页成功。完整8:27字幕已保存；授权段为连接Google Calendar OAuth，后续任务为询问技能迁移及能力，没有定位同句多个@与动作拒绝结果。
- GPT-Live三段对话与独立动画审阅完成；图片序列5帧和独立行程近景入包。短片重新截为目标29.8秒，最终29.821458秒，解码exit0。

本轮逐项处置结论与恢复条件见EVIDENCE-DISPOSITION.md；早期“继续/待审”记录保留为历史进度，最终状态以STATUS.md为准。
