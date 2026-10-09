# 墨伴声音广场（moban-voice-ground）

墨伴 App「声音广场」功能的官方音色库。所有参考音色通过本仓库统一管理，App 启动时拉取 `index.json` 展示音色列表。

## 目录结构

```
moban-voice-ground/
├── index.json        # 音色列表（App 拉取入口）
├── avatars/          # 音色头像（建议 1:1，webp/jpg/png）
├── voices/           # 参考音频（wav，16kHz/单声道/16bit，10-30 秒清晰人声）
├── README.md         # 本文件
└── CONTRIBUTING.md   # 音色提交流程
```

## index.json 字段说明

```json
{
  "name": "音色名称",
  "avatar": "/avatars/xxx.webp",
  "path": "/voices/xxx.wav",
  "vip": false,
  "gender": "male",
  "ageStage": "young",
  "tags": ["中文", "电影解说"]
}
```

| 字段 | 类型 | 说明 |
|------|------|------|
| `name` | string | 音色显示名称 |
| `avatar` | string | 头像路径，相对仓库根目录，以 `/` 开头 |
| `path` | string | 参考音频路径，相对仓库根目录，以 `/` 开头 |
| `vip` | boolean | 是否需要会员 |
| `gender` | string | 性别：`male` / `female` |
| `ageStage` | string | 年龄段：`child` / `young` / `mature` / `elder` |
| `tags` | string[] | 标签列表 |

## 提交音色

请阅读 [CONTRIBUTING.md](./CONTRIBUTING.md) 了解如何提交你的声音样本。
