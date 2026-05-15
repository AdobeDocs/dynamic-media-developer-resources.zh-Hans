---
description: 从PDF文件中提取的搜索字符串记录。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
TQID: 'https://experienceleague.adobe.com/bWokSVoIEkxrKgXAkaR4ycgSjZAWb2trFnqokTe98XQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 12%

---

# [!DNL SearchStrings]{#searchstrings}

从PDF文件中提取的搜索字符串记录。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 搜索字符串 | `xsd:string` | 搜索字符串文本。 |
| keywordsArray | `types:KeywordsArray` | 搜索字符串中的关键字数组。 |
| 状态 | `xsd:boolean` | 如果搜索字符串有效且已启用，则为True。 |
| x | `xsd:int` | 搜索字符串的X轴位置。 |
| y | `xsd:int` | 搜索字符串的Y轴位置。 |
| 宽度 | `xsd:int` | 搜索字符串宽度。 |
| 高度 | `xsd:int` | 搜索字符串高度。 |
| 字体名称 | `xsd:string` | 搜索字符串中使用的字体的名称。 |
| pointSize | `xsd:string` | 字体大小。 |
