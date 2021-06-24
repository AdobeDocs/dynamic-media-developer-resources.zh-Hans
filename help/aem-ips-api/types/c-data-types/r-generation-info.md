---
description: PostScript文件属性。
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 12%

---

# GenerationInfo{#generationinfo}

PostScript文件属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`引擎`*` | `xsd:string` | 使用的生成引擎（有关值，请参阅“生成信息”）。 |
| `*`创作者`*` | `types:Asset` | 生成中使用的主资产的资产记录。 |
| `*`已生成`*` | `types:Asset` | 生成的资产的资产记录。 |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | 与生成过程关联的属性数组。 |
