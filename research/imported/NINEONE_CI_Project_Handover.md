# NINEONE Sports · Technology — CI 项目交接文档

> 用于新对话继续 · 所有决策已锁定 · 直接从"待完成"部分继续

---

## 项目背景

**公司：** NINEONE Sports Ltd  
**全称：** NINEONE Sports · Technology  
**总部：** Auckland, New Zealand (North Shore)  
**扩张方向：** Australia → Asia-Pacific  
**网站：** nineonesports.co.nz  
**品牌口号：** *Powering the Play.* / 驱动每一场对决  

**业务架构（三层飞轮）：**
- **NINE ONE SPORTS** — 实体侧（球场供应链、场馆运营、社区、球员体验）
- **NINE ONE TECHNOLOGIES** — 科技侧（智能球拍、SaaS平台、AI数据）
- 两者共用母品牌 **NINEONE**，不是独立法律实体，是业务单元呈现

---

## 已完成的CI模块

### ✅ 1. 咨询公司CI研究
参考了4份真实文件：BCG NZ Agritech、BCG Enterprise Agents、McKinsey Technology Trends Outlook 2025、Accenture Destination Net Zero 2025

**提炼出7条CI铁律：**
1. 主色只有一个，极度克制
2. 封面 = 满版图 + 文字浮层
3. 数字永远放到极大
4. 每张图都有来源标注（Source:）
5. 结论永远先行
6. 每家都有"签名图形"
7. 页脚每页必有（品牌名 + 报告名 + 页码）

---

### ✅ 2. 色彩系统 v2.0（已锁定）

**核心变动：Orange 升主角，Teal 降级**

| Token | 色值 | 用途 |
|-------|------|------|
| `--color-primary` | `#1A2B3C` Deep Navy | 主背景，50–60% |
| `--color-accent` ★ | `#FF5500` Blaze Orange | 唯一主强调色，12–18%，所有CTA |
| `--color-accent-hi` | `#FF6B1A` | Orange hover状态 |
| `--color-accent-lo` | `#CC4400` | Orange pressed状态 |
| `--color-tech` | `#00FFD4` Neon Teal | 科技轨道专用，3–6% |
| `--color-tech-dim` | `#00CCA9` | Teal在白底页面的可读版本 |
| `--color-muted` | `#5A8090` | 来源标注、次要文字 |
| `--color-white` | `#FFFFFF` | 内容页背景 |

**双轨规则：**
- Sport Track（球员/C端）→ Orange 主导，Teal 不出现
- Tech Track（投资人/B2B）→ Orange 仍是主CTA，Teal 可在图表少量出现（上限6%）

---

### ✅ 3. 字体系统 Final v1.1（已锁定）

**四层字体，职责边界清晰：**

| 层级 | 字体 | 规格 | 用途 |
|------|------|------|------|
| **层级00 · 宣言** | DM Serif Display | Italic | **只给"Powering the Play."这一句，禁止扩展** |
| **层级01 · 展示标题** | Syne | 800/700/500 | 章节标题、大标题、数字展示 |
| **层级02 · 正文** | IBM Plex Sans | 500/400/300 | 所有叙述性内容 |
| **层级03 · 数据标注** | IBM Plex Mono | 500/400 | 来源标注、页脚、标签、Token |

**关键规则：**
- DM Serif Display 必须用 Italic，不可正体
- 不可把这个字体用在其他标题——稀缺性是签名感的来源
- 三套字体全部 Google Fonts 免费

---

### ✅ 4. Logo 系统

**N 标志（原始SVG路径，不可修改）：**
```html
<svg width="200" height="220" viewBox="0 0 200 220" fill="none">
  <rect x="10" y="10" width="70" height="200" fill="[COLOR]"/>
  <path d="M100,10 L100,210 L170,210 L170,80 Q170,10 100,10 Z" fill="[COLOR]"/>
</svg>
```

**已输出10个SVG文件：**
- `01` Teal on Navy — 主要版本
- `02` Orange on Navy — Sport Track
- `03` Navy on White — 报告/打印
- `04` White 透明底 — 叠加摄影
- `05` White on Orange — 活动物料
- `06` Teal 透明底 — 科技叠加
- `07` 横版锁定 Teal/Navy
- `08` 横版锁定 Navy/White
- `09` 横版锁定 Orange/Navy
- `10` 竖版锁定 Stacked

**Logo规则核心：**
- 安全间距 = Logo高度的25%
- 最小数字端：20px；最小印刷端：8mm
- 禁止：拉伸、旋转、镜像、描边、加阴影、非标准颜色

---

### ✅ 5. 文件模板系统

**PPT 16:9 · 6种母版：**
- PPT-01 封面 Sport Track（深色）
- PPT-02 封面 Tech Track（白底）
- PPT-03 章节切换页
- PPT-04 数据页（深色）
- PPT-05 正文内容页（白底）
- PPT-06 结尾页

**A4 报告 · 4种母版：**
- A4-01 报告封面
- A4-02 目录页
- A4-03 正文页（右侧Navy章节导航条）
- A4-04 数据专页（右侧Orange导航条）

---

### ✅ 6. BP投资人模板（天使/种子轮）

**12页精简版（路演用）：**
P01 Cover → P02 Problem → P03 Market → P04 Why Now → P05 Engine → P06 Traction → P07 Biz Model → P08 Moat → P09 Roadmap → **P10 The Ask** → P11 Team → P12 Close

**16页完整版（邮件发送用）= 12页 +：**
- P08 财务预测（3年收入，占位符）
- P09 单位经济（球场级别盈利逻辑）
- P13 顾问背书
- P15 FAQ（投资人必问5问）

**关键设计决策：Team页刻意放在Ask之后**——先让市场打动，再让人打动。

---

### ✅ 7. Logo规范手册 PPTX

9页PPTX，已交付：`NINEONE_Logo_Guidelines.pptx`

章节：The Mark → Colour Variants → Lockups → Clearspace & Sizing → Do & Don't → File Index → Close

---

## 🔄 进行中 · 未完成

### 文字标志（Wordmark）设计

**已确认方向：**
- 结构：方案E — NINE ONE 大字 + 彩色横线 + 子品牌名（**无竖线**）
- 颜色：SPORTS 用 Orange `#FF5500`，TECHNOLOGIES 用 Teal Dim `#00CCA9`
- 字体：正在测试，**Barlow Condensed 800** 是当前推荐（窄体、力量感）
- Syne 被否定：太扁宽

**结构示意：**
```
NINE ONE          ← Barlow Condensed 800，大字
—— SPORTS         ← 橙色横线(22px) + IBM Plex Mono，letter-spacing 0.22em

NINE ONE
—— TECHNOLOGIES   ← Teal横线 + IBM Plex Mono
```

**待完成：**
- [ ] 创始人确认最终字体（Barlow Condensed 推荐，还有Oswald/Anton/Bebas/IBM Plex可选）
- [ ] 输出最终SVG文件（SPORTS版 + TECHNOLOGIES版，各4个颜色变体）
- [ ] 更新Logo规范手册，加入Wordmark章节

---

## ❌ CI待启动模块

- [ ] **签名图形** — 飞轮图标准化（Trade→Technology→Sports，NINEONE的"签名图表"）
- [ ] **排版布局系统** — 页面网格、留白规则、章节结构
- [ ] **品牌语言补充** — 来源标注规范、页脚模板规范、双语（中英）使用规则

---

## 核心战略背景（给AI的上下文）

- 新西兰是**验证场**，不是终局市场
- 当前最重要任务：第一批Padel球场落地，形成**第一个真实样板项目**
- 球场业务是现金流入口，**真正长期资产是AI数据层、俱乐部关系、玩家关系**
- 融资策略：球场业务自我造血；AI/SaaS/硬件未来融资，优先找Smart Money
- **不是一家普通体育公司，是休闲运动的操作系统**

---

## 文件交付清单

| 文件 | 说明 |
|------|------|
| `nineone-color-system-v2.html` | 色彩系统v2.0完整规范 |
| `nineone-typography-final.html` | 字体系统Final v1.1 |
| `nineone-ci-audit.html` | CI诊断报告（对标7条铁律）|
| `nineone-templates.html` | PPT+A4通用模板系统 |
| `nineone-bp-template.html` | BP 12页精简版 |
| `nineone-bp-16page.html` | BP 16页完整版新增页面 |
| `nineone-logo-guidelines.html` | Logo规范手册HTML版 |
| `NINEONE_Logo_Guidelines.pptx` | Logo规范手册PPTX |
| `nineone-logos/01~10.svg` | 10个Logo SVG文件 |
| `nineone-wordmark-refined.html` | 文字标志方案E精修版（进行中）|

---

## 立即可继续的任务

新对话开始后，直接说：

> "继续Wordmark设计，我选择 [字体名]，请输出最终SVG文件"

或者：

> "开始签名图形设计，先做飞轮图的标准化"

---

*文档生成时间：2025 · NINEONE CI项目*
