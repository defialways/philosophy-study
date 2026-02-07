# PROJECTS.md - 项目索引

*记录所有项目的格式、位置和关键信息，方便快速查阅和保持一致性*

---

## 📚 哲学解构报告系列

**仓库地址：** `https://github.com/defialways/philosophy-study.git`  
**GitHub Pages：** `https://defialways.github.io/philosophy-study/`  
**本地路径：** `/root/.openclaw/workspace/reports/`

### 格式规范
- **视觉风格**：白底学术风格，简洁清晰
- **主题色**：紫色系（#9b59b6）
- **字体**：系统默认无衬线字体
- **布局**：单栏，最大宽度800px，居中

### 标准结构
1. **标题** + 元信息（作者、日期、阅读对象）
2. **目录**（锚点导航）
3. **核心论点与逻辑架构**（key-point + logic-chain）
4. **哲学谱系**（表格对比 + philosopher标签）
5. **回答的哲学问题**（timeline）
6. **独创与局限**（check/cross标记）
7. **逆时间阅读节点**（logic-chain展示谱系）
8. **延伸阅读顺序**（reading-list）
9. **概念卡片区**（交互式cards-grid）

### CSS组件类名
```css
/* 核心组件 */
.key-point          /* 要点框，紫色左边框 */
.logic-chain        /* 逻辑链条，等宽字体灰底 */
.quote              /* 引用框，灰色左边框 */
.timeline           /* 时间线/对比区域 */
.reading-list       /* 阅读建议，绿色主题 */
.philosopher        /* 哲学家标签（hegel/kojeve/nietzsche等）*/
.concept-card       /* 交互式概念卡片 */
.cards-grid         /* 卡片容器 */
```

### 已有报告

| 书名 | 文件名 | 作者 | 核心哲学家 | 卡片数量 | 状态 |
|------|--------|------|-----------|---------|------|
| 《人类简史》 | `人类简史哲学解构报告.html` | 赫拉利 | 福柯、萨特、海德格尔、尼采 | 6张 | ✅ 已发布 |
| 《词与物》 | `词与物哲学解构报告.html` | 福柯 | 福柯、尼采、海德格尔、马克思 | 6张 | ✅ 已发布 |
| 《历史的终结》 | `历史的终结哲学解构报告.html` | 福山 | 黑格尔、科耶夫、尼采、马克思 | 6张 | ✅ 已发布 |

### X卡片规范
- **尺寸**：1200×628 像素（Twitter大图卡片标准）
- **卡片预览文件**：`card-preview.html`（用于生成分享图）
- **封面元素**：书名（中文+英文）、副标题、作者、核心概念标签、CTA
- **视觉风格**：深色渐变背景（#1a1a2e → #0f3460），紫色点缀

### Open Graph 配置（每份报告头部）
```html
<meta property="og:title" content="《书名》哲学解构报告">
<meta property="og:description" content="从XX到XX，解构XX的XX论 | 逆时间阅读哲学史">
<meta property="og:type" content="article">
<meta property="og:url" content="https://defialways.github.io/philosophy-study/reports/XXX.html">
<meta property="og:image" content="书籍封面图URL">
<meta name="twitter:card" content="summary_large_image">
```

---

## 🤖 AI周报项目

**仓库地址：** `https://github.com/defialways/tiger-ai-insights.git`  
**GitHub Pages：** `https://defialways.github.io/tiger-ai-insights/`  
**本地路径：** `/root/.openclaw/workspace/tiger-ai-insights/`

### 格式规范
- **视觉风格**：深色科技风（#0f172a背景）
- **主题色**：靛蓝+粉色渐变（#6366f1 → #ec4899）
- **布局**：多板块导航（概览/大模型/应用/投资/政策）

### 标准结构
1. **Header**：Logo + 期号 + 日期
2. **导航栏**：sticky定位，板块切换
3. **统计卡片**：4个关键数字（大模型/应用/融资/政策）
4. **数据图表**：ECharts图表（话题分布/融资/股价/地区）
5. **时间线**：本周大事记
6. **分板块详情**：Models/Applications/Investment/Policy
7. **Footer**：品牌信息

### 定时任务
- **频率**：每周三 10:00（北京时间）
- **内容要求**：
  - 中国AI动态占比 ≥ 30%
  - 覆盖四大板块：大模型、应用落地、投资并购、政策法规
  - 中文撰写，数据详实

### 自动化
- 使用 `cron` 设置定时任务
- `HEARTBEAT.md` 保持空白（跳过心跳检查）

---

## 📝 新项目创建流程

### 如果是哲学解构报告：
1. 读取 `PROJECTS.md` 确认仓库位置
2. 读取 `reports/` 目录查看最新报告作为模板
3. 复制格式，替换内容
4. 添加Open Graph标签（书名、封面图URL）
5. 创建概念卡片（6张，交互式）
6. 创建 `card-preview.html`（X分享卡片）
7. 推送到 `philosophy-study` 仓库

### 如果是AI周报：
1. 读取 `tiger-ai-insights/index.html` 作为模板
2. 更新日期、期号、数据
3. 保持深色科技风格
4. 确保中国AI内容占比
5. 推送到 `tiger-ai-insights` 仓库

---

## ⚠️ 常见错误提醒

1. **仓库混淆**：哲学报告 → philosophy-study，AI周报 → tiger-ai-insights
2. **文件路径**：哲学报告放在 `/reports/` 子目录下
3. **URL编码**：中文文件名需使用URL编码（如 `%E5%8E%86%E5%8F%B2`）
4. **卡片功能**：别忘了添加JS交互代码（toggleCard函数）
5. **X卡片尺寸**：1200×628 像素，不要变形

---

## 🔗 快速链接

| 项目 | 主页 | 最新报告 |
|------|------|---------|
| 哲学解构 | https://defialways.github.io/philosophy-study/ | 历史的终结 |
| AI周报 | https://defialways.github.io/tiger-ai-insights/ | index.html |

---

*最后更新：2026年2月7日*  
*维护者：小老虎 🐯*
