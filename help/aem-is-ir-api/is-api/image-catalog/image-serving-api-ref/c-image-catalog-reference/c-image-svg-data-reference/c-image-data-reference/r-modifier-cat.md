---
description: 前缀请求修饰符字符串。 “&”字符分隔的“图像提供”命令中没有或多个。
solution: Experience Manager
title: 修饰符
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# 修饰符{#modifier}

前缀请求修饰符字符串。 “&amp;”字符分隔的“图像提供”命令中没有或多个。

用于持久修改图像并存储模板正文。

此字段中的命令将被引用此记录的请求或模板中的相同命令和`catalog::PostModifier`中的命令覆盖

允许在`catalog::Modifier`中使用宏，只要它们在同一目录或默认目录中定义。 也可以使用自定义变量。

## 属性 {#section-6674388f77d644469371a17e8809c45f}

文本字符串。 可选。

## 默认 {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

无。

## 另请参阅 {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
