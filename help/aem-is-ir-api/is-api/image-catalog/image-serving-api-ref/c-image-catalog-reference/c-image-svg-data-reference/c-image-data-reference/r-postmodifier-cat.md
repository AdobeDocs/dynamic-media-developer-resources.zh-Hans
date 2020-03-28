---
description: 后缀请求修饰符字符串。 没有或更多以“&”字符分隔的图像服务命令。
seo-description: 后缀请求修饰符字符串。 没有或更多以“&”字符分隔的图像服务命令。
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostModifier{#postmodifier}

后缀请求修饰符字符串。 没有或更多以“&amp;”字符分隔的图像服务命令。

此字段中的命令始终覆盖HTTP请求和中的命令 `catalog::Modifier`。

`catalog::PostModifier` 如果某些图像需要特殊设置（通常可以通过URL进行控制，如或），则此选项 `qlt=` 很有用 `resmode=`。 `catalog::Modifier` 应用于在图像目录中设置大多数IS命令。

只要宏在同一 `catalog::PostModifier`目录中或在默认目录中定义，宏便可在中使用。 自定义变量也可以使用。

>[!NOTE]
>
>如果请求涉及多个层，则仅应用 `catalog::PostModifier` 层0的内容。 `catalog::PostModifier` 忽略所有其他图层。

## 属性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文本字符串。 可选。

## 默认 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

无。

## 另请参阅 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog:::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
