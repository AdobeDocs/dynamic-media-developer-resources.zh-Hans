---
description: 嵌入XMP元数据。 指定是否应将XMP元数据包含在响应图像中。
seo-description: 嵌入XMP元数据。 指定是否应将XMP元数据包含在响应图像中。
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# xmpEmbed{#xmpembed}

嵌入XMP元数据。 指定是否应将XMP元数据包含在响应图像中。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP数据将从源图像传递到响应图像，无需修改。 这可能导致在响应图像中嵌入不正确的数据。

## 属性 {#section-27024c4272f44d9a8c264a0629193af2}

请求属性。 如果源图像不包含XMP数据，则忽略。 只处理`layer=0`源映像中的XMP数据。 忽略来自其他图层图像的XMP数据。

如果输出图像格式不支持XMP嵌入，则忽略。 有关支持XMP嵌入的输出图像格式的列表，请参阅`fmt=`的说明。

## 默认 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, for no embedding of paths in output images.

## 另请参阅 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
