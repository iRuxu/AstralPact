# 工作台道具资产约定

每件道具使用 `assets/props/<道具名>/`。同一道具的不同角度、状态和交付版用同一个资产目录管理。片名字标、地名标识等后期叠加素材放在 `assets/other/`。

```text
assets/props/<道具名>/
├── index.json
├── index.png
├── README.md
├── angles/
├── portraits/
└── archive/
```

## 概览和图片

- 「概览」编辑名称、标签和备注，分别写入 `index.json` 的 `name`、`tags` 和 `note`。显示名称可改，目录路径用于识别道具。
- 自定义标签可用空格、回车或逗号录入，点击标签上的 × 移除。列表支持按名称或标签搜索，多选标签时取交集。工作台也读取目录分组作为标签，在详情中移除分组标签后将其记入 `hiddenGroupTags`。
- 「主图」独立上传根目录的 `index.<图片扩展名>`，沿用图片原格式，根目录只保留一份现行主图。角度图和特写独立登记，默认保留现行主图。
- 「角度」展示 `angles/` 下的图，适合放正面、侧面、背面等角度和机位。索引使用 `category: "angle"`。
- 「特写」展示 `portraits/` 下的图，与角色特写目录命名一致。局部、状态变体和其他交付版也放在这里，索引使用 `category: "portrait"`。
- 角度图、特写和交付参考由 Codex 将生成结果直接写入对应目录，工作台自动读取。两个页签默认预览第一张，点击上方缩略图切换下方大图。生成词由 Codex 登记到 `index.json`，这两个页签仅展示已登记的生成词。
- `index.json` 的 `mainImage` 指向主图条目的 ID。每张图用 `images` 条目登记 `id`、`file`、`label`、`category`、`status`。文件路径相对于道具根目录，替换时沿用图片 ID。状态沿用场景的 `adopted`、`candidate` 和 `reference`。已核实的生成词写入 `prompt`。使用生成记录时，省略 `prompt`，用 `promptRecord` 指向资产目录内的原始 JSON，按需用 `promptEntry` 定位条目。

```json
{
  "name": "星契卡",
  "tags": ["实体道具"],
  "note": "",
  "mainImage": "front",
  "images": [
    {
      "id": "front",
      "file": "index.png",
      "label": "镭射正面概念",
      "category": "angle",
      "status": "reference"
    },
    {
      "id": "side",
      "file": "angles/侧面.png",
      "label": "卡面侧视",
      "category": "angle",
      "status": "reference"
    },
    {
      "id": "detail",
      "file": "portraits/刻线特写.png",
      "label": "细金轨道刻线",
      "category": "portrait",
      "status": "reference"
    }
  ],
  "history": []
}
```

## 道具说明和历史版本

- 「道具说明」预览和编辑根目录的 `README.md`。记录剧情用途、美术设定和连续性，例如材质、与角色的相对尺寸、握持方式、开合与亮灭，以及跨机位固定的细节。
- 替换图片、修订已有生成词或修改已有说明时，按 `archive/YYYY-MM-DD-vNNN/` 规则归档上一版。归档的 `index.json` 用 `images` 登记旧图和对应生成词，旧说明保存在该版本的 `README.md`。当前索引的 `history` 追加 `version`、`note` 和 ISO 8601 格式的 `archivedAt`。
- 「历史版本」按条目展开，可查看归档图、生成词和说明。整理现行文件时同步更新工作台索引、Markdown 和分镜引用。独立历史生成记录保留其原位置和当时的文件名。
