---
title: 晕影大小限制
description: 图像渲染会对非金字塔晕影实施200万像素大小限制。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
TQID: 'https://experienceleague.adobe.com/qPrnkvYXinvZAfx-s6ePjpe64qsoBfwtVbUJ-fYBbmc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# 晕影大小限制{#vignette-size-limitation}

图像渲染会对非金字塔晕影实施200万像素大小限制。

如果您的应用程序需要支持图像区域（宽度x高度）大于此限制的非金字塔晕影，请修改[！DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf]中的`IrMaxNonPyrVignetteSize`值。

>[!NOTE]
>
>调整属性`attribute::MaxPix`和`IS::MaxMessageSize`以允许异常大的响应图像大小。 有关详细信息，请参阅图像服务文档。

