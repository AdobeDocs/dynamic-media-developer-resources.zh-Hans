---
title: 外部视频支持
description: 查看器支持播放在Dynamic Media Classic或Adobe Experience Manager、Dynamic Media之外托管的视频。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 外部视频支持{#external-video-support}

查看器支持播放在Dynamic Media Classic或Adobe Experience Manager、Dynamic Media之外托管的视频。

外部视频支持的格式为H.264格式的MP4或HLS流的M3U8清单。

查看器可以处理Dynamic Media Classic或Experience ManagerDynamic Media视频，也可以处理外部视频。 如果查看者首先查看Dynamic Media Classic/AEM Dynamic Media视频，则以后应将其用于此类资源类型。 无法使用将外部视频加载到此查看器中 [setvideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 方法，反之亦然。 也就是说，如果查看器最初加载了外部视频，则它将继续只处理外部视频。

处理外部视频时，查看器会忽略playback修饰符的值，并从外部视频扩展中检测播放类型。 如果外部视频URL的结尾为 `.m3u8`时，查看器使用的是HLS播放；否则，将使用渐进式播放。
