---
description: PostScript文件属性。
seo-description: PostScript文件属性。
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
topic: Dynamic Media Image Production System API
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---


# GenerationInfo{#generationinfo}

PostScript文件属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`引擎`*` | `xsd:string` | 使用的生成引擎（有关值，请参阅“生成信息”）。 |
| `*`源`*` | `types:Asset` | 生成中使用的主要资产的资产记录。 |
| `*`已生成`*` | `types:Asset` | 生成的资产的资产记录。 |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | 与生成过程关联的属性的数组。 |

