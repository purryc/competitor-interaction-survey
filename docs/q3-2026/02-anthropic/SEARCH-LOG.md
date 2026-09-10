# Anthropic 检索与采集日志

抓取日期：2026-09-09。只记录本品牌。

## 官方名称、日期与状态核实

| 检索词 / 页面 | 站点 | 实际结果 |
|---|---|---|
| `Claude Design Anthropic Labs April 17 2026` | anthropic.com/news、YouTube Claude | 找到官方发布文与 1:21 官方视频；确认 2026-04-17、research preview、Pro/Max/Team/Enterprise，以及 Comment、Edit text、sliders/knobs、导出和 Code handoff。 |
| `Claude Tag Slack June 23 2026` | anthropic.com/news、YouTube Claude | 找到 2026-06-23 官方发布文与 2:25 官方视频；确认 Team/Enterprise Slack beta、管理员访问范围/预算/日志。 |
| `Cowork web desktop mobile July 7 2026` | support.claude.com release notes / surface guide | Release notes 明确 2026-07-07 加入 Web/Mobile；当前 surface guide 说明同一 session 可跨端 start/steer/review，Web/Mobile 的本地 computer use 依赖 Desktop。 |
| `Cowork Dispatch tasks from anywhere` | support.claude.com、YouTube Claude | 找到 2026-03-17 官方 40 秒视频与 2026-08-31 更新的帮助页。视频实际顺序是手机委托→桌面执行/产物→手机结果/追问。 |
| `Cowork folder permission delete approval asks before acting` | support.claude.com、anthropic.com/engineering、YouTube | 当前帮助页确认 Manual（旧 Ask before acting）和永久删除前显式 Allow；工程文确认 workspace folder 与 read-only/read-write/read-write-no-delete。官方当前页面未提供相应 UI 视频。 |
| `Claude Code Skills Subagents Agent Teams UI` | code.claude.com/docs、anthropic.com/webinars、resources.anthropic.com | 找到当前官方文档与 2026-03-24 官方高级模式讲义；p.13 是 Subagents 结构说明，p.14 含 `4 agents launched` 终端截图。 |
| `Anthropic Model Hardware Standard August 27 2026` | anthropic.com/news | 找到 2026-08-27 官方 MHS research preview 与原始图片；确认其为共享设备控制规范，不是 Anthropic 自有硬件。 |
| `Anthropic why no hardware / not building hardware / device strategy` | anthropic.com/news、官方新闻/产品页定向检索 | 未找到 Anthropic 对“为什么不做自有硬件”的明确公开表态；不从产品分发渠道反推动机。 |

## 媒体取得与视觉审阅

| 候选 | 取得方式 | 视觉检查结果 | 正式处置 |
|---|---|---|---|
| Design 官方视频 `t_LBECIQQqs` | 使用用户现有已登录 Chrome 会话供 `yt-dlp` 读取公开 YouTube，不保存账号凭据 | 完整下载 1920×1080；全片 contact sheet 与 22/24/42/48–71 秒候选逐帧复核；全量解码通过 | Comment 与直接文字编辑可形成连续帧；24/42 秒看见真实滑杆，但未见拖动前后，因此 Design 收敛为 PARTIAL |
| Design 自动字幕 / 浏览器 transcript | YouTube 自动字幕与浏览器导出 | 时间轴出现 2:56–4:05，而原片只有 1:22；内容是重复 `Woo!`，与画面不符 | 保留在 `_work` 作失败证据，不用于时间码或事实 |
| Design 发布页 hero | 官方 CDN，2876×1614 | 是完整 Design UI，含 Tweaks/Comment/Edit/Knobs | 作为候选缓存；正式帧优先使用视频中可定位时间码的 UI |
| Dispatch 官方视频 `fVIV-L49eBs` | 同上 | 完整下载 1920×1080；2 秒采样 contact sheet 实际看见手机→桌面→手机；全量解码通过 | 9 帧 + 29.5 秒正式 clip；因时序不符合任务书指定顺序，标 PARTIAL |
| Dispatch 帮助页两张图 | 官方 CDN | 原图分别约 1024×1318、1144×1246，宽度低于 1280；内容是 Dispatch setup / keep-running 设置 | 保留 `_work`，不放正式 assets，不放大凑规格 |
| Cowork 官方 webinar `zfWfczd6keE` | 同上 | 完整视频已定位并截取 24:15–24:45 文件夹段、25:10–25:40 过程段；代表 contact sheet 已目检；分段全量解码通过 | 文件夹选择器与过程可见性帧保留，但发布日期 2026-02-09，全部标背景 |
| Cowork 权限第三方视频 `WWpJeiXgZpo` | 公开视频下载 | 1:35–2:05 看到 folder access request；3:04–3:34 看到 scope warning，按钮原文为 `Cancel / Always allow / Allow`；3:45–4:44 另行完整审阅：用户要求清空 `project_plan.txt`，4:23 发送，4:32 完成，4:42 文件为空，全程没有再次审批，文件本身仍存在 | 保留作者标记，5 帧 + 29.5 秒正式 clip；后段属于清空文件内容而非永久删除文件，不能作为动作级删除审批；`_work` 保留两段补充审阅视频与 contact sheet |
| Claude App 本机自测 | 打开本机 Claude Desktop | 当前被 Cloudflare Turnstile 挡住；未点击、未代做验证码 | 自测不可继续；缺口转用官方帮助、公开视频和第三方上手，STATUS 明确阻塞条件 |
| Claude Code Skills 第三方视频 `epZy_NajGnA` | 公开视频下载 | 完整下载 1920×1080；7:35–8:20 每秒 contact sheet 与三张候选原图已目检；看见 `/` 列表、`/skill-creator`、`/skills` 项目/用户技能面板 | 3 帧 + 29.5 秒 clip；明确第三方 |
| Claude Code 官方高级模式 PDF | 官方资源 PDF | `pdfinfo` 20 页、1600×900 渲染；20 页 contact sheet 及 p.13/p.14 原图已目检 | p.13 标“官方讲义示意”，p.14 标“官方终端截图”；不把 p.13 当 live UI |
| Claude Tag 官方视频 `VojDzHaciKQ` | 公开视频下载 | 完整下载 1920×1080；全片 contact sheet 与 36/44/52/64/80/92 秒候选已目检；全量解码通过 | 6 帧 + 29.53 秒 clip，作为产品矩阵/替代载体补充，不计六项特性 |
| Tag 发布页 hero / YouTube thumbnail | 官方页面 | 前者是 `@Claude` 宣传画面，后者是标题图，不是产品 UI | 保留 `_work`，不计正式 UI |
| MHS 官方页前三张原图 | 官方 CDN | 1999px 宽；分别是统一编排图、实验室实拍、三类实验室架构对比；已做 contact sheet 目检 | 3 张进入 `hardware-strategy`；边界写为共享规范/现有设备 |

## 失败与未取得项

- 没有取得 Cowork “永久删除某个文件”时的动作级审批弹窗；帮助页文字确认不能替代 UI。第三方视频 3:45–4:44 已排除：它清空文件内容但保留文件，且在已授予的文件夹权限下无新弹窗。
- 没有取得任务书指定的桌面起任务→手机看进度→回桌面取产物的准确顺序；官方 Dispatch 视频是反向起点。
- 没有取得 2026-03-09 后同等清晰的 Cowork 计划→日志→文件变更→插话→产物→退出连续官方片段。
- Design 官方短片没有显示滑杆实际拖动；只见静态滑杆。Knobs 数值字段没有被当作滑杆。
- Design→Code 没有显示 Claude Code 接收端和执行结果。
- Claude Code 多代理来源仍混合官方讲义与第三方实录；没有一条连续官方 live UI 覆盖 Skills、Subagents、Agent Teams 的管理和结束。
- Anthropic 为什么不做自有硬件：未找到官方说明。MHS 不作为自有硬件证据。

## 文件验收

- 正式 PNG/JPG 全部宽度 ≥1280px；未放大低分辨率 Dispatch 帮助图。
- 7 个正式 `clip.mp4` 均为 H.264/AAC，时长 7.50–29.53 秒，已逐个 `ffprobe` 并全量解码，无报错。
- 所有正式素材均在对应目录有 `source.md`；逐文件总表见 `SOURCES.md`。
