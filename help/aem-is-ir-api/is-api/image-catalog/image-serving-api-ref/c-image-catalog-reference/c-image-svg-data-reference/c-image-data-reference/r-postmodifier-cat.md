---
description: 后缀请求修饰符字符串。 无或多个以“&”字符分隔的图像服务命令。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 4%

---


# PostModifier{#postmodifier}

后缀请求修饰符字符串。 无或多个以“&amp;”字符分隔的图像服务命令。

此字段中的命令始终覆盖HTTP请求和`catalog::Modifier`中的命令。

`catalog::PostModifier` 当某些图像需要通常由URL控制的特殊设置（如或）时，此 `qlt=` 功能很 `resmode=`有用`catalog::Modifier` 应用于设置图像目录中的大多数IS命令。

宏在`catalog::PostModifier`中是允许的，只要它们在同一目录或默认目录中定义。 也可以使用自定义变量。

>[!NOTE]
>
>如果请求涉及多个层，则仅应用层0的`catalog::PostModifier`的内容。 `catalog::PostModifier` 会忽略所有其他图层。

## 属性 {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

文本字符串。 可选。

## 默认 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

无。

## 另请参阅 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
