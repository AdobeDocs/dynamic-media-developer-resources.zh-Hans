---
description: 图像渲染强制对非金字塔晕影采用两百万像素大小限制。
solution: Experience Manager
title: 晕影大小限制
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# 晕影大小限制{#vignette-size-limitation}

图像渲染强制对非金字塔晕影采用两百万像素大小限制。

如果您的应用程序需要支持图像区域（宽x高）大于此限制的非金字塔晕影，请修改[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]中`IrMaxNonPyrVignetteSize`的值。

>[!NOTE]
>
>`attribute::MaxPix` 和可 `IS::MaxMessageSize` 能还需要进行调整，以允许异常大的响应图像大小。有关详细信息，请参阅图像提供文档。
