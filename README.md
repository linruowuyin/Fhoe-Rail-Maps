# Fhoe-Rail 社区地图仓库

本仓库是 [Fhoe-Rail](https://github.com/linruowuyin/Fhoe-Rail) 的**社区地图共享后端**。用户通过[地图作业站](https://linruowuyin.github.io/fhoe-maps-site/)上传地图，CI 自动校验后合并，**零审核**。

## 目录结构

| 目录 | 内容 |
| --- | --- |
| `map/<version>/` | 地图 JSON（`map_N-N_N.json`） |
| `picture/` | 地图引用的 UI 模板图 |
| `preview/<version>/` | 地图预览缩略图 |
| `star_list.json` | md5 校验清单（客户端增量下载用） |
| `version.json` | 时间戳（UTC+8） |

## 上传方式（用户）

打开[地图作业站](https://linruowuyin.github.io/fhoe-maps-site/) → 编辑地图 → 「🚀 发布到 GitHub」→ 填本仓库名 `linruowuyin/Fhoe-Rail-Maps` + fine-grained PAT → 发布。CI 自动跑 `validate_maps` / `validate_pictures` / `format_maps`，通过即合并。
