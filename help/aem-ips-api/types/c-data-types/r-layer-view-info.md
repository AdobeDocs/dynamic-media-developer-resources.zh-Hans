---
description: 图层视图属性。
seo-description: 图层视图属性。
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
topic: Dynamic Media Image Production System API
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 11%

---


# LayerViewInfo{#layerviewinfo}

图层视图属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`url`*` | `xsd:string` | 表示模板的图像服务器URL。 组合`urlModifier`和`urlPostAp- plyModifier`字段。 |
| `*`urlModifier`*` | `xsd:string` | 在请求或`urlPostApplyModifier`命令之前应用的图像服务协议命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 要在`urlModifier`和请求命令之后应用的图像服务协议命令。 |

