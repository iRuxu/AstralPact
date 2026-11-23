# 狼王

## 背景与职责

- 职责：**证券（非银金融）**（按用户2026-11-19指定）。
- 背景：代表证券及非银金融一方，带领群狼出席内廷会议。
- 固定识别点：银灰长鬃毛、狼吻、直立尖耳、金色眼睛，红宝石金冠、黑色金边礼服外套、酒红马甲与领带、白衬衫、金链、黑裤皮鞋及蓬松狼尾。
- 设定来源：[世界观与角色](../../../../docs/世界观与角色.md)、[角色美术设定](../../../../docs/角色美术设定.md)。

## 文件入口

| 类别 | 文件或目录 | 当前情况 |
| --- | --- | --- |
| 原画三视图 | [2d-turnaround.png](2d-turnaround.png) | 1774×887，原文件名 `狼王-独立三视图.png` |
| 3D三视图 | [3d-turnaround.png](3d-turnaround.png) | 1536×1024，3:2，结合特写新绘，待审阅 |
| 历史修改 | [archive/](archive/) | 预留旧图归档；生成记录存入本角色 archive/生成记录/ |
| 音色参考 | [狼王.mp3](voice/index.mp3) | 配音连续性参考 |
| 特写 | [06-狼王特写.png](portraits/06-狼王特写.png) | 1672×941，议会厅CG参考 |

## 当前使用约定

原画锁定身份、服装结构、全身比例和物种特征；议会厅特写锁定当前CG面部、材质、光照与细节。默认精细3D电影CG，具体沿用项目[3D制作规范](../../../../docs/3D电影CG风格与生成工作流.md)。2026-11-19已结合议会厅特写补齐3D三视图，尚待用户审阅。

当前3D三视图命名为 `3d-turnaround.png`；新增特写可按视角、表情或服装变体命名并放入 `portraits/`。替换当前图片前先将旧图及对应记录放进 `archive/`，不复制原画冒充3D图。

## 实际生成词与来源

特写记录摘录自 [议会厅v2生成记录](../../../../storyboard/第一集-负和游戏/第二场-议会厅/v2/archive/生成记录/生成记录.json)，本地留存于 [历史生成记录](archive/生成记录/特写历史生成记录.json)。渠道为内置 image_gen；模型、seed与质量档位未暴露。历史参考路径仅表示当时附图，当前素材以本README入口为准。

### 特写实际提示词

```text
Use case identity-preserve. ONE landscape16:9 finished cinematic film CG storyboard character closeup, no panels. Image1 AUTHORITATIVE character identity costume and anatomy, if drawing convert rendering only retaining exact design; Image2 same council room geometry and background; Image3 ONLY refined CGI style material detail and lighting, NEVER copy queen species face horns jewelry or white dress. Seated RIGHT NEAR, threequarter medium closeup head chest and hands resting on closed trading ledger at blackgold table, faces screen LEFT to king. Exact crowned SILVERGRAY wolf with long layered graywhite mane cheek fur, upright wolf ears golden eyes thin dark eye contour small antiquegold crown red gemstones, black goldtrim tailored longcoat burgundy waistcoat darkred tie white shirt smallgold lapel pin. Confident worldly slightly sardonic expression lips closed, mature slim upright body not bulky. Background blurred RIGHT darkgold cabinetry and narrow jade panels. High-end feature-film 3D CGI, natural dimensional face anatomy, finely resolved scales fur or wrinkles appropriate to species, convincing cloth weight and folds, raised embroidery only where costume includes it, distinct metal leather pearlstone surfaces. Soft warm key motivated by palace lamps, subtle coolblue window fill, readable facial planes and dark clothing, restrained specular and controlled bloom. Crisp natural fine detail match approved queen closeups, not illustration paper grain celshading plastic videogame or painterly smear. Calm seated council listening portrait, shallow background depth but full face and identifying details sharp. Headgear ears horns fully within comfortable margins. NO text subtitles watermark extra characters or collage.
```

### 原画独立三视图实际提示词

```text
Use case: identity-preserve. 编辑参考原图，生成狼王独立角色三视图。严格保留上方狼王的既有形象：灰色长鬃毛、威严狼脸、金色眼睛、红宝石金色王冠、黑色金边长礼服外套、酒红马甲与领带、白衬衫、金链、黑裤黑皮鞋、灰色蓬松狼尾。仅移除下方整个小狼插图框及三只小狼，将狼王三视图重新居中铺满横幅画面：从左到右正面、严格侧面、背面，三个全身同等比例同一水平基线，耳朵王冠脚尾完整，保留原图二维暗色动画设定稿画风、细致线稿与灰米色纸纹背景。无文字无边框，无其他角色；不能改变狼王服装、体型或面容。
```

## 本次3D补绘

保留特写的银灰鬃毛、金眼和红宝石金冠，按原画重建全身黑金礼服、酒红马甲、金链和狼尾。目视三角度头冠、双手、双腿及鞋完整。原生1536×1024，未放大，内置image_gen。实际提示词、附图顺序及检查记录见 [3D三视图生成记录](archive/生成记录/3D三视图-生成记录.json)。
