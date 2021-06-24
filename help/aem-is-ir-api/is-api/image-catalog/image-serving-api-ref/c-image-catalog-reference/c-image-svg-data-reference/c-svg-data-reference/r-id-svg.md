---
description: Id
solution: Experience Manager
title: Id
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 5%

---

# Id{#id}

通常是一个简短的唯一标识符，例如SKU编号，可能带有某种后缀，例如SKU具有多个图像或具有特定于区域设置的变体。 可能还是一个更复杂的字符串，看起来更像文件路径，可支持使用图像服务轻松改造网站。

>[!NOTE]
>
>加载图像目录后，图像和SVG表将合并到单个表中。 两个表中的ID值必须唯一。 如果图像表包含具有相同ID值的记录，则会丢弃SVG记录。 静态内容通过单独的表进行管理；因此，静态内容项和图像/SVG项可能具有相同的ID值。

## 属性 {#section-874a6853f67b4b229341ca76682884ae}

文本字符串。 必需. 记录图像/SVG或静态内容数据表的标识符。 此图像目录/SVG目录或此静态内容目录中的每个`catalog::Id`值必须唯一，且不得包含“，”字符。

## 默认 {#section-a26e7d83a5ee44b5918baef82ee48e14}

无。

## 另请参阅 {#section-a258d818487d4ee6b7a99a65d18471a9}

[属性：:RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
