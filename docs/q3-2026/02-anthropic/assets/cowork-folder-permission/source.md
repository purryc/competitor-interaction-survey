# Cowork 文件夹授权｜素材来源

状态：PARTIAL。已取得文件夹访问请求、范围警告、`Allow` / `Always allow`，以及背景期官方文件夹选择器；未取得“实际永久删除动作发生时”的专门审批弹窗。

## 正式素材

| 文件 | 实际画面状态 | 来源与时间码 | 日期 / 属性 |
|---|---|---|---|
| `01-folder-access-request.png` | Cowork 在任务中请求访问本地文件夹，显示 `Deny all / Allow` | [HardReset_Pro 实录](https://www.youtube.com/watch?v=WWpJeiXgZpo) `00:01:53` | 2026-05-06 / 第三方 |
| `02-folder-access-options.png` | 同一请求保持在屏幕，路径与两种决策可见 | 同上 `00:01:57` | 2026-05-06 / 第三方 |
| `03-folder-scope-warning.png` | `Allow Claude to change files in “Claude”?` 范围警告出现 | 同上 `00:03:07` | 2026-05-06 / 第三方 |
| `04-allow-and-always-allow.png` | 弹窗原文列出 `Cancel / Always allow / Allow` | 同上 `00:03:18` | 2026-05-06 / 第三方 |
| `05-folder-warning-late-state.png` | 同一范围警告的后段状态；弹窗仍未关闭 | 同上 `00:03:28` | 2026-05-06 / 第三方 |
| `06-background-folder-picker-entry.png` | Cowork 从任务界面进入选择文件夹 | [Anthropic 官方 Cowork webinar](https://www.youtube.com/watch?v=zfWfczd6keE) `00:24:23` | 2026-02-09 / 官方 / 背景 |
| `07-background-folder-picker.png` | macOS 文件夹选择器打开 | 同上 `00:24:25` | 2026-02-09 / 官方 / 背景 |
| `08-background-folder-selected.png` | 文件夹选择器中目标目录被选中 | 同上 `00:24:27` | 2026-02-09 / 官方 / 背景 |
| `09-background-folder-return.png` | 选择后返回 Cowork 任务界面 | 同上 `00:24:29` | 2026-02-09 / 官方 / 背景 |
| `clip.mp4` | 范围警告与 `Always allow / Allow` 选择 | 第三方实录 `00:03:04–00:03:33.5` | 2026-05-06 / 第三方 |

## 当前事实补强

- [Get started with Claude Cowork](https://support.claude.com/en/articles/13345190-get-started-with-claude-cowork)：当前 Cowork 有 Manual（旧称 Ask before acting）、Auto、Skip 等模式；永久删除前始终要求显式 Allow。
- [How we contain Claude](https://www.anthropic.com/engineering/how-we-contain-claude)：2026-05-25 官方说明用户选择 workspace folder，并区分 read-only、read-write、read-write-no-delete。

## 证据边界

第三方范围警告提到 Claude 可读取、编辑、永久删除和分享所选文件夹内容，但它是“授予文件夹权限”的警告，不能当作“删除某个文件时”的动作级审批。弹窗没有 `Allow once` 字样；如将右侧 `Allow` 理解为只处理当前请求，那是语义解释，必须与按钮原文分开。

同一视频 `00:03:45–00:04:44` 已另行完整审阅：用户输入 `Delete everything from project_plan.txt. Simply make this file empty`，`00:04:23` 发送；Claude 没有再弹审批，`00:04:32` 回复文件已清空，`00:04:42` 文件内容为空。这个动作是清空文件内容，文件本身仍存在，所以不能作为“永久删除文件”的审批证据；它只说明先前文件夹权限下的写操作可继续执行。视频左下角原作者标记已保留；没有裁掉或改造成官方素材。
