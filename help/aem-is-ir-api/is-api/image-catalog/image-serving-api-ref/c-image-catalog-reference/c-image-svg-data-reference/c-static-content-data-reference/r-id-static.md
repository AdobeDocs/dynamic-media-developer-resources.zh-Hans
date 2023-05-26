---
description: Id
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 4%

---

# Id{#id}

通常是简短且唯一的标识符，例如SKU编号，可能带有某种类型的后缀，例如SKU具有多个图像或具有特定于区域设置的变体。 也可以是更复杂的字符串，它看起来更像是文件路径，以支持使用图像服务轻松地对网站进行改造。

>[!NOTE]
>
>加载图像目录时，图像和SVG表将合并到单个表中。 两个表中的ID值必须唯一。 如果图像表包含具有相同ID值的记录，则会丢弃SVG记录。 静态内容由单独的表管理；因此，静态内容项目和图像/SVG项目可能具有相同的ID值。

## 属性 {#section-874a6853f67b4b229341ca76682884ae}

文本字符串。 必需. 图像/内容或静态SVG数据表的记录标识符。 每个 `catalog::Id` 此图像目录/SVG目录或此静态内容目录中的值必须是唯一的，并且不得包含“，”字符。

## 默认 {#section-a26e7d83a5ee44b5918baef82ee48e14}

无。

## 另请参阅 {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute：：RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
