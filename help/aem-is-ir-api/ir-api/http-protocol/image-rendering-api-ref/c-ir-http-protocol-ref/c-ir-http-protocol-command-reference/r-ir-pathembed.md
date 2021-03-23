---
description: 嵌入路径数据。 指定是否应将嵌入晕影中的Photoshop路径包含在响应图像中。
seo-description: 嵌入路径数据。 指定是否应将嵌入晕影中的Photoshop路径包含在响应图像中。
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
uuid: d40ea1b5-f2d3-4f81-b96f-abb4eb7eb2b3
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# pathEmbed{#pathembed}

嵌入路径数据。 指定是否应将嵌入晕影中的Photoshop路径包含在响应图像中。

`pathEmbed=0|1`

## 属性 {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

请求属性。 如果晕影不包含路径数据，则忽略。 如果需要，路径数据将缩放为`wid=`和/或`hei=`。

如果输出图像格式不支持路径嵌入，则忽略。 有关支持路径嵌入的输出图像格式的列表，请参阅`fmt=`的说明。

## 默认 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, for no embedding of paths in output images.

## 另请参阅 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
