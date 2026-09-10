# OpenWork 桌面端素材账本

抓取日期：2026-09-09（America/Toronto）  
产品：OpenWork v0.18.44，官方 Apple Silicon DMG  
官方来源：[GitHub 仓库](https://github.com/different-ai/openwork) · [v0.18.44 Release](https://github.com/different-ai/openwork/releases/tag/v0.18.44)

| 文件 | 实际状态 | 来源/方法 | 证据边界 |
|---|---|---|---|
| `01-entry-global-ui.png` | 新会话全局 UI | 官方 DMG，本机自测 | 真实产品空态；非官网宣传图 |
| `02-delegate-ready.png` | 三行文件任务已输入，尚未执行 | `--blank-slate` 隔离 profile | 证明委托内容，不证明执行成功 |
| `03-running.png` | `Working 6s` 与 `Wrote` | 同一隔离成功运行 | 过程可见，但不包含人工审批 |
| `04-success-result.png` | `Wrote`、`Read` 与完成回复 | 同一隔离成功运行 | 证明 agent 报告完成；还需产物视图交叉核验 |
| `05-artifact-preview.png` | OpenWork 内置文件面板显示三行内容 | 同一隔离成功运行 | 证明产物在产品内可读 |
| `06-exit-new-session.png` | 返回新会话，旧会话留在侧栏 | 同一隔离成功运行 | 作为退出/收尾状态 |
| `04-failure-no-result.png` | `task accepted, no result arrived · Resume` | 另一次真实失败运行 | 只证明失败后的 Resume 接管入口；不能接到成功链上 |
| `05-artifact-result.png` | MacDown 打开生成文件 | 失败前正常 profile 运行的本地产物 | 外部查看器补充，不是 OpenWork UI；不用于证明同一隔离成功链 |

隔离核验：renderer 的 `user-data` 与 HOME 均位于系统临时 `openwork-test-profile-*`；生成文件副本保存在 `_work/openwork-q3-openwork-test.md`。未演示人工编辑后继续 agent，也未取得连续原生录屏，因此 coverage 为 PARTIAL。
