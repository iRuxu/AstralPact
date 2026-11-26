# 3D电影CG风格与生成工作流

## 当前确定的方向

用户认可第一集宫殿开场v2这一批分镜，并明确要求后续继续使用这种3D风格。它是**精细、优雅、具有可信体积与物理材质的电影CG**：有美术设计的动物拟人角色、细腻鳞片和毛发、厚重织物、立体刺绣与可区分的珠玉金属。交付仍为二维图片，不包含3D模型。

新角色、场景、道具及分镜默认采用本规范。旧手绘立绘保留为造型设计资料，明确要求普通手绘版本时再用对应手绘规范；无需因此重做已有资产。龙后的美感和宫殿的奢华属于特定角色与场景，不应让普通居民都穿金绣礼服。

## 为什么这次看起来更清晰

这次可确认的操作是：内置image_gen、实际附上角色与场景参考、分镜逐张生成、用新近景锁定后续身份和材质、发现旧图混入早期造型后重新绘制。没有证据表明是某个后台模型突然升级，也没有使用额外的付费高清开关或后期超分流程。

可复用的关键在于：

- 将“高级3D”拆成可见特征：逐片鳞片、分束发丝、金线凸起、珍珠柔润、玉石半透和金属粗糙度差异。
- 让已认可的新成图负责渲染风格；旧图只负责特定构图，防止把旧图模糊的纹理和过时角色一并带回来。
- 柔暖主光加少量冷色补光，让面颊、衣褶与暗部都有体积；控制泛光和过曝。
- 单镜清楚描述机位、景别、视线与动作；发现问题后针对性重绘并目视检查。

这些是本批成功流程的归纳，不是对每个提示词作用的单独实验结论。生成仍有波动，不存在仅靠一句“4K、8K”就保证质量的咒语。

## 当前风格锚点与优先级

以下路径相对项目根目录，生成时必须实际附图，而不只把路径写在正文。

| 用途 | 当前参考 |
| --- | --- |
| 精细侧颜、鳞片、发丝、织物与光线 | [05低眸侧颜](../../storyboard/第一集-负和游戏/01第一场-宫殿开场/05-龙后低眸侧颜.png) |
| 龙后面部身份、美感、珠玉与CG完成度 | [07抬眼询问](../../storyboard/第一集-负和游戏/01第一场-宫殿开场/07-龙后抬眼询问.png) |
| 最新背影、发髻、珠肩、宴服与理事桌 | [03宴后理事](../../storyboard/第一集-负和游戏/01第一场-宫殿开场/03-宴后理事.png) |
| 外立面、暖窗、窗内龙后端坐听取汇报、城景 | [02暖窗之内](../../storyboard/第一集-负和游戏/01第一场-宫殿开场/02-暖窗之内.png) |
| 独立反应、完整冠角、克制表演 | [09等待回应](../../storyboard/第一集-负和游戏/01第一场-宫殿开场/09-等待回应.png) |
| 龙后多视角结构、衣装与配饰 | [龙后3D高清三视图](../../assets/characters/01-龙族王室/龙后/3d-turnaround.png) |

07的冠顶与角尖存在裁切，只将其用于脸和材质，不继承该裁切；需要完整头饰时参考09。新03、02取代早期同名构图的默认生成参考。`v1/`、`archive/`中的旧图可锁机位，不用于覆盖新角色。议会厅和其他场景仍按各自已确认布局，不能以宫殿书房替换其结构。

角色身份以该角色最新明确选定的设计为准；表演与构图以本次镜头要求为准；风格以本规范锚点为准。三者冲突时在提示词中明确旧图仅负责哪部分，禁止简单平均所有参考。

## 通用提示词：每次保留的风格段

```text
Style: High-end feature-film 3D CGI with elegant art-directed character design,
believable volume, physically based materials and natural contact shadows.
Individually resolved scales or layered hair/fur where appropriate, fine surface
roughness variation, weighty woven fabric with convincing folds and raised
gold-thread embroidery where the approved costume includes it. Distinct material
response for warm metal, softly lustrous pearls and jade with subtle translucency.
Precise, crisp and natural detail, without oversharpening or smeared textures.

Lighting: Soft cinematic key light with subtle cool fill or rim motivated by the
scene. Readable facial planes and dark materials, restrained highlights, controlled
bloom, clear subject separation. Focus on the character and relevant props; blur
only distant background when appropriate.

Avoid: flat cel shading, comic outlines, paper grain, painterly gold smears,
plastic toy surfaces, uniform mirror gloss, blown highlights, excessive bloom,
overly orange grading, excessive depth-of-field blur, extra limbs or fingers,
unrequested redesign, text, watermark or multi-panel collage.
```

按角色删改材质：没有鳞片不添鳞片，没有金绣不加金绣。暖冷光配方用于当前宫殿，白天、街巷或普通居室按真实光源调整，保持相同完成度。

## 完整单镜模板

```text
Use case: stylized-concept [or identity-preserve for an edit].
Asset: ONE standalone cinematic storyboard still, landscape 16:9, no panels.

Reference roles and priority:
Image 1: approved latest CGI frame, PRIMARY for rendering quality and materials.
Image 2: target character design, authoritative for species, face, anatomy,
proportions, costume, colors and accessories. Do not borrow Image 1's identity.
Image 3: approved environment, authoritative for architecture, props and lighting.
[Image 4: old shot, ONLY for camera placement; do not copy obsolete characters
or soft rendering from it.]

Shot: [镜号、景别、镜头所处位置、主体朝向、视线与画外对象].
Action and expression: [这个瞬间具体在做什么，表情的细微变化].
Identity invariants: [该角色固定识别点，配饰位置与拟人程度].
Composition: [人物占比、视线留白、冠角/尾翼是否全入画、对焦位置].
Environment continuity: [门窗、桌椅、道具的固定关系].

[插入上方通用风格段，按实际镜头调整材质与光照。]

Output: Use the highest available native detail. Desired framing is 16:9.
Do not substitute a collage. No captions or watermark.
```

本模板的比例和细节是生成要求，实际尺寸仍需读文件。参考图按提示词顺序传入，不能写Image 1却实际附另一张。可参考本次实际使用的[02听取汇报提示词](../../storyboard/第一集-负和游戏/01第一场-宫殿开场/archive/02听取汇报修订.md)、[03与09提示词](../../storyboard/第一集-负和游戏/01第一场-宫殿开场/archive/03与09修订记录.md)。

### 旧图重绘的补充段

```text
Regenerate this shot as a new pristine detailed cinematic CG render, not an
upscale or a softened copy. Preserve the specified camera and scene layout only.
Use the approved NEW references for current character identity and rendering.
Rebuild fine hair strands, scales, embroidery and jewelry with distinct materials.
Replace obsolete character designs and staging explicitly described below:
[明确列出应替换的人物、服饰或陈设].
```

### 等待反应镜头的补充段

```text
Create a distinct next reaction shot after the character has finished speaking.
Preserve exact identity, costume, lighting, camera side and offscreen gaze target.
[Lower chin slightly; subtly lower upper eyelids while eyes stay open; softly
press lips closed; shift to a slightly wider framing with complete headwear.]
The difference must be visible in pose or expression, not just a duplicate file
or a crop. Keep the emotion restrained and appropriate to the scene.
```

## 尺寸、比例与精度验收

| 项目 | 默认要求与实际基准 |
| --- | --- |
| 横向分镜 | 目标16:9；本批实际1672×941，约16:9 |
| 角色三视图 | 目标3:2；全身与突出部位完整，实际尺寸逐张记录 |
| 清晰度 | 达到上述新版样张的主体细节，鳞片、发丝、织物、玉石与金属可分辨 |
| 实际4K | 仅当用户要求或渠道实际返回相应尺寸时按文件验收；1672×941不得称4K |
| 放大或裁切 | 另存并记录处理方式，保留原生输出，不静默拉伸或伪称原生高分辨率 |

本次并没有在工具参数中设置成功的精确宽高或质量档位；不要编造seed、采样器、步数、模型版本或质量开关。提示词写“maximum resolution”不等于工具确实输出更大图。

内置工具可能返回近似比例和不同尺寸。用户未指定固定像素时，使用本批作为默认验收样张；低于本批尺寸或明显不清晰的结果不得无说明标为同等高清。用户指定1920×1080或3840×2160时，分别核对真实宽高；当前渠道未实现就说明差距，采用已授权且可用的处理流程，不能静默换渠道。即使尺寸相同也要检查画面细节，不以文件大小代替视觉验收。

## 执行流程

1. 读当前AGENTS、本规范及相关设定；查看当前目录，确认文件是否已移动，避免引用不存在的旧路径。
2. 打开目标图、最新角色图与风格锚点，明确本次镜头与不变项。新镜头通常选2至3张相关参考，不堆所有历史版本。
3. 普通生成默认用内置image_gen；用户指定渠道则用对应技能。普通任务不自行改用CLI/API，也不猜工具未提供的控制项。
4. 先做关键近景，确定面部与材质；同场其他机位附上该已认可帧及相应空间参考，避免只引用连续改图造成漂移。
5. 一镜一图。多图可独立提交，存在依赖的角色或空间修订按顺序执行。不要把十个镜头塞进一张网格图代替独立文件。
6. 查看每张返回图。核对面部、角冠、发髻、首饰、肢体、服装、冷暖光、主体对焦；检查同场门窗、书柜、道具、视线轴线。动物寓言不擅自引入真人侍从。
7. 关键问题重绘；要求“稍有区别”的镜头也必须有实际表演变化。检查重复文件可辅助核验，但哈希不同不能代替目视。
8. 查看实际尺寸与比例。精细不等于大像素；记录原生尺寸与任何后处理。
9. 将最终图复制到项目目标目录。默认新增版本；用户要求替换时先备份旧图到该场景`archive/`。保留生成工具缓存原件，不只交缓存路径。
10. 保存完整提示词、实际附图顺序与各自用途、工具渠道、实际像素、采用版本及已知缺陷；同步分镜文案、README和当前参考链接，防止下次读回旧规范。

## 当前已知边界

本批质量获认可，不表示每张图的空间连续性都完全通过。不同机位的窗与书柜方位、玉戒大小仍要按镜头检查。宫殿内的金条陈设也不自动证明剧情国库有钱或没钱。图像生成的画面不得反向擅自改写剧情规则。
