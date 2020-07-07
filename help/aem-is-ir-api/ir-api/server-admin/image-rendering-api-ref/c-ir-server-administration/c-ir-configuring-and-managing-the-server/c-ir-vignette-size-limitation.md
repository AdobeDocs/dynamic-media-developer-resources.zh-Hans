---
description: “图像渲染”对非金字塔晕影实施两百万像素大小限制。
seo-description: “图像渲染”对非金字塔晕影实施两百万像素大小限制。
seo-title: 暗角大小限制
solution: Experience Manager
title: 暗角大小限制
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# 暗角大小限制{#vignette-size-limitation}

“图像渲染”对非金字塔晕影实施两百万像素大小限制。

如果应用程序 `IrMaxNonPyrVignetteSize` 需要支持图像区域（宽x高）大 *[!DNL install_root]* 于此限制的非金字塔晕影，请修改[!DNL /ImageServing/conf /ImageServerRegistry.conf]中的值。

>[!NOTE]
>
>`attribute::MaxPix` 并且 `IS::MaxMessageSize` 可能需要进行调整，以允许异常大的响应图像大小。 有关详细信息，请参阅图像服务文档。

