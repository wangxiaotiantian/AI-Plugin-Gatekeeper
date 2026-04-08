# 🛡️ Plugin Gatekeeper | 插件守卫 (Dual-Language)

**Stop AI from burning tokens and over-analyzing.**
**防止 AI 插件乱烧 Token 和过度分析。**

---

## 💡 Why use this? / 为什么要用它？

AI plugins (like Superpowers) are often "too diligent"—re-reading the entire project for a simple fix or re-planning everything after a short break. This Skill gives the control back to you.

AI 插件往往“过度勤快”：修个小错别字也要遍历全项目，或者中断回来就要重读所有文档。本协议通过逻辑门控，把插件的“开关”重新握在用户手中。

---

## ✨ Key Features / 核心功能

### 1. Manual Authorization / 手动授权拦截
AI must ask for permission before performing heavy scans or global searches.
AI 执行重型扫描或全局搜索前必须先“请示”。

### 2. Zero-Latency Resume / 断点无感续传
Skip re-reading docs by using a 3-line `[Session_Anchor]`.
通过 3 行“会话锚点”跳过文档重读，直接进入开发/任务状态。

### 3. Precision Mode / 精准模式
Force AI to focus only on the reported error or the current file.
强制 AI 仅关注报错区域或当前文件，严禁“想太多”。

---

## 🚀 Quick Start / 快速开始

1. **Copy (复制)**: Copy the content of `config/gatekeeper.json`.
2. **Inject (注入)**: Paste it to your AI (Claude, Cursor, GPT-4) and say:
   > "Load this skill and follow the logic gate rules. / 加载此技能并遵守逻辑门控规则。"
3. **Control (控制)**:
   - Choose **Local-Only** to save tokens. (选“本地处理”来节省 Token)
   - Say **"Archive / 存档"** before you leave. (离开前说“存档”)
   - Paste the anchor and say **"Continue / 继续"** when you are back. (回来后贴上锚点说“继续”)

---

## 📂 Repository Structure / 仓库结构

- `/config/gatekeeper.json`: Machine-readable logic. (机器可读逻辑)
- `/docs/guide_en.md`: Detailed English guide.
- `/docs/guide_zh.md`: 详细中文指南。

---

## 📄 License
MIT License. Created for the Vibecoding community.


备注：我是因为修复 Bug 和断点重连太费 Token 才想做这个，实战中可以这样玩：
当 AI 弹出那句“⚠️ [Gatekeeper] 检测到重型任务...”时：
如果你很确定哪里错了，直接回：“3”（即本地处理，不许它搜索）。
如果你毫无头绪，回：“1”（让它搜一次）。
当你想下班时：
输入：“Archive / 存档”。
AI 会吐出 3 行文字（比如：已完成登录逻辑、正在调接口、下一步处理报错）。
重点：你自己把这 3 行存到记事本。
第二天回来时：
把那 3 行贴给 AI，说：“Resume / 继续”。
你会发现它不再废话，也不会去读 README，直接开始敲代码。

Note: I’m doing this because fixing bugs and re-establishing breakpoints wastes too many tokens.This trick works in actual use:
When the AI pops up the message:“⚠️ [Gatekeeper] Heavy task detected…”
If you’re sure exactly what’s wrong, just reply: 3
(Meaning: handle locally, do NOT search)
If you have no clue, reply: 1
(Meaning: let it search once)
When you’re done for the day:Type: Archive
The AI will output 3 lines (for example: Login logic completed, API integration in progress, Next step: fix errors).
Important: save these 3 lines in a notepad yourself.
When you come back the next day:Paste the 3 lines to the AI and say: Resume
You’ll find it skips all the extra talk, won’t re-read the README, and starts coding directly.
