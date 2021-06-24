---
description: SvgRender组件是独立的Java应用程序。
solution: Experience Manager
title: 配置SVG
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 9013e13f-818f-41b4-80b6-2615d9a8742f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 2%

---

# 配置SVG{#configuring-svg}

SvgRender组件是独立的Java应用程序。

SVG配置设置位于[!DNL PlatformServer.conf]、[!DNL SVG.conf]、[!DNL ImageServerRegistry.xml]和[!DNL ServerSupervisorRegistry.xml]中。

套接字连接用于在SvgRender和图像服务器之间通信。 端口号是27346。 如有必要，可通过将[!DNL svg.conf]中的`SVGRender.port`和[!DNL ImageServerRegistry.xml]中的`<SVGTcpPort>`设置为新值来更改此值。

## 另请参阅 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG配置设置](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
