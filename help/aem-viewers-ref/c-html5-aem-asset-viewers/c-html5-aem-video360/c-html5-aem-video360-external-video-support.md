---
description: 查看器支持播放在Dynamic Media经典或AEMDynamic Media之外托管的视频。
solution: Experience Manager
title: 外部视频支持
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# 外部视频支持{#external-video-support}

查看器支持播放在Dynamic Media经典或AEMDynamic Media之外托管的视频。

外部视频支持的格式为H.264格式的MP4或HLS流的M3U8清单。

查看器可以使用Dynamic Media经典或AEMDynamic Media视频，也可以使用外部视频。 如果查看器开始了Dynamic Media经典/Dynamic Media视频，则应将其与此类资产类型结合使用。 无法使用[setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法将外部视频加载到此查看器中，反之亦然。 即，如果查看器最初加载了外部视频，则它继续仅用于外部视频。

处理外部视频时，查看器会忽略任何播放修饰符的值，并从外部视频扩展检测播放类型。 如果外部视频URL以`.m3u8`结尾，则查看器正在使用HLS播放；否则，使用渐进式播放。
