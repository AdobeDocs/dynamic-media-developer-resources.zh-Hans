---
title: 外部视频支持
description: 查看器支持播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media之外托管的视频。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 外部视频支持{#external-video-support}

查看器支持播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media之外托管的视频。

外部视频支持的格式为H.264格式的MP4或HLS流的M3U8清单。

查看器可以处理Dynamic Media Classic或Experience Manager - Dynamic Media视频或外部视频。 如果查看者首先查看Dynamic Media Classic/Dynamic Media视频，然后将其与此类资源类型一起使用，则无法使用将外部视频加载到此查看者中 [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法。 反之：如果查看器最初加载了外部视频，则它应该只处理外部视频。

处理外部视频时，查看器会忽略playback修饰符的值，并从外部视频扩展中检测播放类型。 如果外部视频URL的结尾为 `.M3U8` 查看器正在使用HLS播放，否则使用渐进式播放。
