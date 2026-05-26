# Nine One Sports - Agent 系统关键决策记录

> 用途：记录关键决策的"为什么"，避免未来重复评估
> 维护：每次做出影响系统结构的决策时，记录在此

---

## 🎯 已做出的关键决策

### 决策 #001：选择 Claude Desktop 作为中枢
- 日期：2026-05-06
- 决策：把 Claude Desktop 作为整个 AI Agent 系统的指挥中心
- 替代方案考虑：Dify（无代码 Agent 平台）、n8n（自动化平台）
- 选择理由：
  - Mac 本地 app（符合 Nicholas 需求）
  - 零代码（符合 Nicholas 编程基础）
  - 内置 Connectors + Extensions 生态成熟
  - $20/月一站式
- 触发重新评估的条件：
  - Claude 出现重大功能倒退
  - Nicholas 团队规模扩大需要协作功能

### 决策 #002：跳过 ChatGPT Plus / Codex
- 日期：2026-05-06
- 决策：不订阅 ChatGPT Plus，不使用 Codex
- 替代方案考虑：双订阅（$40/月）、只用 Codex（$20/月）
- 选择理由：
  - Claude Desktop 已含 Claude Code，编程能力足够
  - 节省 $20/月
  - 避免在两个 AI 之间反复切换的认知成本
- 触发重新评估的条件：
  - 出现 Claude 完全做不了但 Codex 能做的具体任务
  - 不是因为"听说 Codex 不错"

### 决策 #003：接入 Figma MCP（决策已更新）
- 日期原版：2026-05-06 → 更新：2026-05-07
- 决策：完整接入 Figma MCP，同时覆盖 FigJam 白板和 Figma Design 设计稿
- 原决策：FigJam 直接使用，不配置 MCP
- 更新原因：
  - Nicholas 确认两个都在用（FigJam + Figma Design）
  - Figma Professional 付费账号，功能完整
  - MCP 配置成功，验收测试通过（能读取 Business Blueprint FigJam）
- 当前能力：
  - Claude 可直接读取 FigJam 白板内容并分析
  - Claude 可在 FigJam 里生成图表、流程图、思维导图
  - Claude 可读取 Figma Design 设计稿结构和组件
- 触发重新评估的条件：
  - Figma MCP 长期不稳定（频繁断线）
  - 实际使用中发现接入的 ROI 不够高

### 决策 #004：用本地 Markdown 替代 Confluence
- 日期：2026-05-06
- 决策：业务文档用本地 .md 文件，不使用 Confluence
- 选择理由：
  - 单人公司不需要团队协作功能
  - Claude 通过 Filesystem 可直接读写本地 Markdown
  - 数据归属在本地，不依赖 Atlassian 服务
  - 完全免费
- 触发重新评估的条件：
  - 团队规模 ≥ 5 人
  - 出现需要严格权限管理的协作场景

### 决策 #005：业务战略和 Agent 系统分两个 Project
- 日期：2026-05-06
- 决策：创建两个独立 Project
  - **Nine One Sports - AI Agent System**：工具、配置、工作流、提示词
  - **Nine One Sports - Business Strategy**：战略、市场、营销、产品、定价
- 选择理由：
  - 两类问题需要的 Claude 角色不同（系统架构师 vs 战略伙伴）
  - 避免 Instruction 互相干扰
  - 知识库内容可以分别维护
- 触发重新评估的条件：
  - 两个 Project 出现频繁交叉引用，不便管理时

---

## 🚫 反模式记录（已识别要避免的）

### 反模式 #1：配了工具但不用
- 描述：装了一个 Extension/Connector，但实际工作中从来不用
- 应对：每月复盘一次，发现就删除/停用

### 反模式 #2：同时搭多个工作流
- 描述：一次性配了 5 个工作流，结果都没用起来
- 应对：强制"一次只搭一个，用满 1 周再搭下一个"

### 反模式 #3：因为新潮就引入新工具
- 描述：看到新工具就想配，没问"现有工具能不能做"
- 应对：引入新工具前必须先验证现有工具不够用

### 反模式 #4：订阅前不算 ROI
- 描述：看到 $20/月觉得不贵，订了一堆
- 应对：每个新订阅必须明确"它能省下多少时间或赚多少钱"

### 反模式 #5：Project 之间内容混杂
- 描述：在 Agent System Project 里讨论业务战略，反之亦然
- 应对：发现话题跑偏时，主动重定向到对应 Project

---

## 📝 决策更新模板

每次做新决策时，按这个格式追加：

```
### 决策 #XXX：[一句话描述]
- 日期：YYYY-MM-DD
- 决策：具体做了什么
- 替代方案考虑：还有哪些选项
- 选择理由：
  - 理由 1
  - 理由 2
- 触发重新评估的条件：
  - 什么情况下应该重新考虑这个决策
```
