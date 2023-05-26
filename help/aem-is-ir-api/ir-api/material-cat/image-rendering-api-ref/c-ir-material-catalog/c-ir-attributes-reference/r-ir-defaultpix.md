---
title: Defaultpix
description: 默认渲染图像大小。 如果请求未使用wid=或hei=明确指定视图大小，服务器将限制回复图像不超过此宽度和高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---

# Defaultpix{#defaultpix}

默认渲染图像大小。 如果请求未使用wid=或hei=明确指定视图大小，服务器将限制回复图像不超过此宽度和高度。

## 属性 {#section-9dc5474fc75842308796ab6440b29611}

0或更大的两个整数，以逗号分隔。 宽度和高度（像素）。 可以将任一值或两个值都设置为0以保持其不受约束。

不适用于嵌套/嵌入的请求。

## 默认 {#section-1935781c561e4679aa87a5bcced8df90}

继承自 `default::DefaultPix` 如果未定义或为空。

## 另请参阅 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)， [attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
