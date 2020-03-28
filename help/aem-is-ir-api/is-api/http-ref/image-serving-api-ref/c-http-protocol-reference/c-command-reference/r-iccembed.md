---
description: 嵌入颜色用户档案。 指定是否应将工作的ICC颜色用户档案或使用icc=指定的用户档案嵌入到回复图像中。
seo-description: 嵌入颜色用户档案。 指定是否应将工作的ICC颜色用户档案或使用icc=指定的用户档案嵌入到回复图像中。
seo-title: iccEmbed
solution: Experience Manager
title: iccEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: ccd3fd2f-6f73-4725-a51a-9daf643d71af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# iccEmbed{#iccembed}

嵌入颜色用户档案。 指定是否应将工作的ICC颜色用户档案或使用icc=指定的用户档案嵌入到回复图像中。

`iccEmbed=0|1`

## 属性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

请求属性。 如果没有可用于嵌入的用户档案，则忽略该选项。

## 默认 {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`，因为输出图像中不嵌入ICC用户档案。 如果输出图像格式不支持嵌入ICC用户档案，则忽略此选项。

See [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) for details.

## 另请参阅 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute:::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) , [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
