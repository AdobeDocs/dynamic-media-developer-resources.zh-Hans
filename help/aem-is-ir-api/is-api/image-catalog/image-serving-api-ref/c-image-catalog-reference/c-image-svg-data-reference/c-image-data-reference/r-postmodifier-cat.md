---
description: 后缀请求修饰符字符串。 没有或多个图像服务命令以“&”字符分隔。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# PostModifier{#postmodifier}

后缀请求修饰符字符串。 没有或多个图像服务命令以“&amp;”字符分隔。

此字段中的命令始终覆盖HTTP请求中的命令和 `catalog::Modifier`.

`catalog::PostModifier` 如果某些图像需要通常从URL控制的特殊设置，则很有用，例如 `qlt=` 或 `resmode=`. `catalog::Modifier` 应该用于设置图像目录中的大多数IS命令。

中允许使用宏 `catalog::PostModifier`，只要它们是在同一目录或默认目录中定义的。 也可以使用自定义变量。

>[!NOTE]
>
>如果请求涉及多个层，则仅请求 `catalog::PostModifier` 应用层0。 `catalog::PostModifier` 会忽略所有其他图层。

## 属性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文本字符串。 可选.

## 默认 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

无。

## 另请参阅 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog：：Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
