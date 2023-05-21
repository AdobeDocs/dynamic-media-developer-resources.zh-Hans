---
title: 外部視訊支援
description: 檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager、Dynamic Media以外託管的視訊。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# 外部視訊支援{#external-video-support}

檢視器支援播放在Dynamic Media Classic或Adobe Experience Manager、Dynamic Media以外託管的視訊。

支援的外部視訊格式為H.264格式的MP4或HLS資料流的M3U8資訊清單。

檢視器可處理Dynamic Media Classic或Experience Manager Dynamic Media影片或外部影片。 如果檢視器以Dynamic Media Classic/AEM Dynamic Media影片開始，則應將其用於未來的這類資產型別。 無法使用將外部視訊載入此檢視器 [setvideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) 方法，反之亦然。 也就是說，如果檢視器最初是隨外部視訊載入，它只會繼續搭配外部視訊運作。

使用外部視訊時，檢視器會忽略任何playback修飾元的值，並從外部視訊擴充功能中偵測播放型別。 如果外部視訊URL結尾為 `.m3u8`，檢視器會使用HLS播放，否則會使用漸進式播放。
