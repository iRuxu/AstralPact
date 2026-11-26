# 龙后

## 背景与身份

龙族王室成员，掌宫中仪典与宴赏；在故事中代表挥霍公帑的一派，把日常排场记入公账。

象牙白鳞片、青玉分枝角、碧绿眼睛、银白盘髻与长发；象牙白金绣宴服、墨青内衬、珠肩、青玉冠饰与印戒、青玉色龙尾。

背景依据：[世界观与角色](../../../../docs/story/世界观与角色.md)；外形依据：[角色美术设定](../../../../docs/art/角色美术.md)。不从服饰画面反推或新增剧情设定。

## 文件入口

| 类别 | 位置 | 用途 |
| --- | --- | --- |
| 原画三视图 | [2d-turnaround.png](2d-turnaround.png) | 造型、服装结构与全身比例 |
| 3D三视图 | [3d-turnaround.png](3d-turnaround.png) | 当前全身CG参考，1536×1024、3:2 |
| 历史修改 | [archive/](archive) | 旧图与历史生成记录，不能覆盖当前版本 |
| 音色参考 | [voice/index.mp3](voice/index.mp3) | 配音连续性参考，不额外猜测声音参数 |
| 特写 | [portraits/](portraits) | 可继续收纳视角、表情、服装变体；不同变体单独命名 |

## 当前版本与参考优先级

当前采用冠角局部修订版（原文件名 `母龙-龙后-特写统一3D三视图-v2.png`），用户已认可。保留新版脸型、侧面龙须位置和花朵；帽冠与龙角按旧版修正。

- [低眸侧颜](portraits/05-龙后低眸侧颜.png)：用户满意的侧脸、鳞片、发丝及材质参考。
- [抬眼询问](portraits/07-龙后抬眼询问.png)：用户满意的脸型、眼睛与珠玉细节参考。
- 当前目录未保留09等待回应，本次未恢复。

默认使用精细3D电影CG；特写锁面部身份、材质与光照，原画锁全身设计。龙后的帽冠及龙角采用已修订三视图，不再照抄高圆顶冠方案。新增图另存，明确替换时先归档旧图。生成渠道为内置image_gen，未暴露模型名、seed或质量档位，不编造参数。

## 生成词

完整历史记录见 [整理前生成记录](archive/2026-11-19-整理前生成记录.md)。以下保留当前冠角修订的实际提示词。提示词中的参考编号是当次附图顺序，不是文件排序。

```text
Edit Image 1 with a strictly localized correction ONLY to crown/headpiece and jade dragon horns in all three views. Preserve the rest of Image 1 unchanged: exact beautiful face, eye shape, snout profile, whisker origin and curve, ivory flower position and petal design, hair and bun, pearl strands, body, costume, embroidery, lighting, framing and background.
Image 1 is the EDIT TARGET current turnaround. Image 2 is authoritative ONLY for the correct OLD crown shape and dragon horn structure. Images 3 and 4 are facial beauty and detailed material protection references, NOT crown shape authority.
Replace the incorrect tall hemispherical cage/dome hat and its tall pearl finial in Image 1 with Image 2's low close-fitting imperial tiara: an upright ornate scalloped fan/leaf-shaped gold filigree crest nestled into the hair between the horns, narrow in side profile, dark inset backing, central oval jade jewel, pearl clusters, modest pearl nested within the crest. Match Image 2's silhouette, height relative to head, forehead attachment and three-view geometry. NO spherical cage, no raised hemisphere over the skull, no tall spire or pearl standing above the crest, no separate round cap visible at the back. Back view must follow Image 2's low crown visibility behind the hair rather than a tall dome.
Restore horns to Image 2's elegant long slender sage-jade branching antlers: symmetrical pair rooted at sides of upper skull, sweeping outward and upward in front/back views, backward in profile, slender tapering main curve and sparse graceful tapered branches. Match Image 2's exact relative length and branching silhouette, avoid short thick horizontal antlers. Retain subtle translucency and physical jade quality of target.
Crucial: do not revert the face, whiskers, flowers, hair or robe to Image 2. The user's preferred prettier face and correct whisker/flower placement are in Image 1, with Images 3-4 supporting identity. Keep the complete three full-body front/left-profile/back arrangement and original 3:2 composition. High-end feature-film CGI, crisp natural details, physically based materials, individually resolved scales/hair, raised gold thread, distinct pearl and jade response. No text. Change only headpiece and horns.
```

当次附图：修订前v2（现位于archive/三视图v2修订前/）→ 旧版写实3D高清（同归档目录）→ portraits/05低眸侧颜 → portraits/07抬眼询问。
