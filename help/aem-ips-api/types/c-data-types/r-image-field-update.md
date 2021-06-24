---
description: 更新与图像资产关联的图像字段。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 9%

---

# ImageFieldUpdate{#imagefieldupdate}

更新与图像资产关联的图像字段。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 资产句柄。 |
| `*`resolution`*` | `xsd:double` | 图像分辨率（以像素/英寸为单位）。 |
| `*`anchorX`*` | `xsd:int` | X轴图像锚点。 |
| `*`anchorY`*` | `xsd:int` | Y轴图像锚点。 |
| `*`用户数据`*` | `xsd:string` | `userData`元数据字段的值，该字段发布到图像服务用户数据目录字段。 |
