---
description: PostScript文件属性。
solution: Experience Manager
title: 生成信息
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScript文件属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 使用的生成引擎（请参阅有关值的“生成信息”）。 |
| [!DNL originator] | `types:Asset` | 生成中使用的主要资源的资源记录。 |
| [!DNL generated] | `types:Asset` | 生成的资源的资源记录。 |
| attributeArray | `types:GenerationAttributeArray` | 与生成进程关联的属性数组。 |
