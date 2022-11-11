---
description: 从PDF文件提取的搜索字符串记录。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# [!DNL SearchStrings]{#searchstrings}

从PDF文件提取的搜索字符串记录。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| searchString | `xsd:string` | 搜索字符串文本。 |
| keywordsArray | `types:KeywordsArray` | 搜索字符串中的关键词数组。 |
| 状态 | `xsd:boolean` | 如果搜索字符串有效且已启用，则返回true。 |
| x | `xsd:int` | 搜索字符串的X轴位置。 |
| y | `xsd:int` | 搜索字符串的Y轴位置。 |
| 宽度 | `xsd:int` | 搜索字符串宽度。 |
| 高度 | `xsd:int` | 搜索字符串高度。 |
| fontName | `xsd:string` | 搜索字符串中使用的字体的名称。 |
| pointSize | `xsd:string` | 字体大小. |
