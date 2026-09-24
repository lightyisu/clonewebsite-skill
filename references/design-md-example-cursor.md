# Cursor — Style Reference

> Warm parchment atelier lit by embers
> 来源: https://styles.refero.design/style/4e3b4717-84c8-4599-baaf-a343c3d619b6 (Refero Styles, 取自 cursor.com 实测数据)

主题: light

风格综述: Cursor 使用"暖羊皮纸编辑排版"语言——奶油色画布、墨黑文字、单一余烬橙强调色(只用于链接和强调,不填充按钮)。标题一律 400 字重 + 随字号增大而收紧的字距("whisper headline",权威感来自克制而非加粗)。表面扁平如纸,发丝线边框 + 暖灰柔和阴影,圆角统一 4px。EB Garamond 只出现在编辑性副标题和正文段落,berkeleyMono 负责代码/标签/元数据。整体像一本文学期刊,而不是 SaaS 仪表盘。

## 颜色

| 名称 | 值 | 用途 |
|------|-----|------|
| Parchment | `#f7f7f4` | 页面背景/主画布,暖奶油色 |
| Bone | `#f2f1ed` | 卡片表面、浮起容器(比画布深一档,"纸上叠纸") |
| Linen | `#e6e5e0` | 浅色按钮填充、更高层级表面 |
| Stone | `#cdcdc9` | 发丝线边框、分隔线(暖调 1px) |
| Mist | `#a1a19f` | 三级辅助文字、说明 |
| Driftwood | `#84847e` | 二级正文、表格内容 |
| Ash | `#7a7974` | 图标填充、弱化标签——主力灰 |
| Ink | `#26251e` | 主文字、主按钮背景、导航文字(暖调近黑,禁用纯黑) |
| Ember | `#f54e00` | 橙色强调,仅用于内联链接/标签/强调短语,禁止做按钮背景 |
| Amber | `#c08532` | 暖色动作按钮填充(Build/Continue)、图标描边 |
| Forest | `#34785c` | 绿色实心按钮、选中导航态 |
| Verdant | `#1f8a65` | 绿色文字强调 |
| Crimson | `#cf2d56` | 红色文字强调 |

文字选中高亮: `#8BC4F8`(全系统唯一的冷色,只用于浏览器文本选区)。

## 字体

### CursorGothic(主字体)
- 替代: Inter, system-ui, Helvetica Neue
- 字重: 400, 500(标题禁用 600+)
- 字号: 11, 13, 14, 16, 22, 26, 36, 72px
- 行高: 1.00–1.50
- 字距(签名特性,随字号收紧): 14px: 0.01em → 22px: -0.005em → 26px: -0.012em → 36px: -0.02em → 72px: -0.03em
- OpenType 特性: `"ss08", "ss09", "tnum"`
- 角色: UI、标题、导航、正文、产品界面

### EB Garamond(编辑衬线)
- 替代: Iowan Old Style, Palatino Linotype, ui-serif, Georgia
- 字重: 400, 500;字号 16/17/19px;行高 1.35–1.50;字距 normal
- 角色: 编辑性副标题、散文正文、表格数据。不用于 UI 标签和导航

### berkeleyMono(等宽)
- 替代: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas
- 字重: 400, 500;字号 12/13px;行高 1.43–1.67
- 角色: 代码块、CLI 片段、元数据标签、文件路径、开发者向文案

## 字号层级

| 角色 | 字号 | 行高 | 字距 |
|------|------|------|------|
| eyebrow | 12px | 1.63 | — |
| body-sm | 14px | 1.5 | 0.14px |
| body | 16px | 1.5 | — |
| heading-sm | 22px | 1.3 | -0.11px |
| heading | 26px | 1.25 | -0.312px |
| heading-lg | 36px | 1.2 | -0.72px |
| display | 72px | 1.1 | -2.16px |

## 间距与形状

- 基础单位: 4px;密度: compact
- 间距阶梯: 4 / 8 / 12 / 16 / 20 / 24 / 32 / 48 / 56 / 64 px
- 圆角: 卡片/瓦片/输入框/按钮 4px;弹窗 8px(禁用药丸形 ≥999px)
- 布局: 页面最大宽 1300px,外边距 24px;区块间距 64–96px;卡片内边距 24px;元素间距 8px

## 阴影

- 产品 mockup 卡片: `rgba(0,0,0,0.14) 0 28px 70px, rgba(0,0,0,0.1) 0 14px 32px, oklab(0.263 -0.002 0.012 / 0.1) 0 0 0 1px`
- Flyout/popover: `0 0 1rem #00000005, 0 0 0.5rem #00000002`
- subtle: `rgb(235,234,229) 0 0 0 2px`
- 阴影必须保持暖调,禁止偏蓝/偏冷

## 组件规格

- **主按钮(Download)**: 背景 Ink `#26251e`、文字 Parchment,4px 圆角,padding 0.78em 1.35em,CursorGothic 14px/400,无渐变无边框,transition 150ms cubic-bezier(0.4,0,0.2,1)
- **次按钮**: 背景 Linen `#e6e5e0`、文字 Ink,同尺寸,可带 → 箭头;与主按钮成对出现
- **Ghost 文字按钮**: 透明背景,Ink 60% 透明度,无边框,hover 下划线,13–14px/400
- **Amber 按钮**: 背景 `#c08532`、浅奶油文字,紧凑 padding 6px 12px,用于产品 UI/CLI mockup 内
- **Forest 按钮**: 背景 `#34785c`、Parchment 文字、同色 1px 边框
- **产品卡片**: 背景 Bone,4px 圆角,1px 边框 color-mix(in oklab, #26251e 5%, transparent),双层暖阴影,内边距 24px
- **导航栏**: 透明背景,高 52px,左右 padding 24px;左侧 logo+字标(14px/500),中间 4 个链接(14px/400),右侧 Sign in + ghost + 实心 Download;无 sticky 阴影
- **终端输入框**: 透明或 Bone 背景,1px 边框 color-mix(#26251e 10%, transparent),4px 圆角,padding 10px 12px,berkeleyMono 12px,提示符 $ 用 Ash 色
- **页脚链接列**: 列标题 14px/500 Ink,链接 13px/400 Ash,行距 8px,直接坐在画布上无卡片
- **Mono 元数据标签**: berkeleyMono 12px Ash,无背景无边框,内联使用

## 布局骨架

1. 顶部透明导航(52px)
2. Hero: 左对齐大标题(display 72px)+ 双 CTA,下方通栏产品 mockup 卡片
3. 信任条: 一行 8 个客户 logo 瓦片(Linen 背景,logo 用 Ink 60% 透明度的单色字标)
4. 特性区: 左文右图两栏 40/60,区块间 64–96px 呼吸感分隔(不用分割线)
5. 页脚: 四列链接栅格 + 左侧品牌标

## Do / Don't

**Do**
- 全部 4px 圆角(按钮/卡片/输入框/瓦片)
- 标题一律 CursorGothic 400 字重,靠收紧字距制造权威感
- 字距随字号渐进收紧(见字号层级表)
- 画布 #f7f7f4 + 卡片 #f2f1ed 分层;优先用 1px color-mix 边框,其次才是阴影
- Ember 橙只做内联文字强调
- EB Garamond 只用于编辑性副标题和散文
- berkeleyMono 12px 用于一切代码/路径/CLI
- 同一动作组: 一个实心深色 + 一个实心浅色(或 ghost),不超过两种

**Don't**
- 禁用纯白 #ffffff 和纯黑 #000000
- 标题禁用 600/700 字重
- 禁用药丸形按钮/卡片
- 禁用渐变、辉光、色块渐染——深度只来自发丝线边框和暖灰阴影
- 阴影禁止偏蓝偏冷
- Ember 橙禁止做背景或大面积填充
- 标题/重要文字禁用 system-ui
- 动作组内禁止三个实心按钮堆叠

## 图片与图标

产品截图为主——大型 macOS 窗口 mockup(文件标签、diff 视图、agent 计划、终端面板),每个窗口外面包 Bone 色卡片框。Hero 背后可衬一张低饱和风景照(山脉/沙漠地平线)。客户 logo 用单色字标。不用人物照片、不用插画、不用抽象装饰图形。图标统一细描边 monoline,Ash 灰填充,永不用彩色。

## CSS 变量(直接可用)

```css
:root {
  /* 颜色 */
  --color-parchment: #f7f7f4;
  --color-bone: #f2f1ed;
  --color-linen: #e6e5e0;
  --color-stone: #cdcdc9;
  --color-mist: #a1a19f;
  --color-driftwood: #84847e;
  --color-ash: #7a7974;
  --color-ink: #26251e;
  --color-ember: #f54e00;
  --color-amber: #c08532;
  --color-forest: #34785c;
  --color-verdant: #1f8a65;
  --color-crimson: #cf2d56;

  /* 字体 */
  --font-cursorgothic: 'CursorGothic', ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-eb-garamond: 'EB Garamond', ui-serif, Georgia, serif;
  --font-berkeleymono: 'berkeleyMono', ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;

  /* 字号 */
  --text-eyebrow: 12px;      --leading-eyebrow: 1.63;
  --text-body-sm: 14px;      --leading-body-sm: 1.5;   --tracking-body-sm: 0.14px;
  --text-heading-sm: 22px;   --leading-heading-sm: 1.3; --tracking-heading-sm: -0.11px;
  --text-heading: 26px;      --leading-heading: 1.25;  --tracking-heading: -0.312px;
  --text-heading-lg: 36px;   --leading-heading-lg: 1.2; --tracking-heading-lg: -0.72px;
  --text-display: 72px;      --leading-display: 1.1;   --tracking-display: -2.16px;

  /* 间距 */
  --spacing-unit: 4px;
  /* 4/8/12/16/20/24/32/48/56/64px */

  /* 布局 */
  --page-max-width: 1300px;
  --section-gap: 64px 96px;
  --card-padding: 24px;
  --element-gap: 8px;

  /* 圆角 */
  --radius-md: 4px;   /* 卡片/按钮/输入框 */
  --radius-lg: 8px;   /* 弹窗 */

  /* 阴影 */
  --shadow-xl: rgba(0,0,0,0.14) 0 28px 70px 0, rgba(0,0,0,0.1) 0 14px 32px 0, oklab(0.263084 -0.00230259 0.0124794 / 0.1) 0 0 0 1px;
  --shadow-subtle: rgb(235,234,229) 0 0 0 2px;

  /* 表面层级 */
  --surface-canvas: #f7f7f4;
  --surface-card: #f2f1ed;
  --surface-elevated: #e6e5e0;
  --surface-outline: #cdcdc9;
}
```

## Tailwind v4 @theme

```css
@theme {
  --color-parchment: #f7f7f4;
  --color-bone: #f2f1ed;
  --color-linen: #e6e5e0;
  --color-stone: #cdcdc9;
  --color-mist: #a1a19f;
  --color-driftwood: #84847e;
  --color-ash: #7a7974;
  --color-ink: #26251e;
  --color-ember: #f54e00;
  --color-amber: #c08532;
  --color-forest: #34785c;
  --color-verdant: #1f8a65;
  --color-crimson: #cf2d56;

  --font-cursorgothic: 'CursorGothic', ui-sans-serif, system-ui, sans-serif;
  --font-eb-garamond: 'EB Garamond', ui-serif, Georgia, serif;
  --font-berkeleymono: 'berkeleyMono', ui-monospace, SFMono-Regular, Menlo, monospace;

  --text-eyebrow: 12px;      --leading-eyebrow: 1.63;
  --text-body-sm: 14px;      --leading-body-sm: 1.5;  --tracking-body-sm: 0.14px;
  --text-heading-sm: 22px;   --leading-heading-sm: 1.3; --tracking-heading-sm: -0.11px;
  --text-heading: 26px;      --leading-heading: 1.25; --tracking-heading: -0.312px;
  --text-heading-lg: 36px;   --leading-heading-lg: 1.2; --tracking-heading-lg: -0.72px;
  --text-display: 72px;      --leading-display: 1.1;  --tracking-display: -2.16px;

  --radius-md: 4px;
  --radius-lg: 8px;

  --shadow-xl: rgba(0,0,0,0.14) 0 28px 70px 0, rgba(0,0,0,0.1) 0 14px 32px 0;
  --shadow-subtle: rgb(235,234,229) 0 0 0 2px;
}
```

## 类似风格品牌(备选参考)

Linear(同款奶油+墨色、4px、400 字重标题)、Vercel(暖白画布 + 单一强调色)、Stripe(文档式排版层级)、Arc Browser(纸质浮起的窗口卡片)、Notion(近单色 + 暖强调 + 衬线点缀)。
