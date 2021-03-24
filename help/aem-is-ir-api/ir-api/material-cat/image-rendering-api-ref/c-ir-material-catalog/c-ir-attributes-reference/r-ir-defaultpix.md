---
description: 默认渲染图像大小。 如果请求未使用wid=或hei=显式指定视图大小，则服务器将限制返回图像不大于此宽度和高度。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---


# DefaultPix{#defaultpix}

默认渲染图像大小。 如果请求未使用wid=或hei=显式指定视图大小，则服务器将限制返回图像不大于此宽度和高度。

## 属性 {#section-9dc5474fc75842308796ab6440b29611}

两个整数，0或更大，用逗号分隔。 宽度和高度（以像素为单位）。 可以将任一或两个值设置为0，以保持它们不受约束。

不适用于嵌套/嵌入请求。

## 默认 {#section-1935781c561e4679aa87a5bcced8df90}

如果未定义或为空，则从`default::DefaultPix`继承。

## 另请参阅 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [属性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
