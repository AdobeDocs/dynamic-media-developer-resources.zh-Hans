---
description: SvgRender组件是独立的Java应用程序。
seo-description: SvgRender组件是独立的Java应用程序。
seo-title: 配置SVG
solution: Experience Manager
title: 配置SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: f6e131af-283e-4649-b349-123489c0838d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 配置SVG{#configuring-svg}

SvgRender组件是独立的Java应用程序。

SVG配置设置位于、 [!DNL PlatformServer.conf]、 [!DNL SVG.conf]和 [!DNL ImageServerRegistry.xml]中 [!DNL ServerSupervisorRegistry.xml]。

套接字连接用于在SvgRender和图像服务器之间通信。 端口号为27346。 如果需要，可以通过将中值和中 `SVGRender.port` 值设 [!DNL svg.conf] 置 `<SVGTcpPort>` 为新 [!DNL ImageServerRegistry.xml] 值来更改它。

## 另请参阅 {#section-c085b47d54d44059bdaa67fd5e226e91}

[SVG配置设置](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-svg.md#reference-232104868b2d4af9a4ac9c87552c0bb5)
