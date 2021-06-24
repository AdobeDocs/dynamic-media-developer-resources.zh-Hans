---
description: 嵌入XMP元数据。 指定是否应将XMP元数据包含在响应图像中。
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# xmpEmbed{#xmpembed}

嵌入XMP元数据。 指定是否应将XMP元数据包含在响应图像中。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP数据无需修改即可从源图像传递到响应图像。 这可能会导致响应图像中嵌入错误的数据。

## 属性 {#section-27024c4272f44d9a8c264a0629193af2}

请求属性。 如果源图像不包含XMP数据，则忽略。 仅处理`layer=0`源图像中的XMP数据。 将忽略其他图层图像的XMP数据。

如果输出图像格式不支持XMP嵌入，则忽略。 有关支持XMP嵌入的输出图像格式的列表，请参阅`fmt=`的说明。

## 默认 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`，以禁止在输出图像中嵌入路径。

## 另请参阅 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
