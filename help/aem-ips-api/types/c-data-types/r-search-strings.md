---
description: 从PDF文件中提取的搜索字符串记录。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 13%

---


# SearchStrings{#searchstrings}

从PDF文件中提取的搜索字符串记录。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`searchString`*` | `xsd:string` | 搜索字符串文本。 |
| `*`keywordsArray`*` | `types:KeywordsArray` | 搜索字符串中的关键字数组。 |
| `*`状态`*` | `xsd:boolean` | 如果搜索字符串有效且已启用，则返回true。 |
| `*`x`*` | `xsd:int` | 搜索字符串的X轴位置。 |
| `*`y`*` | `xsd:int` | 搜索字符串的Y轴位置。 |
| `*`width`*` | `xsd:int` | 搜索字符串宽度。 |
| `*`height`*` | `xsd:int` | 搜索字符串高度。 |
| `*`fontName`*` | `xsd:string` | 搜索字符串中使用的字体的名称。 |
| `*`pointSize`*` | `xsd:string` | 字体大小. |

