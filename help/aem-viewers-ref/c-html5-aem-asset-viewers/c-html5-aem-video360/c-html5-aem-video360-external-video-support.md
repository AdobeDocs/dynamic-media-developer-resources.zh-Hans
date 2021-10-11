---
title: 外部视频支持
description: 查看器支持播放在Dynamic Media Classic或Dynamic MediaAdobe Experience Manager以外托管的视频。
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

查看器支持播放在Dynamic Media Classic或Dynamic MediaAdobe Experience Manager以外托管的视频。

外部视频支持的格式为H.264格式的MP4或HLS流的M3U8清单。

查看器可以使用Dynamic Media Classic、Experience ManagerDynamic Media视频，也可以使用外部视频。 如果查看器以Dynamic Media Classic/AEM Dynamic Media视频开头，则应将其与此类资产类型一起使用。 无法使用[setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法将外部视频加载到此查看器中，反之则无法加载。 也就是说，如果查看器最初加载了外部视频，则它将继续仅用于外部视频。

使用外部视频时，查看器会忽略任何播放修饰符的值，并检测来自外部视频扩展的播放类型。 如果外部视频URL以`.m3u8`结尾，则查看器使用的是HLS播放；否则，使用渐进式播放。
