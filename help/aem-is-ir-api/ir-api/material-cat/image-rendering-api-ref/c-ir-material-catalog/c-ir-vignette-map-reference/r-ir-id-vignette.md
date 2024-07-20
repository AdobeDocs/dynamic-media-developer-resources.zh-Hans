---
description: 晕影标识符。 服务器查找晕影映射文件中记录的索引键值。
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5c0c8788-ffe5-4b42-86f6-6b4683dd7c21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 6%

---

# Id{#id}

晕影标识符。 服务器查找晕影映射文件中记录的索引键值。

通常是简短且唯一的标识符，如SKU编号。 也可能是更复杂的字符串，它可能与文件路径类似。

## 属性 {#section-267bbf34677e4401abbaf6fdce52191b}

文本字符串。 必需。 晕影映射表的主索引键。 每个`vignette::Id`值在表中都必须是唯一的，并且不得包含“，”字符。

## 默认 {#section-736d3419b19045efa00887cb595b0337}

无。

## 另请参阅 {#section-19dce97a43a9461caf74ef3cdd560a3a}

[attribute：：RootId](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootid.md#reference-54b42b7125824be593378c1accb70d5a)
