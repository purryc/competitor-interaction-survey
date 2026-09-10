# 社区分歧素材账本

抓取日期：2026-09-09（America/Toronto）。页面为真实 GitHub issue，浏览器顶栏裁去以避免其他标签信息；issue 标题、仓库、状态与正文边界保留。

| 文件 | Issue | 状态与选择理由 | 来源 |
|---|---|---|---|
| `01-opendesign-login-required-6599.png` | Open Design #6599 Mandatory Login | 2026-08-07 创建、2026-08-31 关闭；48 条评论，issue 顶层 27 reactions（23 👍、4 👀）；围绕本地优先与强制登录的产品原则冲突 | https://github.com/nexu-io/open-design/issues/6599 |
| `02-opendesign-byok-local-2986.png` | Open Design #2986 BYOK private IP | 2026-05-26 创建、截至核验日 open；40 条评论、顶层 2 👀、`priority:p1`；内部 LLM 代理/私网地址被阻断，直接影响企业本地部署 | https://github.com/nexu-io/open-design/issues/2986 |
| `03-openwork-summary-loop-1103.png` | OpenWork #1103 session summary loop | 2026-03-22 创建、2026-03-26 关闭；22 条评论、顶层 0 reactions；普通问候也触发自动摘要循环，导致会话无法正常推进，属于可靠性与接管问题 | https://github.com/different-ai/openwork/issues/1103 |

选取范围是两个项目截至 2026-09-09 的公开 GitHub issues；先按评论量/反应筛高互动候选，再按权限、隐私/本地性、兼容与恢复的交互影响定稿三条，并非全量统计或严格数学排名。截图里的 issue 标题与正文是用户报告，不自动等于当前产品事实。closed 不表示争议从未发生；#6599 随 v0.21.1 的登录调整关闭，#1103 已关闭，#2986 截至抓取日仍 open。
