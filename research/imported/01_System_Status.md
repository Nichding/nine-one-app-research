# Nine One Sports - AI Agent System Status

> 最后更新：2026-05-06
> 维护者：Nicholas
> 用途：让 Claude 立即了解当前 Agent 系统的完整状态

---

## 📊 当前订阅与成本

| 服务 | 订阅 | 月成本 | 用途 |
|---|---|---|---|
| Claude Pro | ✅ 已订阅 | $20 | 核心中枢 |
| ChatGPT Plus | ❌ 已跳过 | $0 | 决策：功能重叠 |
| Figma | 付费版 | 已有 | FigJam 白板 |
| Microsoft 365 | 工作账号 | 已有 | 邮件、文档、Teams |
| NotebookLM | 免费 | $0 | 业务知识库 |
| **AI 工具总成本** | | **$20/月** | |

---

## 🟢 已完成配置

### Claude Desktop（核心中枢）
- 安装：✅
- 登录账号：Nicholas 的 Anthropic 账号
- 订阅：Pro
- 平台：Mac (Apple Silicon M2)

### Filesystem Extension
- 安装：✅
- 授权文件夹：`~/Desktop/Nine One Sports/`
- 验证测试：✅ 已通过（能列出文件、读写正常）

### Microsoft 365 Connector
- 连接：✅
- 账号类型：工作账号（Microsoft Entra）
- 解锁能力：
  - Outlook 邮件（读取）
  - Outlook 日历
  - OneDrive 文件
  - SharePoint 文档
  - Teams 聊天和会议
- 验证测试：✅ 已通过（邮件读取成功）

### NotebookLM 业务知识库
- 名称：`Nine One Sports - Padel Business Knowledge`
- 当前 sources：3 个（行业基础资料）
- 验证测试：✅ 已通过（能基于资料回答问题，引用清晰）
- 访问方式：notebooklm.google.com（独立工具，不直连 Claude）

### Claude Code
- 项目文件夹：`~/Desktop/Nine One Sports/99_Code_Projects/`
- 模式：Local
- 默认模型：Sonnet 4.6
- 状态：已配置但还未实际使用

### FigJam
- 决策：直接使用，不接 MCP
- 替代方案：AI 生成结构化内容 → 手动粘贴到 FigJam
- 用途：白板、头脑风暴、流程图

---

## 🔴 已主动跳过（带理由）

### ChatGPT Plus / OpenAI Codex
- 理由：跟 Claude Pro 功能重叠 90%
- 节省：$20/月（年节省 $240）
- 重新评估时机：如果遇到 Claude 完全做不了但 Codex 能做的事

### Figma Design MCP Server
- 理由：Nicholas 主要用 FigJam 不是 Figma Design
- MCP 主要服务"设计稿转代码"，需求不匹配
- 重新评估时机：如果 Nicholas 开始用 Figma Design 做 UI 设计

### Confluence
- 理由：单人公司无需团队协作功能
- 替代方案：本地 Markdown + Filesystem Extension（Claude 直接读写）
- 重新评估时机：团队规模 > 5 人时

---

## 🟡 已规划但未搭建的工作流

按优先级排序：

| 优先级 | 工作流 | 涉及工具 | 预计搭建时间 |
|---|---|---|---|
| P0 | 邮件助手 | Outlook + NotebookLM + Claude | 30 分钟 |
| P0 | 财务/订单 Excel 自动化 | Cowork + Filesystem | 30 分钟 |
| P1 | 产品描述生成器 | NotebookLM + Claude | 20 分钟 |
| P1 | 竞品监控（每周） | Web Search + Claude | 15 分钟 |
| P2 | 独立站建站 | Claude Code + Filesystem | 多天 |

---

## 🧠 已建立的核心心智模型

### 双脑协作
NotebookLM（知识大脑）↔ Nicholas（翻译官）↔ Claude Desktop（执行大脑）

两个 AI 不会自动通信，Nicholas 是协调者。

### 知识分层
- 第 1 层：NotebookLM —— 长期稳定知识、行业资料、品牌指南
- 第 2 层：本地 Markdown —— 业务文档、产品规格、SOP（可读写）
- 第 3 层：OneDrive —— 合同、发票、原始 Excel
- 第 4 层：Confluence —— 暂不使用

### 工具选择原则
- 零代码优先
- 一次搭一个，用了再搭下一个
- 主动节省成本（功能重叠的订阅默认跳过）

---

## 📁 当前文件夹结构

```
~/Desktop/Nine One Sports/
├── 01_Orders/              （订单数据）
├── 02_Finance/             （财务报表）
├── 03_Suppliers/           （供应商发票）
├── 04_Reports/             （Claude 生成的报告）
├── 05_Products/            （产品资料）
├── 99_Code_Projects/       （Claude Code 项目）
└── [建议添加] 00_Knowledge_Base/（本地 Markdown 知识库）
```
