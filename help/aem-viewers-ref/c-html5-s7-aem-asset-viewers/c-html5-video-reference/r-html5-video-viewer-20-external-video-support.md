---
description: 查看器支持播放在Scene7出版系统或AEMDynamic Media之外托管的视频。
seo-description: 查看器支持播放在Scene7出版系统或AEMDynamic Media之外托管的视频。
seo-title: 外部视频支持
solution: Experience Manager
title: 外部视频支持
topic: Dynamic Media
uuid: 24739a5a-3a5d-49b8-9a15-bcf3a95fc192
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---


# 外部视频支持{#external-video-support}

查看器支持播放在Scene7出版系统或AEMDynamic Media之外托管的视频。

外部视频支持的格式为H.264格式的MP4或HLS流的M3U8清单。

查看器可以使用Scene7或Dynamic Media视频，也可以使用外部视频。 如果查看器开始Scene7/Dynamic Media视频，则将其与此类资产类型结合使用，则无法使用[ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法将外部视频加载到此查看器中。 还有副词：如果查看器最初加载了外部视频，则应继续仅处理外部视频。

处理外部视频时，查看器会忽略播放修饰符的值，并检测来自外部视频扩展的播放类型。 如果外部视频URL以。m3u8结尾，则查看器正在使用HLS回放，否则将使用渐进式回放。
