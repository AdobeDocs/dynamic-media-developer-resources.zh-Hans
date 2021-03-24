---
description: 更新与图像资产关联的图像字段。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 8%

---


# ImageFieldUpdate{#imagefieldupdate}

更新与图像资产关联的图像字段。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 资产句柄。 |
| `*`分辨率`*` | `xsd:double` | 图像分辨率，以像素/英寸为单位。 |
| `*`anchorX`*` | `xsd:int` | X轴图像锚点。 |
| `*`anchorY`*` | `xsd:int` | Y轴图像锚点。 |
| `*`用户数据`*` | `xsd:string` | `userData`元数据字段的值，将发布到图像服务用户数据目录字段。 |

