---
description: 图层视图属性。
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '54'
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

