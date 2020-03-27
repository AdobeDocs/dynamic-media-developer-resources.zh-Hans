---
description: 默认渲染图像大小。 如果请求未使用wid=或hei=明确指定视图大小，则服务器将限制返回图像不大于此宽度和高度。
seo-description: 默认渲染图像大小。 如果请求未使用wid=或hei=明确指定视图大小，则服务器将限制返回图像不大于此宽度和高度。
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 27574811-a920-4e54-8635-5a643b8655ef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultPix{#defaultpix}

默认渲染图像大小。 如果请求未使用wid=或hei=明确指定视图大小，则服务器将限制返回图像不大于此宽度和高度。

## 属性 {#section-9dc5474fc75842308796ab6440b29611}

两个整数，0或更大，以逗号分隔。 宽度和高度（以像素为单位）。 可以将任一或两个值都设置为0以保持它们不受约束。

不适用于嵌套／嵌入请求。

## 默认 {#section-1935781c561e4679aa87a5bcced8df90}

如果未定义 `default::DefaultPix` 或为空，则从中继承。

## 另请参阅 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)，属 [性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
