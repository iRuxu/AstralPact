# 蜘蛛 · 八爪

## 背景与职责

- 职责：**情报**（按用户2026-11-19指定）。
- 背景：王室情报总管，梳理宫内外消息与关系，能从鹦鹉直播的新词追查消息出处。
- 固定识别点：深紫灰色蜘蛛面部、多眼与原图口器轮廓；精致盘发、珍珠金饰、深紫金色蛛网纹礼服、大钻戒，人形双手及八根背部附肢。沿用蜘蛛贵妇形象，不改成人脸。
- 设定来源：[世界观与角色](../../../../docs/世界观与角色.md)、[角色美术设定](../../../../docs/角色美术设定.md)。

## 文件入口

| 类别 | 文件或目录 | 当前情况 |
| --- | --- | --- |
| 原画三视图 | [2d-turnaround.png](2d-turnaround.png) | 1536×1024，原文件名 `蜘蛛-八爪.png` |
| 3D三视图 | [3d-turnaround.png](3d-turnaround.png) | 1536×1024，3:2，结合特写新绘，待审阅 |
| 历史修改 | [archive/](archive/) | 保存已找到的实际历史生成记录；本目录暂无历史修改图片 |
| 音色参考 | [蜘蛛.mp3](voice/index.mp3) | 配音连续性参考 |
| 特写 | [04-八爪特写.png](portraits/04-八爪特写.png) | 1672×941，议会厅CG参考 |

## 当前使用约定

原画锁定身份、服装结构、全身比例和物种特征；议会厅特写锁定当前CG面部、材质、光照与细节。默认精细3D电影CG，具体沿用项目[3D制作规范](../../../../docs/3D电影CG风格与生成工作流.md)。2026-11-19已结合各自特写补绘独立3D三视图，新稿待用户审阅。

当前3D三视图命名为 `3d-turnaround.png`；新增特写可按视角、表情或服装变体命名并放入 `portraits/`。替换当前图片前先将旧图及对应记录放进 `archive/`，不复制原画冒充3D图。

## 实际生成词与来源

特写记录摘录自 [议会厅v2生成记录](../../../../storyboard/第一集-负和游戏/第二场-议会厅/v2/archive/生成记录/生成记录.json)，本地留存于 [历史生成记录](archive/生成记录/特写历史生成记录.json)。渠道为内置 image_gen；模型、seed与质量档位未暴露。历史参考路径仅表示当时附图，当前素材以本README入口为准。

### 特写实际提示词

```text
Use case identity-preserve. ONE standalone landscape16:9 cinematic film CG still, elegant SPIDER NOBLEWOMAN Bachua seated at LEFT NEAR seat of same council room, medium closeup face shoulders waist and TWO hands resting at blackgold table edge, threequarter body turned slightly toward screen RIGHT toward king. Image1 authoritative exact character identity anatomy attire: dark purplegray genuine SPIDER FACE multiple glossy blackgold eyes and distinct original mandible contours, NOT human nose lips chin and NOT hairy tarantula; sophisticated mature graceful dignity. Ornate dark sculpted bun pearl chains gold floral hairpieces, pearl earrings necklaces, rich deep plum gown gold raised WEB embroidery shawl and magnificent clear faceted diamond ring on one hand, ring clearly visible. TWO humanlike arms/hands plus exactly SIX jointed spider appendages connected to BACK, 3 per side, fold gracefully around chair; do not grow extra hands. Keep visible head and hair complete with margin, dignified slim upright torso. Image2 room reference background LEFT windows blue coastal city consistent, warmgold white flowing ribs and blackgold chair, shallow blur. Image3 ONLY high-end dimensional CGI quality soft warm key coolblue fill precise strands pearls embroidery nuanced chitin roughness, do NOT copy queen horns muzzle white scales or gown. Beauty with inhuman spider identity, no smile grotesque teeth or horror gore. Camera at seated eye level, subject face clear and poised listening, no dialogue text labels collage watermark.
```

## 3D三视图补绘（2026-11-19）

目视检查正面、左侧面、背面完整；八根背部附肢（左右各四）及两只手保留，钻戒、多眼、盘发与紫金礼服可见。 原生1536×1024，未放大。采用内置image_gen，模型与质量参数未暴露。完整实际提示词、参考顺序和修订记录见 [3D三视图生成记录](archive/生成记录/3D三视图-生成记录.json)。新稿尚未标记为用户已确认。

## 当前附肢约定（2026-11-19用户修正）

八爪指八根背部蜘蛛附肢，左右各四根，另保留两只人形手臂。此设计致敬《权力的游戏》。坐姿特写可自然遮住最下方两根，不要求每个镜头露出全部八根，不因遮挡删减角色结构。当前3D三视图已恢复八附肢版本，六附肢修改版归档至 `archive/六附肢旧版/`。上方历史特写实际提示词中的SIX为旧生成原文，已失效，不能作为后续数量依据；本次直接恢复已有图，未重新生成。
