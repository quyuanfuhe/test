# MR Flag Battle 项目总结汇报 — Design Spec

> Human-readable design narrative. Machine-readable execution contract: `spec_lock.md`. On divergence, `spec_lock.md` wins.

## I. Project Information

| Item | Value |
| ---- | ----- |
| **Project Name** | MR Flag Battle 项目总结汇报 |
| **Canvas Format** | PPT 16:9 (1280×720) |
| **Page Count** | 18 页 |
| **Design Style** | dark-tech — 深色科技风 |
| **Target Audience** | 项目评审老师 / 团队同学 |
| **Use Case** | 项目答辩 / 结题汇报 |
| **Delivery Purpose** | `presentation` — 演讲展示型，每页一个核心观点 |
| **Content Strategy** | 用户提供完整章节结构。四大板块各设章节导览页（简述该板块子内容），每个子内容独立一页。结构：标题页→目录→4个板块(章节页+子内容页)→结束页。精炼内容，保持来源事实不变。 |
| **Created Date** | 2026-07-15 |

## II. Canvas Specification

| Property | Value |
| -------- | ----- |
| **Format** | PPT 16:9 |
| **Dimensions** | 1280×720 |
| **viewBox** | `0 0 1280 720` |
| **Margins** | 左右 60px，上 50px，下 40px |
| **Content Area** | 1160×630 |

## III. Visual Theme

### Theme Style

- **Mode**: `pyramid` — 结论先行，MECE 分解，每页标题即结论
- **Visual style**: `dark-tech` — 深色画布、发光强调、几何精准
- **Theme**: Dark theme
- **Tone**: 专业、科技、前沿、自信

### Color Scheme

| Role | HEX | Purpose |
| ---- | --- | ------- |
| **Background** | `#0A0E17` | 页面主背景，深蓝黑 |
| **Secondary bg** | `#111827` | 卡片/区块背景 |
| **Primary** | `#3B82F6` | 标题装饰、关键分区、发光强调 |
| **Accent** | `#06D6D0` | 数据高亮、关键信息点 |
| **Secondary accent** | `#8B5CF6` | 次要强调、渐变过渡 |
| **Body text** | `#E2E8F0` | 正文文字，浅灰白 |
| **Secondary text** | `#94A3B8` | 说明文字、标注 |
| **Tertiary text** | `#64748B` | 补充信息、页脚 |
| **Border/divider** | `#1E293B` | 卡片边框、分割线 |
| **Success** | `#10B981` | 完成/正面指标 |
| **Warning** | `#F59E0B` | 提示标记 |

No AI image strategy section — the deck has no AI-generated images.

### Gradient Scheme (SVG)

```xml
<!-- 页面背景呼吸渐变 -->
<radialGradient id="bgGlow" cx="85%" cy="15%" r="60%">
  <stop offset="0%" stop-color="#3B82F6" stop-opacity="0.08"/>
  <stop offset="100%" stop-color="#3B82F6" stop-opacity="0"/>
</radialGradient>

<!-- 标题下划线发光渐变 -->
<linearGradient id="titleUnderline" x1="0%" y1="0%" x2="100%" y2="0%">
  <stop offset="0%" stop-color="#3B82F6"/>
  <stop offset="100%" stop-color="#06D6D0"/>
</linearGradient>
```

## IV. Typography System

### Font Plan

- **Title font**: `"Microsoft YaHei", Arial, sans-serif` — 清晰现代的标题
- **Body font**: `"Microsoft YaHei", Arial, sans-serif` — 正文
- **Code font**: `Consolas, "Courier New", monospace` — 技术术语/代码引用
- **Font stacking**: Windows 预装优先，`Microsoft YaHei` 主导 CJK，`Arial` 主导 Latin

### Font Sizes (px, unitless)

| Role | Size | Usage |
| ---- | ---- | ----- |
| **cover_title** | 60 | 封面主标题 |
| **cover_subtitle** | 28 | 封面副标题 |
| **section_title** | 52 | 章节导览页大标题 |
| **section_desc** | 22 | 章节导览页子内容描述 |
| **page_title** | 36 | 内容页标题 |
| **lead** | 24 | 页面核心观点/引言 |
| **body** | 20 | 正文列表、段落 |
| **subheading** | 24 | 分组标题 |
| **annotation** | 16 | 预留区标签、注脚 |
| **footnote** | 14 | 页码、底部标注 |

All sizes are px.

## V. Layout Plan

Free-design layout, dark-tech principles:
- **Page structure**: 深色背景 + 右上角呼吸渐变。标题左对齐，底部蓝色→青色渐变下划线分隔标题与正文。
- **Chapter opener pages**: 大号章节编号 + 章节标题居中/左侧，下方列出该板块子内容条目（用发光圆点或序号标注）。
- **Cards**: 使用 `secondary_bg (#111827)` 填充的圆角矩形卡片 (rx=8)，1px `border` 色描边。
- **Grid**: 2列/3列网格布局用于多要点展示。
- **Placeholder blocks**: 使用虚线边框 (`stroke-dasharray="6,4"`) 的半透明矩形标识预留区域，居中加文字提示，颜色使用 `text_tertiary`。
- **Page rhythm**: 章节导览页为 `breathing`（低密度、重在引导），内容密集页为 `dense`，封面/目录/结束页为 `anchor`。

## VI. Icon Plan

No icons used in this deck. dark-tech visual style is sparse by default; geometric shapes and glow accents replace iconography.

## VII. Visualization Plan

No charts or data visualizations in this deck.

## VIII. Image Resource List

No images in this deck. All visual expression uses native SVG shapes, gradients, and decorative geometry. Placeholder zones use dashed-border rectangles.

## IX. Content Outline

| Page | Title | Rhythm | Description |
| ---- | ----- | ------ | ----------- |
| P01 | MR Flag Battle 混合现实夺旗大战 | anchor | 封面：项目名称、团队信息、日期。深色背景 + 发光几何图形装饰 + 渐变呼吸光。 |
| P02 | 目录 | anchor | 四大板块索引：①项目介绍与意义 ②前期设计与最终实现 ③工作汇报 ④思考与收获。每项带页码。 |
| P03 | 项目介绍与意义 | breathing | 板块导览页：大号"01"编号 + 章节标题，下方列出本板块3个子内容（项目背景 / 项目介绍 / 项目意义），各附一句简要说明。 |
| P04 | 项目背景 | dense | 开发工具与游戏受众。左侧卡片列开发环境（Unity、Pico SDK、Go后端），右侧卡片列目标受众。 |
| P05 | 项目介绍 | breathing | 游戏概述：MR Flag Battle 是什么，核心玩法（单人/双人夺旗），核心功能（地图编辑、空间锚点、实时同步）。大标题 + 简段 + 功能要点卡片。 |
| P06 | 项目意义 | dense | 双列布局：左列项目本身的价值（技术探索、MR闭环、全栈链路、参考方案），右列成员的成长收获。 |
| P07 | 前期设计与最终实现 | breathing | 板块导览页：大号"02"编号 + 章节标题，列出本板块4个子内容（游戏流程与构筑要素 / 开发计划 / 需求分析与设计文档 / 最终实现），各附简要说明。 |
| P08 | 游戏流程与构筑要素 | dense | 上排：5步游戏流程图（线性步骤）。下排：4组构筑要素卡片（场景物体、旗帜系统、玩家系统、UI系统）。 |
| P09 | 开发计划 | dense | 六阶段开发计划，水平时间线样式。每阶段一个卡片：标题 + 关键内容简述。 |
| P10 | 需求分析与设计文档 | breathing | 两个预留图片框：上方 "需求分析文档" 虚线框，下方 "设计文档" 虚线框。框内居中提示文字，尺寸各约 500×220px。 |
| P11 | 最终实现 — 实现成果 | dense | ✅ 九大功能模块清单，2列网格，每项带绿色状态标记和简短描述。 |
| P12 | 最终实现 — 技术亮点与演示 | breathing | 左侧：3个技术亮点卡片（空间锚点、MsgPack编解码、开发简化模式）。右侧：预留视频区域（虚线框 + "演示视频" 提示文字）。 |
| P13 | 工作汇报 | breathing | 板块导览页：大号"03"编号 + 章节标题，简要说明本板块为各成员的工作内容汇报。 |
| P14 | 成员工作概览 | dense | 2×2 网格排列4个成员卡片，统一风格。每个卡片含：姓名占位符、工作内容占位区（虚线填充）。 |
| P15 | 思考与收获 | breathing | 板块导览页：大号"04"编号 + 章节标题，列出子内容（技术与管理收获 / 未来展望）。 |
| P16 | 技术与管理收获 | dense | 双列布局：左列技术收获（XR开发、空间锚点、网络通信、协议设计），右列项目管理收获（Git协作、模块架构、代码保护策略）。 |
| P17 | 未来展望 | breathing | 5个未来规划方向，横向排列的发光卡片（更多模式、Avatar优化、音效特效、物理交互、编辑器增强）。 |
| P18 | 谢谢观看 | anchor | 结束页：大字"谢谢观看" + 团队信息占位。与封面风格呼应，深色背景 + 呼吸渐变。 |

## X. Speaker Notes

Each page carries a brief speaker note: the key takeaway (one sentence) in the conclusion-first pyramid style, followed by 1-2 supporting points. Notes are authored during SVG generation (Step 6) and written to `notes/total.md`.
