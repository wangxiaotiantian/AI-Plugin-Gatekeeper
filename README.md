# 🛡️ Plugin Gatekeeper | 插件守卫（Cursor / Claude 通用）

**Stop AI from burning tokens and over-analyzing.**  
**防止 AI 插件乱烧 Token、过度分析、无意义全仓扫描。**

---

## 这是什么？

这是一个“**对话协议型**”的 Gatekeeper Skill：通过一份机器可读的 `config/gatekeeper.json`，把重型动作（全仓搜索、遍历大量文件、反复重读文档等）变成**必须先授权**的流程。

> 重要：它不会自动“魔法生效”。你必须把 `config/gatekeeper.json` **作为强约束协议**注入到对话（推荐：新开会话时置顶粘贴），或在你的工作流里固定加载。

---

## 快速开始（推荐）

1. 打开 `config/gatekeeper.json`
2. 新开对话，把文件内容**完整粘贴**到第一条消息，并追加一句：

> “从现在开始严格按 `gatekeeper.json` 的 `protocol` 执行；任何冲突以 `gatekeeper.json` 为准。”

3. 当你看到模型准备做重型动作时，它必须先输出 Gatekeeper 菜单并等待你选择 `1/2/3`（或命令别名）。

---

## 你将得到什么？

- **手动授权拦截**：重型动作前必须询问
- **断点续传锚点**：可校验的 `Session_Anchor`，减少“回来又重读一遍”
- **精准模式**：Local-Only 下明确禁止全仓扫描等行为

---

## 文档

- 中文：`docs/guide_zh.md`
- English：`docs/guide_en.md`

---

## License

MIT
