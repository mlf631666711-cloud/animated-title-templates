# 动态开头 / 标题模板库 · animated-title-templates

20 个**单文件 HTML** 动态开头 / 标题动画模板 —— 纯前端、零依赖、双击即播，全部提炼自动效工程实战。

> 每个模板都是一份自包含的 HTML：文字、配色、时长等参数**直接用代码就能改**（文件内即有配置对象），改完刷新即见效果。`demo.mp4` 是逐个实录的效果样片，`preview.png` 为落定帧封面。

## 模板一览

| # | 模板 | 规格 | 在线预览 | 效果视频 |
|---|------|------|----------|----------|
| 01 | Cyber 章节卡 | 1280×720 | [打开](demos/cyber/cyber-chapter-card.html) | [demo.mp4](demos/cyber/demo.mp4) |
| 02 | Cyber2 开场 | 2048×1152 | [打开](demos/cyber2/part02-opener.html) | [demo.mp4](demos/cyber2/demo.mp4) |
| 03 | 霓虹电路 | 2048×1152 | [打开](demos/neon/neon-circuit.html) | [demo.mp4](demos/neon/demo.mp4) |
| 04 | MOTION 文字弹球 | 1280×720 | [打开](demos/motion/motion-wipe.html) | [demo.mp4](demos/motion/demo.mp4) |
| 05 | 云朵弹跳 | 1280×720 | [打开](demos/cloudpop/cloud-pop.html) | [demo.mp4](demos/cloudpop/demo.mp4) |
| 06 | Opener 开场 | 1920×1080 | [打开](demos/opener/opener.html) | [demo.mp4](demos/opener/demo.mp4) |
| 07 | 芯片弹跳 | 1280×720 | [打开](demos/schema/chip-pulse_tpl.html) | [demo.mp4](demos/schema/demo.mp4) |
| 08 | 网格标题 | 1920×1080 | [打开](demos/gridblue/grid-blue-open.html) | [demo.mp4](demos/gridblue/demo.mp4) |
| 09 | 蓝图制图台 | 1920×1080 | [打开](demos/draftdesk/draft-desk.html) | [demo.mp4](demos/draftdesk/demo.mp4) |
| 10 | 黑金突入 | 1920×1080 | [打开](demos/helldive/hell-dive.html) | [demo.mp4](demos/helldive/demo.mp4) |
| 11 | 竹窗苔原 | 1920×1080 | [打开](demos/mosswin/moss-window.html) | [demo.mp4](demos/mosswin/demo.mp4) |
| 12 | 薄荷撞色 | 1920×1080 | [打开](demos/popmint/pop-mint.html) | [demo.mp4](demos/popmint/demo.mp4) |
| 13 | 半调套印 | 1920×1080 | [打开](demos/pressht/press-halftone.html) | [demo.mp4](demos/pressht/demo.mp4) |
| 14 | 莫兰迪柔雾 | 1920×1080 | [打开](demos/blushm/blush-morandi.html) | [demo.mp4](demos/blushm/demo.mp4) |
| 15 | 液态铬镜 | 1920×1080 | [打开](demos/liqchr/liquid-chrome.html) | [demo.mp4](demos/liqchr/demo.mp4) |
| 16 | 金缮合缝 | 1920×1080 | [打开](demos/gsam/gold-seam.html) | [demo.mp4](demos/gsam/demo.mp4) |
| 17 | 黑胶落针 | 1920×1080 | [打开](demos/vinyl/vinyl.html) | [demo.mp4](demos/vinyl/demo.mp4) |
| 18 | 纸层隧道 | 1920×1080 | [打开](demos/pcut/paper-cut.html) | [demo.mp4](demos/pcut/demo.mp4) |
| 19 | 极坐标徽 | 1920×1080 | [打开](demos/mb/mission-badge.html) | [demo.mp4](demos/mb/demo.mp4) |
| 20 | 黄铜表 | 1920×1080 | [打开](demos/bz/brass-gauge.html) | [demo.mp4](demos/bz/demo.mp4) |

也可以从[画廊首页](index.html)点卡片浏览。

## 用代码改文案 / 参数（这是重点）

每个模板内部都有配置对象，改一行刷新即生效，不用碰动画代码。例如：

**云朵弹跳**（`demos/cloudpop/cloud-pop.html`）：

```js
let cfg={title:'BEYOND\nCLOUD',sub:'',part:'名称1',partTag:'Part.01',br:'名称2'};
```

**黄铜表**（`demos/bz/brass-gauge.html`）：

```js
var cfg={part:'Part.02', title:'满格压力', sub:'AT FULL SCALE', img:''};
```

常见可改项：`title`（主标题，支持 `\n` 换行）、`sub`（副标题）、`part` / `partTag`（章节号）、`img`（贴图地址）等。其余风格参数（配色、速度、字体）在文件顶部 `:root` CSS 变量或 `const` 常量区，同样可以直接改。

Cyber 系列还支持 **postMessage 驱动**（`cyber-cfg{part,title,sub}` / `cyber-color{vars}`），可以把模板嵌进你自己的页面、由外部程序实时喂参数。

## 目录结构

```
animated-title-templates/
├── index.html                      # 画廊首页（卡片墙）
├── README.md
├── LICENSE                         # MIT
└── demos/<slug>/                   # 每个模板一个目录
    ├── <原文件名>.html              # 模板源码（单文件，可直接双击打开）
    ├── demo.mp4                    # 实录效果样片（与源码同分辨率 / 30fps）
    └── preview.png                 # 落定帧封面
```

## 本地使用

克隆后直接双击任意 HTML 即可播放（无需构建、无外部依赖）；要挂到自己的站点上，把对应 `demos/<slug>/` 目录整个拷走即可。

## License

[MIT](LICENSE)
