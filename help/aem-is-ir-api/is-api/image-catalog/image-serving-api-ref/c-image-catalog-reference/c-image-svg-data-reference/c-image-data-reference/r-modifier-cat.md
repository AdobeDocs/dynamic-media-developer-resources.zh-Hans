---
description: 前缀请求修饰符字符串。 没有或更多以“&”字符分隔的图像服务命令。
solution: Experience Manager
title: 修饰符
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
TQID: 'https://experienceleague.adobe.com/b1j5WmY-PNOt1zW9qglJob5W8csmI3TidhDwoHK3kCM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 7%

---

# 修饰符{#modifier}

前缀请求修饰符字符串。 没有或更多以“&amp;”字符分隔的图像服务命令。

用于持久修改图像并存储模板正文。

此字段中的命令被引用此记录的请求或模板中的相同命令以及`catalog::PostModifier`中的命令覆盖

`catalog::Modifier`中允许使用宏，只要这些宏是在同一目录或默认目录中定义的。 也可以使用自定义变量。

## 属性 {#section-6674388f77d644469371a17e8809c45f}

文本字符串。 可选.

## 默认 {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

无。

## 另请参阅 {#section-7a67803d141b442180c418c1f3cff029}

[catalog：：PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
