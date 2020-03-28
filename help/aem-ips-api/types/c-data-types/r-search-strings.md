---
description: 从PDF文件中提取的搜索字符串记录。
seo-description: 从PDF文件中提取的搜索字符串记录。
seo-title: SearchStrings
solution: Experience Manager
title: SearchStrings
topic: Scene7 Image Production System API
uuid: aade2741-3e77-44c6-ab3c-0810ff034412
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SearchStrings{#searchstrings}

从PDF文件中提取的搜索字符串记录。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`searchString`*` | `xsd:string` | 搜索字符串文本。 |
| ` *`keywordsArray`*` | `types:KeywordsArray` | 搜索字符串中的关键字数组。 |
| ` *`状态`*` | `xsd:boolean` | 如果搜索字符串有效且已启用，则返回true。 |
| ` *`x`*` | `xsd:int` | 搜索字符串的X轴位置。 |
| ` *`y`*` | `xsd:int` | 搜索字符串的Y轴位置。 |
| ` *`width`*` | `xsd:int` | 搜索字符串宽度。 |
| ` *`height`*` | `xsd:int` | 搜索字符串高度。 |
| ` *`fontName`*` | `xsd:string` | 搜索字符串中使用的字体的名称。 |
| ` *`pointSize`*` | `xsd:string` | 字体大小. |

