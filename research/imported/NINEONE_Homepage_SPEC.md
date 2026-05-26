# NINE ONE — Homepage Spec
**Version:** 1.0  
**Page:** Homepage (`/`)  
**Based on:** Homepage_mockup.png  
**Tech Stack:** Next.js 14 · Tailwind CSS · Framer Motion · Vercel  

---

## 设计 Token

### 色彩

```css
--color-black:        #0A0A0A;   /* 主背景 */
--color-black-2:      #0D0D0B;   /* 次级背景 */
--color-white:        #F5F5F3;   /* 主文字 */
--color-graphite:     #8A8A8A;   /* 次要文字 */
--color-lime:         #C7F000;   /* 主强调色：CTA / 标签 / 句点 */
--color-lime-hover:   #D8FF4D;   /* Hover 状态 */
--color-blue:         #2D7DFF;   /* Tech 强调色 */
--color-blue-hover:   #4B9CFF;   /* Tech Hover */
```

### 字体

```
Primary (全站正文 / UI):  Satoshi — 400 / 500 / 700 / 900
Accent (Hero / 标题):     Josefin Sans — 300 / 400 / 600
```

引入方式：
```html
<!-- Satoshi -->
<link href="https://api.fontshare.com/v2/css?f[]=satoshi@900,700,500,400&display=swap" rel="stylesheet">
<!-- Josefin Sans -->
<link href="https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300;400;600&display=swap" rel="stylesheet">
```

### 间距基准

```
页面左右 padding:    80px (desktop) / 24px (mobile)
Section 上下:        120px
模块间距:             64px
```

---

## 全局组件

### Navigation

**布局：** fixed top，全宽，`padding: 28px 80px`  
**滚动后：** `background: rgba(10,10,10,0.95)` + `backdrop-filter: blur(16px)` + `padding: 18px 80px`  
**过渡时长：** 400ms ease

**结构：**
```
[左] Logo mark + wordmark
[中] 导航链接
[右] CTA 按钮
```

**Logo（左）：**
- mark：`no`（小写），Satoshi 900，22px，letter-spacing: -0.03em
- wordmark：`NINE ONE`（大写），Josefin Sans 400，8px，letter-spacing: 0.5em，color: graphite
- 两行竖排，行距紧凑

**导航链接（中）：**
- 文字：`SPORTS` / `TECHNOLOGIES` / `ABOUT`
- 字体：Josefin Sans 400，11px，letter-spacing: 0.28em，uppercase
- 颜色：graphite，hover → white
- hover 下方出现 1px Lime 下划线（scaleX 0→1，transform-origin: left，300ms）

**CTA 按钮（右）：**
- 文字：`BUILD WITH US →`
- 背景：Lime `#C7F000`
- 字体：Josefin Sans 600，10px，letter-spacing: 0.3em，uppercase
- color：black
- padding：12px 24px
- border-radius：0（无圆角）
- hover：background → `#D8FF4D`，箭头 translateX 4px

---

## Section 01 · Hero

### 视觉

**容器：** `height: 100vh`，`min-height: 700px`，`overflow: hidden`，`position: relative`

**背景图：**
- 全屏摄影：夜间 Padel 俱乐部建筑 + 球场
- `object-fit: cover`，`object-position: center`
- overlay：`linear-gradient(to bottom, rgba(10,10,10,0.1) 0%, rgba(10,10,10,0.72) 100%)`
- 进入动画：`scale: 1.06 → 1.0`，duration 8s，ease-out

**布局：** flex，`justify-content: flex-end`（内容靠底部），`padding: 0 80px 72px`

### 内容

**主标题：**
```
MOVE
TOGETHER.
```
- 字体：Josefin Sans 300（light weight）
- 字号：clamp(72px, 10vw, 120px)
- letter-spacing：-0.02em
- line-height：0.92
- color：white
- `TOGETHER.` 末尾句点：color Lime `#C7F000`
- 进入：fadeUp，y: 40→0，opacity 0→1，duration 1s，delay 0.4s

**副标题：**
```
Building the future infrastructure
of recreational movement.
```
- 字体：Satoshi 400
- 字号：16px
- line-height：1.7
- color：rgba(245,245,243,0.65)
- margin-top：32px
- 进入：fadeUp，delay 0.7s

**CTA 区域：**
- margin-top：44px
- display flex，align-items center，gap 24px
- 进入：fadeUp，delay 0.9s

**Primary CTA：**
- 文字：`BUILD WITH US →`
- 同 Nav CTA 样式，padding：15px 32px

**Secondary CTA：**
- 文字：`PLAY VIDEO` + 圆形播放按钮图标
- 播放圆圈：width/height 36px，border 1px solid rgba(255,255,255,0.3)，border-radius 50%，内含 ▶ icon（8px）
- 字体：Josefin Sans 400，10px，letter-spacing 0.3em，uppercase
- color：rgba(255,255,255,0.6)
- hover：color → white，border-color → white

### 动效总结

| 元素 | delay | duration | 效果 |
|------|-------|----------|------|
| 背景图 | 0s | 8s | scale 1.06→1 |
| 主标题 | 0.4s | 1s | fadeUp y:40 |
| 副标题 | 0.7s | 0.9s | fadeUp y:32 |
| CTA | 0.9s | 0.9s | fadeUp y:24 |

---

## Section 02 · Sports

**背景：** `#0A0A0A`（或接近纯黑的深色）  
**布局：** CSS Grid，`grid-template-columns: 1fr 1fr`，`min-height: 85vh`

### 左侧（文字区）

**padding：** `100px 80px`  
**display：** flex column，justify-content center

**节号标签：**
- 文字：`01 ——`
- 字体：Josefin Sans 400，10px，letter-spacing 0.4em，uppercase
- color：Lime
- `——` 是一条 32px 宽的 1px Lime 横线（用 `::after` 或 `<span>` 实现）
- margin-bottom：20px

**主标题：**
- 文字：`SPORTS`
- 字体：Satoshi 900
- 字号：clamp(48px, 6vw, 80px)
- letter-spacing：-0.03em
- color：white
- margin-bottom：20px

**Body copy：**
```
We build more than courts.
We build movement destinations.
```
- 字体：Satoshi 400，15px，line-height 1.8
- color：graphite
- max-width：300px
- margin-bottom：48px

**CTA 链接：**
- 文字：`BUILD WITH US →`
- 字体：Josefin Sans 600，10px，letter-spacing 0.35em，uppercase
- color：Lime
- 无背景，无边框，纯文字链接
- hover：箭头 translateX 6px，200ms

### 右侧（图片网格区）

**布局：** CSS Grid，`grid-template-columns: 1fr 1fr`，`grid-template-rows: 1fr 1fr`  
**overflow：** hidden  
**height：** 100%（撑满父容器）

**图片分布（2×2 网格）：**

```
┌─────────────────┬────────┐
│                 │ 右上图  │
│  左侧大图        ├────────┤
│  (跨2行)        │ 右下图  │
│                 ├────────┤
│                 │ 右下角  │
└─────────────────┴────────┘
```

具体：
- 左侧大图：`grid-row: 1 / 3`，`grid-column: 1`，球场全景（夜间，球员剪影）
- 右上图：俱乐部室内休息区（暖色调）
- 右中图：俱乐部走廊 / 导视系统
- 右下图：社区聚会场景（带 `no` logo 可见）

**图片样式：**
- `object-fit: cover`，`width: 100%`，`height: 100%`
- 各图之间：2px gap（深色分割线感）
- hover：轻微 scale 1.03，400ms ease（optional）

**开发阶段 placeholder URLs（Unsplash）：**
```
左大图:  https://images.unsplash.com/photo-1554068865-24cecd4e34b8?w=800&q=80
右上:    https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=500&q=80
右中:    https://images.unsplash.com/photo-1590650153855-d9e808231d41?w=500&q=80
右下:    https://images.unsplash.com/photo-1529156069898-49953e39b3ac?w=500&q=80
```

### Scroll Reveal

左侧文字区：IntersectionObserver，threshold 0.15，fadeUp（y:32，opacity 0→1，800ms）  
各元素 stagger delay：标签 0s → 标题 0.1s → body 0.2s → CTA 0.35s

---

## Section 03 · Technologies

**背景：** `#070710`（极深蓝黑，区别于纯黑）  
**布局：** CSS Grid，`grid-template-columns: 1fr 1fr`，`min-height: 85vh`，`align-items: center`

### 左侧（视觉区）

**布局：** relative，overflow hidden，height 100%  
**display：** flex，align-items center，justify-content center，padding 60px

**包含两个叠层元素：**

**① 手机 App 截图（Dashboard）：**
- 位置：居中偏右
- 模拟手机屏幕：圆角矩形，深色背景，蓝色边框 `border: 1px solid rgba(45,125,255,0.2)`
- 内容（UI 模拟，非真实截图）：
  - 顶部：`Performance` + `Overview` 标签（Josefin Sans，9px，蓝色）
  - 大数字：`87`（Satoshi 900，80px，white）
  - 副标签：`Movement Score`（10px，蓝色）
  - 指标行：`↑ 12%`（12px，Lime）
  - 底部：Activity 折线图（用 CSS/SVG 模拟，蓝色线条）
  - 底部导航栏：4个图标（Home / Activity / Clubs / Profile）
- 整体：width ~220px，shadow `0 24px 64px rgba(0,0,0,0.6)`

**② 球拍图（叠在手机左后方）：**
- 位置：absolute，left: -20px，bottom: 40px，z-index: 0
- 球拍图片（黑色球拍，带 `no` logo），角度：rotate(-20deg)
- 浮动动画：translateY 0→-12px→0，6s ease-in-out infinite
- opacity：0.9

### 右侧（文字区）

**padding：** `100px 80px`  
**display：** flex column，justify-content center

**节号标签：**
- 文字：`02 ——`
- color：Blue `#2D7DFF`
- 其余同 Sports 标签规则

**主标题：**
- 文字：`TECHNOLOGIES`
- 同 SPORTS 字号规则，Satoshi 900

**Body copy：**
```
Intelligent systems,
connected data and AI
to elevate performance
and operations.
```
- Satoshi 400，15px，line-height 1.8，color graphite
- margin-bottom：48px

**CTA 链接：**
- 文字：`EXPLORE TECHNOLOGIES →`
- color：Blue `#2D7DFF`
- hover → `#4B9CFF`，箭头 translateX 6px

---

## Section 04 · Ecosystem

**背景：** `#0A0A0A`  
**padding：** `100px 80px`

### 左侧文字（上方）

**节号标签：** `03 ——`，color Lime

**主标题：** `ECOSYSTEM`，Satoshi 900

**Body copy：**
```
An integrated ecosystem
connecting physical, digital
and intelligence layers.
```

**CTA：** `EXPLORE ECOSYSTEM →`，color Lime

### 流程图（核心视觉）

**布局：** 横向排列，`display: flex`，`align-items: center`，`gap: 0`  
**margin-top：** 64px

**节点结构（5个节点 + 1个终点圆）：**

```
[COURTS] --→-- [CLUBS] --→-- [HARDWARE] --→-- [DATA] --→-- [AI] --→-- (no · MOVEMENT ECOSYSTEM)
```

**每个节点：**
- 外圆：直径 80px，border 1px solid rgba(255,255,255,0.15)，border-radius 50%
- 内图标：线框风格 SVG icon（24px），color white/graphite
- 图标下方标题：Josefin Sans 600，10px，letter-spacing 0.3em，uppercase，color white，margin-top 16px
- 副标签：Satoshi 400，11px，color graphite，text-align center，max-width 80px

**节点图标对应：**
| 节点 | 图标 |
|------|------|
| COURTS | 球场俯视线框（矩形+网格线） |
| CLUBS | 建筑线框 |
| HARDWARE | 圆柱形数据库堆叠 |
| DATA | 信号/波纹 |
| AI | 脑神经网络 |

**连接线：**
- 样式：`border-top: 1px dashed rgba(199,240,0,0.4)`
- 宽度：flex 1，自适应
- 中点有箭头：`→`，color Lime，font-size 12px
- 箭头位置：绝对居中于连接线上

**终点圆（Movement Ecosystem）：**
- 直径：96px
- border：1px solid rgba(199,240,0,0.5)
- 内部：
  - `no` logo（Satoshi 900，18px，white）
  - `MOVEMENT` （Josefin Sans 400，7px，letter-spacing 0.4em，Lime）
  - `ECOSYSTEM`（同上）
- 与上一个节点连接线同样样式

**Scroll reveal：** 节点从左到右 stagger，delay 0.1s × index

---

## Section 05 · Why We Exist

**背景：** 黑色  
**布局：** CSS Grid，`grid-template-columns: 1fr 1fr`，`min-height: 80vh`，`align-items: center`

### 左侧（文字区）

**padding：** `100px 80px`

**节号标签：** `04 ——`，color Lime

**主标题：** `WHY WE EXIST`，Satoshi 900，clamp(40px, 5vw, 64px)

**Body copy（两段）：**
```
We believe movement should bring
people together. Not pressure. Not
performance. But heathier lives,
stronger communities and better
everyday experiences.
```
（空行）
```
NINE ONE is building the future
infrastructure of recreational
movement — through sports
spaces, connected technology
and intelligent systems.
```
- Satoshi 400，15px，line-height 1.85，color graphite
- max-width：380px
- 两段间距：24px

**底部 Lime 高亮文字：**
```
Padel is the starting point.
Movement is the future.
```
- 字体：Satoshi 500，15px
- color：Lime `#C7F000`
- margin-top：32px
- 可做 typewriter 出现动效（optional）

### 右侧（图片区）

**布局：** position relative，overflow hidden，height 100%

**背景图：**
- 黄昏剪影：一群人（4–5人）手持球拍，面对夕阳，强剪影效果
- `object-fit: cover`，暖橙色黄昏调
- overlay：`linear-gradient(to right, rgba(10,10,10,0.7) 0%, rgba(10,10,10,0.1) 100%)`

**开发阶段 placeholder：**
```
https://images.unsplash.com/photo-1529156069898-49953e39b3ac?w=900&q=80
```

---

## Footer

**背景：** `#040404`  
**border-top：** `1px solid rgba(255,255,255,0.06)`  
**padding：** `48px 80px 36px`

### 上部区域

**布局：** flex，justify-content space-between，align-items center  
**margin-bottom：** 40px

**左：Logo**
- mark `no`：Satoshi 900，22px
- wordmark `NINE ONE`：Josefin Sans 400，8px，letter-spacing 0.5em，uppercase，color graphite

**中：导航链接**
- SPORTS / TECHNOLOGIES / ABOUT / BUILD WITH US / CONTACT US
- Josefin Sans 400，10px，letter-spacing 0.3em，uppercase，color graphite
- hover → white，200ms

**右：社交图标**
- Instagram / LinkedIn / YouTube（或 ▶ 播放图标）
- 图标大小：18px
- color：graphite，hover → white
- gap：20px

### 下部区域

**border-top：** `1px solid rgba(255,255,255,0.04)`  
**padding-top：** 24px  
**布局：** flex，justify-content space-between

**左：**
```
© 2024 NINE ONE. All rights reserved.
```
- Satoshi 400，11px，color rgba(138,138,138,0.4)

**右：**
```
Privacy Policy    Terms of Service
```
- Josefin Sans 400，10px，letter-spacing 0.25em，uppercase，color rgba(138,138,138,0.4)
- hover → graphite

---

## 全局动效规范

### Scroll Reveal（通用）

```javascript
// Framer Motion 版本
const variants = {
  hidden: { opacity: 0, y: 32 },
  visible: { opacity: 1, y: 0, transition: { duration: 0.8, ease: [0.16, 1, 0.3, 1] } }
};

// IntersectionObserver 版本（纯 CSS）
.reveal { opacity: 0; transform: translateY(32px); transition: opacity 0.8s ease, transform 0.8s ease; }
.reveal.in { opacity: 1; transform: none; }
```

### 禁止

- Glitch / Noise 动效
- Bounce / Spring（弹跳感）
- 粒子系统
- 过度 3D transform
- 霓虹 / 赛博朋克效果

---

## 响应式断点

| 断点 | 处理 |
|------|------|
| < 1024px | 双列 → 单列 |
| < 768px | padding 80px → 24px |
| < 768px | Nav 链接隐藏，汉堡菜单 |
| < 768px | Hero 字号 clamp 最小值生效 |
| < 768px | Ecosystem 流程图纵向排列 |

---

## 文件结构建议

```
/app
  page.tsx                    ← Homepage 入口

/components
  /layout
    Nav.tsx                   ← 固定导航
    Footer.tsx                ← 页脚

  /sections/home
    Hero.tsx                  ← Section 01
    Sports.tsx                ← Section 02
    Technologies.tsx          ← Section 03
    Ecosystem.tsx             ← Section 04
    WhyWeExist.tsx            ← Section 05

  /ui
    Button.tsx                ← Lime / Ghost / Text 三种
    SectionLabel.tsx          ← "01 ——" 标签组件
    RevealWrapper.tsx         ← Scroll reveal 包装器

/lib
  constants.ts                ← 品牌 token、文案内容
  animations.ts               ← Framer Motion variants
```

---

## 文案总表

| 位置 | 文案 |
|------|------|
| Nav CTA | BUILD WITH US → |
| Hero H1 | MOVE TOGETHER. |
| Hero H1 句点 | Lime 色 |
| Hero Sub | Building the future infrastructure of recreational movement. |
| Hero CTA 1 | BUILD WITH US → |
| Hero CTA 2 | PLAY VIDEO ▶ |
| S02 标签 | 01 —— |
| S02 标题 | SPORTS |
| S02 Body | We build more than courts. We build movement destinations. |
| S02 CTA | BUILD WITH US → |
| S03 标签 | 02 —— |
| S03 标题 | TECHNOLOGIES |
| S03 Body | Intelligent systems, connected data and AI to elevate performance and operations. |
| S03 CTA | EXPLORE TECHNOLOGIES → |
| S04 标签 | 03 —— |
| S04 标题 | ECOSYSTEM |
| S04 Body | An integrated ecosystem connecting physical, digital and intelligence layers. |
| S04 CTA | EXPLORE ECOSYSTEM → |
| S04 节点 | COURTS / CLUBS / HARDWARE / DATA / AI |
| S04 终点 | no · MOVEMENT ECOSYSTEM |
| S05 标签 | 04 —— |
| S05 标题 | WHY WE EXIST |
| S05 Lime | Padel is the starting point. Movement is the future. |
| Footer 版权 | © 2024 NINE ONE. All rights reserved. |
| Footer 链接 | Privacy Policy · Terms of Service |

---

*NINE ONE Homepage Spec V1.0*  
*Based on: Homepage_mockup.png*  
*Move Together.*
