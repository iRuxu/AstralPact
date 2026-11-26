# 大象 · 未央

## 背景与职责

- 职责：**央行**（按用户2026-11-19指定）。
- 背景：央行代表，以象鼻喷水表现释放流动性。
- 固定识别点：大象宽耳、长鼻、象牙与厚重体量，金框圆眼镜、蓝灰西装、黄铜阀门胸针。
- 设定来源：[世界观与角色](../../../../docs/story/世界观与角色.md)、[角色美术设定](../../../../docs/art/角色美术.md)。

## 文件入口

| 类别 | 文件或目录 | 当前情况 |
| --- | --- | --- |
| 原画三视图 | [2d-turnaround.png](2d-turnaround.png) | 1536×1024，原文件名 `大象-未央.png` |
| 3D三视图 | [3d-turnaround.png](3d-turnaround.png) | 1536×1024，3:2，结合特写新绘，待审阅 |
| 历史修改 | [archive/](archive) | 保存已找到的实际历史生成记录；本目录暂无历史修改图片 |
| 音色参考 | 暂缺，目录已预留；未创建或推断音色 | 配音连续性参考 |
| 特写 | [03-未央特写.png](portraits/03-未央特写.png) | 1672×941，议会厅CG参考 |

## 当前使用约定

原画锁定身份、服装结构、全身比例和物种特征；议会厅特写锁定当前CG面部、材质、光照与细节。默认精细3D电影CG，具体沿用项目[3D制作规范](../../../../docs/art/3D电影CG风格与生成工作流.md)。2026-11-19已结合各自特写补绘独立3D三视图，新稿待用户审阅。

当前3D三视图命名为 `3d-turnaround.png`；新增特写可按视角、表情或服装变体命名并放入 `portraits/`。替换当前图片前先将旧图及对应记录放进 `archive/`，不复制原画冒充3D图。

## 实际生成词与来源

特写记录摘录自 [议会厅v2生成记录](../../../../storyboard/第一集-负和游戏/第二场-议会厅/v2/archive/生成记录/生成记录.json)，本地留存于 [历史生成记录](archive/生成记录/特写历史生成记录.json)。渠道为内置 image_gen；模型、seed与质量档位未暴露。历史参考路径仅表示当时附图，当前素材以本README入口为准。

### 特写实际提示词

```text
Use case identity-preserve. ONE landscape16:9 finished cinematic film CG storyboard character closeup, no panels. Image1 AUTHORITATIVE character identity costume and anatomy, if drawing convert rendering only retaining exact design; Image2 same council room geometry and background; Image3 ONLY refined CGI style material detail and lighting, NEVER copy queen species face horns jewelry or white dress. Seated at LEFT FAR council seat, medium closeup head ears upperbody two hands on closed dark ledger at table edge, subtly faces screen RIGHT toward head of table. Exact gray elephant adult broad ears long trunk curved ivory tusks ROUND GOLD glasses slateblue threepiece business suit white shirt navy tie brass VALVE WHEEL brooch on lapel, pocket square. Wise serious reserved accountant. Delicate natural skin wrinkles, woven wool weave. Trunk naturally down not extra limb. Background blurred LEFT window sea city ivory ribs, consistent left-window light. High-end feature-film 3D CGI, natural dimensional face anatomy, finely resolved scales fur or wrinkles appropriate to species, convincing cloth weight and folds, raised embroidery only where costume includes it, distinct metal leather pearlstone surfaces. Soft warm key motivated by palace lamps, subtle coolblue window fill, readable facial planes and dark clothing, restrained specular and controlled bloom. Crisp natural fine detail match approved queen closeups, not illustration paper grain celshading plastic videogame or painterly smear. Calm seated council listening portrait, shallow background depth but full face and identifying details sharp. Headgear ears horns fully within comfortable margins. NO text subtitles watermark extra characters or collage.
```

## 3D三视图补绘（2026-11-19）

目视检查正面、左侧面、背面完整；可见裤腿、鞋与地面承托，保留特写面部和原画服装道具。 原生1536×1024，未放大。采用内置image_gen，模型与质量参数未暴露。完整实际提示词、参考顺序和修订记录见 [3D三视图生成记录](archive/生成记录/3D三视图-生成记录.json)。新稿尚未标记为用户已确认。
