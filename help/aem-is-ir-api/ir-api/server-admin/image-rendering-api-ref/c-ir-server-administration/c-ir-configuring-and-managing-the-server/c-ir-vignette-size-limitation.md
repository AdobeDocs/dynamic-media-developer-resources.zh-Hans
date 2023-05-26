---
description: 图像渲染会对非金字塔晕影实施200万像素大小限制。
solution: Experience Manager
title: 晕影大小限制
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# 晕影大小限制{#vignette-size-limitation}

图像渲染会对非金字塔晕影实施200万像素大小限制。

修改值 `IrMaxNonPyrVignetteSize` 在[！DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]如果您的应用程序需要支持图像区域（宽度x高度）大于此限制的非金字塔晕影。

>[!NOTE]
>
>`attribute::MaxPix` 和 `IS::MaxMessageSize` 可能还需要调整以允许异常大的响应图像大小。 有关详细信息，请参阅图像服务文档。
