# 设计系统 token 素材账本

抓取日期：2026-09-09（America/Toronto）  
官方来源：[Open Design GitHub](https://github.com/nexu-io/open-design) · [v0.12.0 品牌设计系统文章](https://github.com/nexu-io/open-design/blob/main/apps/landing-page/app/content/blog/open-design-0-12-0-brand-backed-design-system.md)

| 文件 | 实际状态 | 来源/方法 | 证据边界 |
|---|---|---|---|
| `01-apple-token-picker.png` | 真实 Apple design-system picker 与色板 | Open Design v0.19.0 本机 UI | 证明可选 Apple system；不证明产物已经套用 |

同日 `GET /api/design-systems` 返回 151 项；Apple 条目 id=`apple`、status=`published`。同任务前后生成已真实尝试四条通道：Codex 缺 code-mode host，Claude 401，Hermes 401，AMR 余额不足；全部 0 artifact。定向官方检索只找到“切换后下次 render 使用新 token”的说明和不同示例，未找到同任务基线/应用后成对素材。故为 PARTIAL，不能用 picker 冒充应用结果。
