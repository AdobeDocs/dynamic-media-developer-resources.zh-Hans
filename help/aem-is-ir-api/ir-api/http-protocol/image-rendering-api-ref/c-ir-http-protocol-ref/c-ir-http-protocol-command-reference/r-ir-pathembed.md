---
title: pathEmbed
description: 嵌入路径数据。 指定晕影中嵌入的Photoshop路径是否应包含在响应图像中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# pathEmbed{#pathembed}

嵌入路径数据。 指定晕影中嵌入的Photoshop路径是否应包含在响应图像中。

`pathEmbed=0|1`

## 属性 {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

请求属性。 如果晕影不包含路径数据，则忽略。 如有必要，路径数据将缩放为`wid=`和/或`hei=`。

如果输出图像格式不支持路径嵌入，则忽略。 有关支持路径嵌入的输出图像格式列表，请参阅`fmt=`的说明。

## 默认 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`，用于在输出图像中不嵌入路径。

## 另请参阅 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)，[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)，[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
