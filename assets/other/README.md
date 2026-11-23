# 其他资产

- [片名字标](片名/README.md)
- [花夏星与星沙城入场标识](地名/README.md)

这里收纳用于后期叠加的字标、图形和特效素材。每项资产使用 `assets/other/<资产名>/`，可按工作台资产约定分组。

```text
assets/other/<资产名>/
├── index.json
├── README.md
├── index.png
├── extend/
└── archive/
```

## 工作台详情

- 「概览」编辑名称、标签和备注，分别保存到 `index.json` 的 `name`、`tags`、`note`。更改显示名称时沿用原目录和现有引用。
- 「主图」保存为资产根目录的 `index.<图片扩展名>`，沿用图片原格式，根目录只保留一份现行主图。索引的 `mainImage` 指向主图条目的 ID。
- Codex 将扩展图片直接放入 `extend/`，工作台自动读取。为图片写入 `images` 条目以登记名称、分类、采用状态和生成词。扩展页按缩略图切换大图，并展示已登记的生成词。
- 图片条目用 `id`、`file`、`label`、`category`、`status` 登记，文件路径相对于资产根目录。分类可用 `graphic`、`effect`、`delivery`，状态可用 `adopted`、`candidate`、`reference`。已核实的实际生成词写入 `prompt`。使用生成记录时，省略 `prompt`，用 `promptRecord` 指向资产目录内的原始 JSON，按需用 `promptEntry` 定位条目。
- 「说明」编辑当前资产目录的 `README.md`。替换图片、修订生成词或修改已有说明前，将旧版保存到 `archive/YYYY-MM-DD-vNNN/`，归档索引用 `images` 登记旧图和对应生成词，旧说明保存为版本目录的 `README.md`。当前索引的 `history` 追加 `version`、`note` 和 ISO 8601 格式的 `archivedAt`，供「历史版本」显示时间及对应内容。
