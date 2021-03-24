---
description: PostScript文件属性。
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

---


# GenerationInfo{#generationinfo}

PostScript文件属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`引擎`*` | `xsd:string` | 使用的生成引擎（有关值，请参阅“生成信息”）。 |
| `*`origin`*` | `types:Asset` | 生成中使用的主要资产的资产记录。 |
| `*`已生成`*` | `types:Asset` | 生成的资产的资产记录。 |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | 与生成过程关联的属性数组。 |

