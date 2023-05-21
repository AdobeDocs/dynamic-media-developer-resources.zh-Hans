---
title: 外部視訊支援
description: 檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media外部託管的視訊。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# 外部視訊支援{#external-video-support}

檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media外部託管的視訊。

支援的外部視訊格式為H.264格式的MP4或HLS資料流的M3U8資訊清單。

檢視器可搭配Dynamic Media Classic或Experience Manager - Dynamic Media影片或外部影片使用。 如果檢視器從Dynamic Media Classic/Dynamic Media影片開始，並搭配此類資產型別使用，則無法使用將外部影片載入此檢視器 [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 方法。 反過來：如果檢視器最初是透過外部視訊載入，則應僅繼續使用外部視訊。

使用外部視訊時，檢視器會忽略playback修飾元的值，並從外部視訊擴充功能中偵測播放型別。 如果外部視訊URL結尾為 `.m3u8` 檢視器使用HLS播放，否則使用漸進式播放。
