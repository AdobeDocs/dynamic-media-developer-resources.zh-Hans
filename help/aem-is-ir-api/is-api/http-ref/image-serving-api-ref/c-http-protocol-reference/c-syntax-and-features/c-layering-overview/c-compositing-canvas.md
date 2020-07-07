---
description: 图层按layer=命令指定的顺序合成，其中编号较高的图层会隐藏编号较低的图层。
seo-description: 图层按layer=命令指定的顺序合成，其中编号较高的图层会隐藏编号较低的图层。
seo-title: 合成画布
solution: Experience Manager
title: 合成画布
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# 合成画布{#the-compositing-canvas}

图层按layer=命令指定的顺序合成，其中编号较高的图层会隐藏编号较低的图层。

第0层构成背景层，它始终是必需的，并定义复合图像的大小。 允许对层0使用任何层类型。 必须根据内容图像或文本显式地使用或 `size=` 隐式地定义图层0的大小。 输出图像中不包括位于层0区域之外的其他层的任何区域。

>[!NOTE]
>
>拼合所有图层后，复合图像将转换为最终响应图像，如使用视图命令和属 [性所指定](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)。

