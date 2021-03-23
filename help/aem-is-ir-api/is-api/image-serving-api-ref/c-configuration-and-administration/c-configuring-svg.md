---
description: SvgRender组件是独立的Java应用程序。
seo-description: SvgRender组件是独立的Java应用程序。
seo-title: 配置SVG
solution: Experience Manager
title: 配置SVG
uuid: f6e131af-283e-4649-b349-123489c0838d
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 2%

---


# 配置SVG{#configuring-svg}

SvgRender组件是独立的Java应用程序。

SVG配置设置位于[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]和[!DNL ServerSupervisorRegistry.xml]中。

套接字连接用于在SvgRender和图像服务器之间通信。 端口号是27346。 如有必要，可将[!DNL svg.conf]中的`SVGRender.port`和[!DNL ImageServerRegistry.xml]中的`<SVGTcpPort>`设置为新值，以更改该值。

## 另请参阅 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG配置设置](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
