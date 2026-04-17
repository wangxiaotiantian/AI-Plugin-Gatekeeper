# Plugin Gatekeeper 使用指南（中文）

## 1. 它解决什么问题？

- 防止助手“太勤快”：小问题也全仓搜索、反复重读文档、重新做大计划，导致 token 浪费。

## 2. 怎么让它真的生效？

Gatekeeper 是**协议**，不是自动补丁。请在新会话第一条消息：

1) 粘贴完整的 `config/gatekeeper.json`  
2) 追加一句强约束：  
   “从现在开始严格按 `gatekeeper.json` 的 `protocol` 执行。”

## 3. 交互方式（菜单 / 命令式）

当助手准备做重型动作时，它必须先输出以 `⚠️ [Gatekeeper]` 开头的菜单，然后停止等待你选择：

- `1` / `SINGLE` / `GK:1`：单次授权  
- `2` / `SESSION` / `GK:2`：全程授权（直到 `ARCHIVE/FINISH/存档/完成`）  
- `3` / `LOCAL` / `GK:3`：本地处理（禁止全仓搜索/广遍历）

你回复后，它下一条消息必须输出模式标签：

- `[GATEKEEPER_MODE=SINGLE_USE]`
- `[GATEKEEPER_MODE=SESSION_AUTHORIZED]`
- `[GATEKEEPER_MODE=LOCAL_ONLY]`

## 4. 存档与续传（Session Anchor）

下班前对助手说：`ARCHIVE` 或 `存档`  
助手必须输出**恰好 3 行**，且第 1 行必须是：

`[Session_Anchor:Universal_Plugin_Gatekeeper_Dual v2.0.0]`

第二天把 3 行原样粘贴，并说：`RESUME` 或 `继续`。

## 5. 常见问题

### Q：我没看到 Gatekeeper 菜单？

通常是你没有把 JSON 当“强约束”置顶加载。请新开会话重试，并明确要求“必须遵守 protocol.hard_stop_rule”。

### Q：我想更省 token？

优先使用 `LOCAL_ONLY`，并只粘贴报错栈/相关代码片段给助手。
