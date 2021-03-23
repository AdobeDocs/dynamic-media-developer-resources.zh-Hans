---
description: 查看器支持播放在Dynamic Media Classic或AEM Dynamic Media之外托管的视频。
solution: Experience Manager
title: 外部视频支持
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# 外部视频支持{#external-video-support}

查看器支持播放在Dynamic Media Classic或AEM Dynamic Media之外托管的视频。

外部视频支持的格式为H.264格式的MP4或HLS流的M3U8清单。

查看器可以使用Dynamic Media Classic或AEM Dynamic Media视频，也可以使用外部视频。 如果查看器开始Dynamic Media Classic/Dynamic Media视频，则继续使用此类资产类型，则无法使用[ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法将外部视频加载到此查看器中。 还有副诗：如果查看器最初加载了外部视频，则应继续仅处理外部视频。

使用外部视频时，查看器会忽略播放修饰符的值，并检测来自外部视频扩展的播放类型。 如果外部视频URL以.m3u8结尾，则查看器正在使用HLS回放，否则使用渐进式回放。
