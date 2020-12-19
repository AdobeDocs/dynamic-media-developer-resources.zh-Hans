---
description: 'null'
seo-description: 'null'
seo-title: Id
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: a700472c-e1eb-4eb0-95ff-7afd4ce27931
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 6%

---


# Id{#id}

通常是短的唯一标识符，如SKU编号，可能带有某种后缀，如SKU具有多个图像或具有特定于区域设置的变体。 也可能是一个更复杂的字符串，它看起来更像文件路径，支持使用图像服务轻松改造网站。

>[!NOTE]
>
>在加载图像目录时，图像和SVG表将合并到单个表中。 两个表的ID值必须唯一。 如果图像表包含具有相同ID值的记录，则放弃SVG记录。 静态内容由单独的表管理；静态内容项和图像/SVG项可能因此具有相同的ID值。

## 属性 {#section-874a6853f67b4b229341ca76682884ae}

文本字符串。 必需. 记录图像/SVG或静态内容数据表的标识符。 此图像目录/SVG目录或此静态内容目录中的每个`catalog::Id`值必须唯一，且不得包含“,”字符。

## 默认 {#section-a26e7d83a5ee44b5918baef82ee48e14}

无。

## 另请参阅 {#section-a258d818487d4ee6b7a99a65d18471a9}

[属性：:RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
