---
description: 嵌入XMP元数据。 指定是否应在响应图像中包含XMP元数据。
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

嵌入XMP元数据。 指定是否应在响应图像中包含XMP元数据。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP数据无需修改即可从源图像传递到响应图像。 这可能会导致在响应图像中嵌入不正确的数据。

## 属性 {#section-27024c4272f44d9a8c264a0629193af2}

请求属性。 如果源图像不包含XMP数据，则忽略。 仅来自的源图像的XMP数据 `layer=0` 都会被处理。 来自其他层图像的XMP数据将被忽略。

如果输出图像格式不支持XMP嵌入，则忽略。 请参阅 `fmt=` 以获取支持XMP嵌入的输出图像格式列表。

## 默认 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`，以便在输出图像中不会嵌入路径。

## 另请参阅 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
