---
description: 更新与图像资产关联的图像字段。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---

# ImageFieldUpdate{#imagefieldupdate}

更新与图像资产关联的图像字段。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 资产句柄。 |
| 解析度 | `xsd:double` | 图像分辨率（以像素/英寸为单位）。 |
| anchorX | `xsd:int` | X轴图像锚点。 |
| anchorY | `xsd:int` | Y轴图像锚点。 |
| 用户数据 | `xsd:string` | 值 `userData` 元数据字段，该字段发布到图像服务用户数据目录字段。 |
