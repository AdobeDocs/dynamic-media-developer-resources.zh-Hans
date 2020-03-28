---
description: 图层视图属性。
seo-description: 图层视图属性。
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Scene7 Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LayerViewInfo{#layerviewinfo}

图层视图属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`url`*` | `xsd:string` | 表示模板的图像服务器URL。 组合 `urlModifier` 字段 `urlPostAp- plyModifier` 和字段。 |
| ` *`urlModifier`*` | `xsd:string` | 在请求或命令之前应用的图像服务协议 `urlPostApplyModifier` 命令。 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | 在命令和请求命令后应用的图像 `urlModifier` 服务协议命令。 |

