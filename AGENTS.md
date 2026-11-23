# 项目工作约定

开始任何项目任务前先读根目录 `AGENTS.md`，再按任务读取下列对应文档和当前资产。用户在本次对话给出的新要求优先。工作台的「设定」读取同一批项目文档。

## 项目技能

通用制作技能随咔嚓 npm 包提供。接到制作任务时，在 `node_modules/@2kog/kacha/skills/` 下按各 `SKILL.md` 的 `description` 选择匹配的技能，再按下表查阅本剧的对应约定。如使用全局安装，在 `npm root -g` 返回的目录下查找 `@2kog/kacha/skills/`。

## 按任务查阅设定

| 工作内容 | 先读 |
| --- | --- |
| 剧情、人物关系、台词与叙事连续性 | [世界观与角色](docs/世界观与角色.md)，再读对应剧集的 `scripts/<剧集>/剧本.md` 或用户指定稿 |
| 角色、场景和道具的现行外观 | [角色美术设定](docs/角色美术设定.md)、[场景总览](assets/scenes/README.md)、[道具美术设定](docs/道具美术设定.md)，再读本次使用的资产说明和当前参考 |
| 生成或修订图片 | [3D电影CG风格与生成工作流](docs/3D电影CG风格与生成工作流.md)和[分镜与生成工作流](docs/agents/production-workflow.md)。涉及角色原画、CG三视图转换时加读[角色双版本与3D高清生成规范](docs/角色双版本与3D高清生成规范.md) |
| 设计分镜、制作视频提示词或核对交付格式 | [分镜与生成工作流](docs/agents/production-workflow.md)，以及 `storyboard/<剧集>/<场次>/` 的当前分镜与参考 |
| 新建、补齐、迁移或替换资产 | 先读下方「工作台资产落盘」，再读对应资产约定和现有索引 |
| 调整工作台或项目结构 | [工作台项目目录约定](docs/agents/workbench-project-layout.md)，以及下文对应资产的约定 |
| 调整工作台页面、交互或样式 | [咔嚓源码的工作台设计规范](https://github.com/iRuxu/kacha/blob/main/AGENTS.md) |

叙事事实以现行剧本和世界观为据。生成约束、当前参考优先级与交付格式由美术及制作规范维护。涉及同一场次时，以同一集和场次对应剧本与分镜核对对白、动作和空间。

## 沟通与项目习惯

- 默认中文回复。研究临时文件放在项目 `tmp/` 下。
- 如涉及Web应用，默认Vue3 Options API；一般软件默认JS/Node.js。简单修改不频繁调起浏览器。
- 业务与制作规范放在 `docs/`，工作约定可补在 `docs/agents/`；不要改写或恢复用户移动、删除的资产。

## 工作台项目配置

- 工作台左上角的项目名称取自项目根目录 `package.json` 的 `name`。缺少有效名称时显示「制作项目」。
- 名称下方的描述取自同一文件的 `description`。缺少有效描述时显示「制作工作台」。
- 项目图标可放在根目录的 `config/logo.{ext}`。使用小写文件名，支持 SVG、PNG、WebP、AVIF、JPG、JPEG、GIF、ICO 和 BMP。建议只放一份。《星契》的 `config/logo.svg` 的默认图标为兔子头。找不到图标或图片加载失败时，也显示兔子头。

## 工作台资产落盘

AI 生成、修订或整理素材时，直接将文件写入对应的资产目录，并同步维护索引。先确认资产实际目录、当前采用版本和现有引用，沿用现存分组与资产路径。

| 资产库 | 根目录的默认文件 | 其他现行素材 | 详细约定 |
| --- | --- | --- | --- |
| `assets/characters/` 角色 | `2d-turnaround.<扩展名>`、`3d-turnaround.<扩展名>` | 特写放 `portraits/`，皮肤直接平铺在 `skin/`，音色与台词放 `voice/`，默认音色命名为 `voice/index.<扩展名>` | [角色资产约定](docs/agents/character-assets.md) |
| `assets/props/` 道具 | `index.<扩展名>` | 角度图放 `angles/`，特写、状态图及其他参考放 `portraits/` | [道具资产约定](docs/agents/prop-assets.md) |
| `assets/scenes/` 场景 | `index.<扩展名>` | 机位、时间、天气、季节、空间定位、局部图分别放 `views/`、`time/`、`weather/`、`seasons/`、`layout/`、`details/` | [场景资产约定](docs/agents/scene-assets.md) |
| `assets/other/` 其他 | `index.<扩展名>` | 扩展图放 `extend/` | [其他资产约定](assets/other/README.md) |

- **维护索引和说明。** 在具体资产根目录维护 `index.json` 和 `README.md`。名称、标签和用户备注分别写入 `name`、`tags` 和 `note`。制作、美术或剧情说明写入 `README.md`。素材路径以该资产目录为基准，文件保留真实格式。目录名使用上表的标准拼写。
- **登记主图和实际生成词。** 道具、场景和其他资产使用 `images` 登记图片，`mainImage` 指向主图条目的 ID。新增图片时登记 `id`、`file`、`label`、`category` 和已知采用状态，替换时沿用同一条目的 ID。生成词用条目的 `prompt` 保存，或用 `promptRecord` 和可选的 `promptEntry` 引用实际生成记录。角色用 `mainImage` 选择 `image2d` 或 `image3d` 作为封面，默认图、音色和模型的生成词使用 `prompts`，特写和皮肤使用 `assetPrompts`，以角色目录内的相对文件路径为键。只登记能与该文件版本核实对应的实际生成词。
- **保留确认状态。** 主图用于默认展示。修改采用状态以用户确认和资产说明为据。生成候选时按对应资产约定另存并登记为候选，用户确认替换现行版本后再更新默认图或对应的现行条目。
- **遵循现有素材边界。** 角色的 2D、3D 默认图都是三视图，单张立绘、候选图或历史稿须按实际用途登记。缺失的默认图或音色保留缺项，旧目录兼容仅用于读取历史结构。新增和迁移素材按表中目录落盘。
- **归档后再替换。** 替换现行素材、修订已有生成词或改写既有资产说明时，按各库格式保存上一版素材、生成词或 `README.md` 到 `archive/YYYY-MM-DD-vNNN/`，在当前索引的 `history` 登记版本和 `archivedAt`。首次补缺可直接写入现行目录。移动或改名时同步修正现行索引、Markdown 和分镜引用，历史生成记录保留执行时的原文。

## 工作台资产嵌套

`assets/characters/`、`assets/scenes/`、`assets/props/` 和 `assets/other/` 都支持多层分组，例如 `assets/props/宫廷/服饰/龙纹玉佩/`。Codex 新建分组时，在每一层分组目录放一个内容为 `{}` 的 `group.json`。在具体资产目录根部维护 `index.json` 和 `README.md`。工作台使用相对于所属资产库根目录的完整路径识别资产，不同组可以有同名资产。分组名自动成为对应资产的标签。需要隐藏某项资产的继承标签时，在该资产索引记录 `hiddenGroupTags`，保留实际目录。

已有编号分组继续识别。没有标记的旧目录可通过内部明确登记的资产识别为分组。识别到具体资产后，其机位、状态图、特写、皮肤和归档作为该资产的内容处理。要在某个目录下再定义独立资产，先把该目录按分组管理。

## 工作台音频资产

可复用音乐、音效和台词素材放在 [assets/audio/](assets/audio/README.md)，沿用多层分组规则。音频用 `index.json` 的 `tracks` 登记文件、类型、用途和来源，自定义标签另存于根级 `tags`。角色音色继续随角色存储，正式配音随场次存储。
