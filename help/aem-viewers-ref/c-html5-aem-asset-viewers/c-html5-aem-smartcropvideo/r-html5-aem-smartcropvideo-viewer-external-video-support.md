---
title: 外部視訊支援
description: 檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media外部託管的視訊。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 2ab5a083-5995-440a-a9a6-6642277b8a58
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# 外部視訊支援{#external-video-support}

檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager - Dynamic Media外部託管的視訊。

支援的外部視訊格式為H.264格式的MP4或HLS資料流的M3U8資訊清單。

檢視器可搭配Dynamic Media Classic或Experience Manager - Dynamic Media影片或外部影片使用。 如果檢視器從Dynamic Media Classic/Dynamic Media影片開始，並搭配此類資產型別使用，則無法使用將外部影片載入此檢視器 [`setVideo`]
(../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c)方法。 反過來：如果檢視器最初是透過外部視訊載入，則應僅繼續使用外部視訊。

使用外部視訊時，檢視器會忽略playback修飾元的值，並從外部視訊擴充功能中偵測播放型別。 如果外部視訊URL結尾為 `.M3U8` 檢視器使用HLS播放，否則使用漸進式播放。
