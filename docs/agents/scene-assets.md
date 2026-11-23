# 工作台场景资产约定

每个场景一个目录。角色会经过同一地点的不同机位、天气或时间时，尽量共用同一个场景。只有需要单独管理空间连续性时才拆分场景，例如宫殿整体与议会厅。已有共享外景沿用原入口，房间说明可以直接链接到共享图。

```text
assets/scenes/<场景名>/
├── index.json
├── index.png
├── README.md
├── views/
├── time/
├── weather/
├── seasons/
├── layout/
├── details/
└── archive/
    └── 2026-11-23-v001/
        ├── index.json
        └── 旧机位.png
```

## 概览、主图和分类

- 「概览」编辑场景名称、标签和个人备注，分别写入 `index.json` 的 `name`、`tags` 和 `note`。编辑名称后沿用原目录和现有引用。列表按名称或标签搜索，多选标签取交集。
- 根目录的 `index.<扩展名>` 是主图，沿用图片原格式，根目录只保留一份现行主图。索引的 `mainImage` 指向主图条目的 ID，`images` 中用 `id`、`file`、`label`、`category`、`status` 和 `prompt` 登记图片。优先选择能说明空间的代表性画面。候选主图仍显示候选标记。空场景显示待补主图占位。
- 其他图片按用途放入下表目录，可按需建立。图片路径相对于场景根目录。环境条件可以跨分类组合，例如临窗机位同时标记冬季、黄昏和雪。工作台兼容读取旧索引登记的目录。
- 主图是独立的场景概念稿，在「主图」页签上传或替换。
- 分类页签展示图片、标题和已有生成词。Codex 将图片直接写入对应目录，将实际生成词登记到 `index.json` 中对应图片的条目。
- 采用状态用 `adopted`（已采用）、`candidate`（候选）、`reference`（参考）。以用户确认和场景说明为准。
- 「场景说明」可预览和编辑根目录的 `README.md`，记录用途、所在位置、空间关系与连续性。可按需要补充入口通路、窗景朝向、固定布置、受光变化、可复用素材和待验收项。

| 页签 | 目录 | `category` |
| --- | --- | --- |
| 机位 | `views/` | `view` |
| 时间 | `time/` | `time` |
| 天气 | `weather/` | `weather` |
| 季节 | `seasons/` | `season` |
| 空间定位 | `layout/` | `layout` |
| 局部与陈设 | `details/` | `detail` |

```json
{
  "name": "滨海街角",
  "tags": ["星沙城", "室外"],
  "note": "",
  "mainImage": "overview",
  "images": [
    {
      "id": "overview",
      "file": "index.png",
      "label": "临海街角全景",
      "category": "view",
      "status": "candidate",
      "conditions": { "season": "冬季", "time": "黄昏", "weather": "雪" },
      "prompt": "实际使用的完整生成词"
    }
  ],
  "history": []
}
```

`conditions` 和生成词按实际情况填写。使用生成记录时，省略图片条目的 `prompt`，用 `promptRecord` 指向资产目录内的原始 JSON。批量记录可再加 `promptEntry` 定位条目，例如 `["outputs", 0]`。工作台在对应图片下展示生成词。找不到确切来源时保留空缺。

## 修订与既有项目接入

- 替换图片前将旧图和旧生成词归入同一个 `archive/YYYY-MM-DD-vNNN/`。归档内的 `index.json` 以 `images` 数组登记旧素材和当时的生成词。当前索引保留图片 ID 并更新路径、状态和生成词，`history` 追加 `version`、`note` 和 ISO 8601 格式的 `archivedAt`。修订已有场景说明时归档上一版 `README.md`。
- 历史版本按条目展开，可查看归档图片、生成词和旧版说明。时间按北京时间显示。旧归档优先使用目录名中的日期，没有日期时使用目录创建时间。直接放在 `archive/` 下的图片归入「早期归档」，显示 `archive/` 的创建时间。直接落盘或整理旧目录时，同步更新现行索引和 Markdown、分镜等引用。
- 旧归档目录的图片可以浏览。独立历史生成记录继续保存在原位置，已确认对应关系的现行图片通过索引链接原记录。

## 场景文档集中维护

每个场景的当前说明统一写在`assets/scenes/<场景>/README.md`，包含用途、城市/建筑位置、室内外机位、连续性、采用状态和记录入口。子目录不另建README，不在docs并行维护重复场景说明；通用场景制作约定与总索引放在`assets/scenes/README.md`。多个房间共用的宫殿外景与位置图归`王室宫殿/`，房间目录引用；实际生成记录仍随资产保存在各自`archive/生成记录/`。
