---
title: 外部视频支持
description: 查看器支持播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media之外托管的视频。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# 外部视频支持{#external-video-support}

查看器支持播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media之外托管的视频。

外部视频支持的格式为H.264格式的MP4或HLS流的M3U8清单。

查看器可以是Dynamic Media Classic，也可以是Experience Manager - Dynamic Media视频或外部视频。 如果查看器首先显示Dynamic Media Classic/Dynamic Media视频，然后将其用于此类资源类型，则无法使用[`setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法将外部视频加载到此查看器中。 反之：如果查看器最初加载了外部视频，则它应该只处理外部视频。

处理外部视频时，查看器会忽略playback修饰符的值，并检测外部视频扩展中的播放类型。 如果外部视频URL以`.m3u8`结尾，则查看器正在使用HLS播放，否则使用渐进式播放。
