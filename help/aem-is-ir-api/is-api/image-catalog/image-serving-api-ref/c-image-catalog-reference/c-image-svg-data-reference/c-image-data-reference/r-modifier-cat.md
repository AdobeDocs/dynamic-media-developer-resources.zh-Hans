---
description: 前缀请求修饰符字符串。 无或多个以“&”字符分隔的图像服务命令。
solution: Experience Manager
title: 修饰符
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---


# 修饰符{#modifier}

前缀请求修饰符字符串。 无或多个以“&amp;”字符分隔的图像服务命令。

用于永久修改图像和存储模板正文。

此字段中的命令由引用此记录的请求或模板中的相同命令和`catalog::PostModifier`中的命令覆盖

宏在`catalog::Modifier`中是允许的，只要它们在同一目录或默认目录中定义。 也可以使用自定义变量。

## 属性 {#section-6674388f77d644469371a17e8809c45f}

文本字符串。 可选。

## 默认 {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

无。

## 另请参阅 {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
