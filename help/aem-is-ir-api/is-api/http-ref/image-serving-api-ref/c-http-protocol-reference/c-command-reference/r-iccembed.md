---
title: iccEmbed
description: 嵌入颜色配置文件。 指定是否应在回复图像中嵌入正在使用的ICC颜色配置文件或使用icc=指定的配置文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc5637f6-5452-4bfb-bf30-def6f153f4ad
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# iccEmbed{#iccembed}

嵌入颜色配置文件。 指定是否应在回复图像中嵌入正在使用的ICC颜色配置文件或使用icc=指定的配置文件。

`iccEmbed=0|1`

## 属性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

请求属性。 如果没有可供嵌入的配置文件，则忽略。

## 默认 {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`，用于在输出图像中不嵌入ICC配置文件。 如果输出图像格式不支持嵌入ICC配置文件，则忽略。

有关详细信息，请参阅[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)。

## 另请参阅 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute：：IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ， [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)， [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
