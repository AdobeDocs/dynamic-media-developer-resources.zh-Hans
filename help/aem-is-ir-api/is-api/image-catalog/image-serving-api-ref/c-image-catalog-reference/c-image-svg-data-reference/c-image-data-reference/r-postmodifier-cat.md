---
description: 后缀请求修饰符字符串。 “&”字符分隔的“图像提供”命令中没有或多个。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---

# PostModifier{#postmodifier}

后缀请求修饰符字符串。 “&amp;”字符分隔的“图像提供”命令中没有或多个。

此字段中的命令始终会覆盖HTTP请求和`catalog::Modifier`中的命令。

`catalog::PostModifier` 当某些图像需要特殊设置（通常由URL控制，例如或）时，此变量将 `qlt=` 很有用 `resmode=`。`catalog::Modifier` 应用于在图像目录中设置大多数IS命令。

允许在`catalog::PostModifier`中使用宏，只要它们在同一目录或默认目录中定义。 也可以使用自定义变量。

>[!NOTE]
>
>如果请求涉及多个层，则仅应用层0的`catalog::PostModifier`内容。 `catalog::PostModifier` 会忽略所有其他层。

## 属性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文本字符串。 可选。

## 默认 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

无。

## 另请参阅 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[目录：：修饰符](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
