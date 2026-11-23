# 龙王

## 背景与身份

龙族王室的幕后统治者，在宫殿内廷召集议事。

东方龙头、炭黑鳞片、分枝金角、黑色鬃须、金色眼睛；黑金冕服、垂珠冠、宽肩披领、腰部饰扣及厚重长尾。

背景依据：[世界观与角色](../../../../docs/世界观与角色.md)；外形依据：[角色美术设定](../../../../docs/角色美术设定.md)。不从服饰画面反推或新增剧情设定。

## 文件入口

| 类别 | 位置 | 用途 |
| --- | --- | --- |
| 原画三视图 | [2d-turnaround.png](2d-turnaround.png) | 造型、服装结构与全身比例 |
| 3D三视图 | [3d-turnaround.png](3d-turnaround.png) | 当前全身CG参考，1536×1024、3:2 |
| 历史修改 | [archive/](archive/) | 旧图与历史生成记录，不能覆盖当前版本 |
| 音色参考 | [voice/index.mp3](voice/index.mp3) | 配音连续性参考，不额外猜测声音参数 |
| 特写 | [portraits/](portraits/) | 可继续收纳视角、表情、服装变体；不同变体单独命名 |

## 当前版本与参考优先级

当前3D三视图由整理前的 `龙-龙王-写实3D探索.png` 改名，沿用目录现存版本。此前记录中的议会厅风格新图已不在该目录，本次未恢复；下方议会厅重绘提示词属于历史生成记录，不表示现存图由该提示词生成。

- [议会厅特写](portraits/龙王议会厅特写.png)：当前面部、鳞片鬃须及电影CG材质参考。

默认使用精细3D电影CG；特写锁面部身份、材质与光照，原画锁全身设计。龙后的帽冠及龙角采用已修订三视图，不再照抄高圆顶冠方案。新增图另存，明确替换时先归档旧图。生成渠道为内置image_gen，未暴露模型名、seed或质量档位，不编造参数。

## 生成词

完整历史记录见 [整理前生成记录](archive/2026-11-19-整理前生成记录.md)。以下保留议会厅风格重绘历史提示词（并非现存探索图的已证实生成词）。提示词中的参考编号是当次附图顺序，不是文件排序。

```text
Use case: stylized-concept. Create ONE polished 3D CGI character turnaround sheet, landscape 3:2, three complete full-body views side by side: FRONT, exact LEFT PROFILE facing left, BACK. Same Dragon King in all three, aligned crown heights and ground baseline, generous margins, complete horns, crown, claws and tails visible. No text or panel borders. Neutral warm grey seamless studio backdrop, soft contact shadows.
REFERENCE PRIORITY: Image 1 council closeup is authoritative for current facial identity, mature regal expression, dragon anatomy, elaborate branching gold horns, golden eyes, charcoal individual scales, layered black mane and beard, fine long whiskers, flat-topped black imperial crown with gold edge and hanging gold beads, red jewel, and ALL rendering/material quality. Reproduce this face and costume faithfully in full body. Image 2 original drawing is authoritative for full-body slender tall upright mature proportions, costume construction and front/profile/back arrangement: black gold cloud-and-dragon embroidered wide shoulder cape, layered long wide sleeves, geometric gold borders, beast-face belt clasp, red and gold ornaments and hanging tassels, cream and muted dark-red inner skirts, black scaled clawed feet and thick long curved black scaled tail with dark flowing tuft and subtle gold accents. Image 3 prior 3D exploration only supports continuity of full-body costume and tail structure; REBUILD with the much richer council closeup quality, don't copy its softer face or simplified materials.
High-end feature-film CGI, physically based materials, individually resolved scales and fine hair strands, raised gold-thread embroidery following woven fabric, visible thread relief rather than flat gold paint. Natural weighted dark brocade folds, distinct brushed gold metal, polished red gemstone and softly reflective beads. Soft warm key and subtle cool fill, readable dark surfaces, restrained specular, crisp natural detail across ALL THREE entire figures, no depth of field blur. Maintain identical crown, horn branching, facial identity, robe pattern placement, body proportions and accessories between views. Arms relaxed, both hands anatomical with clearly formed dragon claws, feet grounded. Back view shows long mane, cape and original large embroidered dragon on robe, tail emerges anatomically at lower back. Profile is true side-on with consistent skull and long neck, not a three-quarter pose. No throne, furniture, architecture, new accessories, human face, wings, bulky short proportions, toy plastic, painted smears, overexposure or sharpened halos. Deliver maximum native detail.
```
