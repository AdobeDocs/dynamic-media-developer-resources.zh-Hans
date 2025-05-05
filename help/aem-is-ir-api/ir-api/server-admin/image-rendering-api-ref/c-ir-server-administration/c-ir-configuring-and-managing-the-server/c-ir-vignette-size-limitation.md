---
title: 晕影大小限制
description: 图像渲染会对非金字塔晕影实施200万像素大小限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# 晕影大小限制{#vignette-size-limitation}

图像渲染会对非金字塔晕影实施200万像素大小限制。

如果您的应用程序需要支持图像区域（宽度x高度）大于此限制的非金字塔晕影，请修改[!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]中的`IrMaxNonPyrVignetteSize`值。

>[!NOTE]
>
>调整属性`attribute::MaxPix`和`IS::MaxMessageSize`以允许异常大的响应图像大小。 有关详细信息，请参阅图像服务文档。
