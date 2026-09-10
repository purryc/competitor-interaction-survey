# OpenDesign CLI 素材账本

抓取日期：2026-09-09（America/Toronto）  
本机版本：Open Design v0.19.0；上游最新稳定版：0.22.1（2026-09-09）  
官方来源：[GitHub](https://github.com/nexu-io/open-design) · [v0.19.0 Release](https://github.com/nexu-io/open-design/releases/tag/open-design-v0.19.0)

| 文件 | 实际状态 | 来源/方法 | 证据边界 |
|---|---|---|---|
| `01-headless-cli-status.png` | daemon 状态 + MCP 安装帮助 | 原生 Terminal 中执行 v0.19.0 CLI | 证明 loopback daemon、CLI 入口和 agent 目标；未提交生成任务 |
| `02-clean-global-ui.png` | 桌面端全局 UI | Open Design v0.19.0 本机自测 | 证明桌面壳的入口视图；不证明 headless 产物 |
| `03-headless-artifact-complete.png` | project 创建后 artifact API 返回 complete | 自建实时 stdout 查看器，真实执行 CLI 子进程 | 输入是本地 HTML fixture；是文件通道测试，不是模型生成 |
| `clip.mp4` | daemon→project→artifact→files 的实时 stdout | Playwright 录制自建实时转录查看器 | 7.68 秒、1600×1000、H.264；非原生 Terminal UI，未预置/回放静态输出 |

视频验收：`ffprobe` 7.680 秒；完整解码无错误；1/4/7 秒代表帧已目检。原生 macOS 录屏只得到 0.0667 秒/1 帧，窗口与区域连续抓取被拒；失败文件保存在 `_work`，因此该项保留 PARTIAL。
