# 鳄王

## 背景与职责

- 职责：**财政**（按用户2026-11-19指定）。
- 背景：财政大臣，负责预算和宫廷支出；龙后宴席超支后，将账目中的“宴饮”改记为“礼制维护”。
- 固定识别点：橄榄灰鳞片、突出长吻与鳄类轮廓，圆框眼镜、深褐官服、铜扣，红笔与预算册。
- 设定来源：[世界观与角色](../../../../docs/世界观与角色.md)、[角色美术设定](../../../../docs/角色美术设定.md)。

## 文件入口

| 类别 | 文件或目录 | 当前情况 |
| --- | --- | --- |
| 原画三视图 | [2d-turnaround.png](2d-turnaround.png) | 1536×1024，原文件名 `鳄鱼-鳄王.png` |
| 3D三视图 | [3d-turnaround.png](3d-turnaround.png) | 1536×1024，3:2，结合特写新绘，待审阅 |
| 历史修改 | [archive/](archive/) | 保存已找到的实际历史生成记录；本目录暂无历史修改图片 |
| 音色参考 | [鳄王.mp3](voice/index.mp3) | 配音连续性参考 |
| 特写 | [05-鳄王特写.png](portraits/05-鳄王特写.png) | 1672×941，议会厅CG参考 |

## 当前使用约定

原画锁定身份、服装结构、全身比例和物种特征；议会厅特写锁定当前CG面部、材质、光照与细节。默认精细3D电影CG，具体沿用项目[3D制作规范](../../../../docs/3D电影CG风格与生成工作流.md)。2026-11-19已结合各自特写补绘独立3D三视图，新稿待用户审阅。

当前3D三视图命名为 `3d-turnaround.png`；新增特写可按视角、表情或服装变体命名并放入 `portraits/`。替换当前图片前先将旧图及对应记录放进 `archive/`，不复制原画冒充3D图。

## 实际生成词与来源

特写记录摘录自 [议会厅v2生成记录](../../../../storyboard/第一集-负和游戏/第二场-议会厅/v2/archive/生成记录/生成记录.json)，本地留存于 [历史生成记录](archive/生成记录/特写历史生成记录.json)。渠道为内置 image_gen；模型、seed与质量档位未暴露。历史参考路径仅表示当时附图，当前素材以本README入口为准。

### 特写实际提示词

```text
Use case identity-preserve. ONE landscape16:9 finished cinematic film CG storyboard character closeup, no panels. Image1 AUTHORITATIVE character identity costume and anatomy, if drawing convert rendering only retaining exact design; Image2 same council room geometry and background; Image3 ONLY refined CGI style material detail and lighting, NEVER copy queen species face horns jewelry or white dress. Seated RIGHT FAR, threequarter closeup head chest and hands by budgetbook redpen on blackgold table, faces screen LEFT toward king. Exact olivegray CROCODILE long snout small visible teeth ROUND GOLD spectacles, rich dark BROWN bureaucratic coat matching original gold fine edging and round brass star clasps, brown suit and tie underneath white collar. Calculating composed older official, no roaring. Detailed scute roughness, fine fabric and goldthread. Background blurred RIGHT cabinetry alternating dark wood wide bays jade narrow panels. High-end feature-film 3D CGI, natural dimensional face anatomy, finely resolved scales fur or wrinkles appropriate to species, convincing cloth weight and folds, raised embroidery only where costume includes it, distinct metal leather pearlstone surfaces. Soft warm key motivated by palace lamps, subtle coolblue window fill, readable facial planes and dark clothing, restrained specular and controlled bloom. Crisp natural fine detail match approved queen closeups, not illustration paper grain celshading plastic videogame or painterly smear. Calm seated council listening portrait, shallow background depth but full face and identifying details sharp. Headgear ears horns fully within comfortable margins. NO text subtitles watermark extra characters or collage.
```

## 3D三视图补绘（2026-11-19）

目视检查正面、左侧面、背面完整；可见裤腿、鞋与地面承托，保留特写面部和原画服装道具。 原生1536×1024，未放大。采用内置image_gen，模型与质量参数未暴露。完整实际提示词、参考顺序和修订记录见 [3D三视图生成记录](archive/生成记录/3D三视图-生成记录.json)。新稿尚未标记为用户已确认。
