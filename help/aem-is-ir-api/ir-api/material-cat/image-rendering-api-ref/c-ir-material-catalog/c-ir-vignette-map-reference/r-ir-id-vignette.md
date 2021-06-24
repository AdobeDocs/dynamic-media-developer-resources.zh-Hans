---
description: 晕影标识符。 索引键值，服务器通过该值查找晕影映射文件中的记录。
solution: Experience Manager
title: Id
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 5c0c8788-ffe5-4b42-86f6-6b4683dd7c21
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 7%

---

# Id{#id}

晕影标识符。 索引键值，服务器通过该值查找晕影映射文件中的记录。

通常是短的唯一标识符，如SKU编号。 也可以是一个更复杂的字符串，看起来可能像文件路径。

## 属性 {#section-267bbf34677e4401abbaf6fdce52191b}

文本字符串。 必需. 晕影图表的主索引键。 每个`vignette::Id`值在表中必须唯一，且不得包含“，”字符。

## 默认 {#section-736d3419b19045efa00887cb595b0337}

无。

## 另请参阅 {#section-19dce97a43a9461caf74ef3cdd560a3a}

[属性：:RootId](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootid.md#reference-54b42b7125824be593378c1accb70d5a)
