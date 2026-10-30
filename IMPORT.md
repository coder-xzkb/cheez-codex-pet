# 把 cheez 导入自己的 Codex 应用

## 1. 下载并解压

下载 [cheez-pet.zip](cheez-pet.zip)，解压后应看到：

```text
cheez/
├── pet.json
└── spritesheet.png
```

两个文件需要放在同一个 `cheez` 文件夹中。

## 2. 放入宠物目录

先退出 Codex 桌面应用，将整个 `cheez` 文件夹复制到：

| 系统 | 默认目标目录 |
| --- | --- |
| Windows | `%USERPROFILE%\.codex\pets\cheez\` |
| macOS | `~/.codex/pets/cheez/` |

没有 `pets` 文件夹时可以自行创建。如果你设置了自定义 `CODEX_HOME`，使用该目录下的 `pets/cheez/`。

Windows 可以按 `Win + R`，输入 `%USERPROFILE%\.codex\pets` 打开目录。最终确认 `pet.json` 位于 `pets/cheez/pet.json`，不要多套一层文件夹。

## 3. 选择 cheez

重新打开应用，进入 **设置 → Pets（宠物）**，点击 **Refresh（刷新）**（如果显示），然后选择 **cheez**。使用 `/pet` 或 **Show pet（显示宠物）** 显示桌面宠物。

如果列表中没有 cheez，先检查文件夹层级，再更新并重启应用。本教程按本机已有的自定义宠物文件结构整理；若当前版本不识别本地导入，可把 `cheez/spritesheet.png` 附给已启用 Pets 插件的聊天，并发送：

> 请将这张已完成的 v2 宠物精灵图导入为自定义宠物 cheez，验证后直接使用现成动画，不重新生成画面。她的待机动作不眨眼。

## 使用自己的宠物

用自己的完整动画精灵图替换 `spritesheet.png`，同时修改 `pet.json` 中的 `id`、`displayName` 和 `description`。每个宠物使用独立的文件夹和 ID。普通单张立绘需要先制作成合规精灵图，不能直接替换。

本包使用 v2 布局：8 列 × 11 行、1536 × 2288 像素，保留透明背景。前九行帧数依次为 `6, 8, 8, 4, 5, 8, 6, 6, 6`，最后两行各有 8 个视线方向，其余格子留空。

应用操作入口参考：[OpenAI Pets 官方说明](https://learn.chatgpt.com/docs/pets)。官方文档没有在该页面列出本地导入文件结构，以上目录与 `pet.json` 格式依据本机已有配置；仅适用于支持这一结构的桌面版本。
