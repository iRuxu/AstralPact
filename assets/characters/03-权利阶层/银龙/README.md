# 银翼 · 银龙 · 银行

## 补绘原画三视图（2026-11-19）

使用内置image_gen，唯一参考为本目录已认可的 `3d-turnaround.png`，锁身份和服装，转换为细致线稿、柔和分色及纸纹的2D设定稿。原生1536×1024，3:2，未放大。目视三个全身角度完整，冠角、手脚和尾部入画，服饰与CG版本一致；细节存在生成差异，非精确建模图。

### 实际原画提示词

```text
Use case: style-transfer / identity-preserve. Create the HAND-DRAWN ORIGINAL CHARACTER DESIGN turnaround counterpart to the attached APPROVED CGI Silver Dragon. Exactly preserve this young adult handsome male Eastern silver dragon's identity, elegant long snout and neck, ice blue eyes, silver-white individual scales, swept-back short silver mane, silver branching antler silhouette, delicate muzzle whiskers, tall slender adult male proportions, long scaled silver tail with flowing silver tuft. Preserve EXACT midnight navy tailored three-piece suit, mid-thigh jacket, waistcoat, silver buttons, white shirt, silver-blue tie, small silver coin lapel pin, pocket square, trousers and black formal shoes. Do not redesign or add crown, robes, jewelry, wings, props or characters.
Render as beautiful finished 2D hand-drawn animated-film concept art: refined clear ink/pencil contour lines, deliberate fine internal linework defining scales and hair, controlled painted shading in soft cel-shaded planes, nuanced muted color, visible gentle warm grey-beige paper grain, tactile illustration rather than photoreal CGI. Rich clean drawing precision, sophisticated attractive face and readable tailoring. Keep silver scales luminous but not chrome. Front, strict left profile facing left, back, complete full bodies side by side in same order and proportions as reference, same ground baseline and figure heights, full horn tips, tails and shoes uncropped with margins. Landscape 3:2 character sheet on plain warm grey-beige paper, subtle grounding shadows, no panel borders, no labels, no text or watermark. Three views of the SAME approved character, preserve identity and costume details. This is a 2D original art style version, not another 3D render or a pencil filter overlay.
```


## 身份与当前设计

- 用户确定：姓名为**银翼**，银龙、青年男龙，代表银行；参考龙后的美术风格。
- 当前新稿：银白细鳞、银色分枝龙角、冰蓝眼睛、向后梳理的银白鬃发、修长龙首与长尾；深海军蓝三件套、银蓝领带、银色钱币形胸针、黑皮鞋。
- 用户已认可本轮3D造型；原画版依此转换为手绘表现，新原画待审阅。
- 与大象未央（央行）、狼王（证券／非银金融）分别记录；具体银行类型、职务与王室亲缘关系未定，不从龙族外形推断。
- 本次只生成二维3D风格图片，不含可编辑3D模型。

## 文件入口

| 类别 | 位置 | 状态 |
| --- | --- | --- |
| 原画三视图 | [2d-turnaround.png](2d-turnaround.png) | 按认可CG造型补绘的2D手绘版，1536×1024 |
| 3D三视图 | [3d-turnaround.png](3d-turnaround.png) | 本次新稿，1536×1024，3:2 |
| 历史修改 | [archive/](archive) | 预留，尚无旧稿 |
| 音色参考 | [voice/](voice) | 预留，尚无音色 |
| 特写 | [portraits/](portraits) | 预留，尚无独立特写 |

## 生成与验收

2026-11-19，内置 image_gen，原生1536×1024，未放大；工具未暴露模型名、seed或质量档位。目视正面、左侧面和背面完整，角、手、鞋及尾巴入画，裤腿和落地承托清楚。侧背视图细小结构仍可能有生成差异，非精确建模结构图。待用户审阅。

实际附图顺序：
1. [龙后当前3D三视图](../../01-龙族王室/龙后/3d-turnaround.png)：龙族比例、全身CG完成度；不复制女性身份和服装配饰。
2. [龙后抬眼特写](../../01-龙族王室/龙后/portraits/007-龙后抬眼询问.png)：面部美感、鳞片发丝、物理材质和柔暖主光／冷补光。

## 实际提示词

```text
Use case: stylized-concept. Design a NEW young adult MALE SILVER EASTERN DRAGON, representing banking in the same animal-fable universe as the reference Dragon Queen. ONE polished full-body character turnaround sheet, landscape 3:2, exactly three views side by side: FRONT, true LEFT PROFILE facing left, BACK. Same character and clothes in all rotations, aligned heights and ground baseline, complete horns, feet, hands and long tail with margins. Neutral warm grey studio backdrop, subtle floor contact shadows, no text or borders.
Reference 1 Dragon Queen turnaround: use ONLY graceful upright anthropomorphic Eastern dragon anatomy, refined proportions and cohesive premium CGI finish, not her female identity, jewelry, hairdo or dress. Reference 2 Queen closeup: PRIMARY for refined attractive dragon facial design, individually resolved tiny scales, delicate sculpted cheek mane, hair strands, realistic material separation and soft warm key/cool fill. Adapt to a distinct handsome young adult male, late twenties equivalent, poised intelligent attentive expression, subtly stronger jaw and brow, elegant long dragon snout, alert ice-blue eyes, long graceful neck, slender athletic tall body. Entire head remains a dragon, not human. Pearlescent SILVER-WHITE scales with natural soft grey recesses, not chrome armor. A pair of elegant backward/upward swept branching silver antlers, cool ivory-silver organic texture; neatly swept back SILVER hair/mane ending around nape/upper shoulders, no long elderly beard, fine short whiskers at muzzle sides. Clear youth and masculine refinement, no elderly face.
Costume: distinguished young banker, precisely tailored midnight-navy three-piece formal suit, white shirt, muted silver-blue silk tie, elegant fitted long suit jacket ending around mid-thigh, waistcoat and fully visible matching trousers, black polished formal shoes shaped to accommodate dragon feet. Understated silver buttons and a small silver circular coin-inspired lapel pin with simple geometric center, no lettering, no bank brand, no crown. Hands relaxed at sides, pale silver scaled clawed fingers. Restrained professional luxury, no queen's pearl drapes, earrings, flower ornaments, gold crown, imperial robe or excessive embellishment. Long silver-scaled dragon tail emerges anatomically from a tailored rear opening, curves clearly beside body without obscuring feet, soft silver hair tuft, consistent through views. Back view clearly resolves jacket split, two trouser legs and tail attachment. Slim upright posture, not bulky, no wings.
High-end feature-film CGI, physically based materials, individually resolved scales/hair, fine wool weave and tailored seams, believable fabric weight, silk tie luster, distinct subtle brushed silver metal and polished leather response. Soft warm key with subtle cool fill, crisp natural detail in all three full-body views, no depth of field blur. Attractive elegant expressive face consistent with the reference's artistry while distinctly young MALE. No toy plastic, flat cel shading, paper grain, painterly smear, overexposure, mirror-chrome body, extra limbs or hidden missing legs. Maximum native detail.
```

