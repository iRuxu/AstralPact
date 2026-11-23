# 音频资产

可跨镜头复用的背景音乐、音效和台词素材放在这里，环境底声归音效。角色音色沿用各角色 `voice/`，正式场次配音随对应场次存放。

每个资产一个目录，音频文件放在 `tracks/`，归档在 `archive/`。分组可嵌套，每层分组放 `group.json`。资产根目录的 `index.json` 示例：

```json
{
  "name": "交易所人群底声",
  "type": "effect",
  "note": "交易所广场议论声",
  "tags": ["交易所", "人群"],
  "mainTrack": "crowd",
  "tracks": [
    {
      "id": "crowd",
      "file": "tracks/交易所人群底声.wav",
      "label": "交易所人群底声",
      "category": "effect",
      "status": "reference",
      "source": "",
      "loop": true
    }
  ],
  "history": []
}
```

`tracks[].category` 是音轨的类型，可用 `music`（音乐）、`effect`（音效）或 `dialogue`（台词）。资产的自定义标签存入根级 `tags`。新建时只填写名称。打开资产详情后，可在根级保存 `type` 与 `note`（用途备注），上传的音轨继承资产类型。筛选优先使用资产的 `type`，旧资产仍可按音轨类型筛选。旧音轨的 `usage` 继续在详情显示。`source` 记录来源和授权，未知时留空。工作台从音频文件读取时长。详情只需选择一个文件，选中后立即上传。再次上传会替换当前主音频，归档旧文件及原条目信息，并更新 `history`。
