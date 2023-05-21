---
title: Dynamic Media HTML5檢視器的系統需求
description: Dynamic Media HTML5檢視器的系統需求。
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 7793e9befcf3050b9f4e12deeffa018d7c91aaf7
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 1%

---

# Dynamic Media HTML5檢視器系統需求{#system-requirements}

Dynamic Media HTML5檢視器的系統需求。

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 伺服器硬體與軟體 {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1或更新版本。
* HTML5檢視器需要SDK JavaScript伺服器端程式庫3.11.5或更新版本。
* *傳送電子郵件給朋友* 社交功能需要s7ondemand 5.0.9或更新版本。
* eCatalog檢視器 —  [資訊面板快顯視窗](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) 支援需要info server 2.1.8或更新版本。
* 搜尋功能元件需要s7search 2.3.0或更新版本。

## 檢視器系統需求 {#section-cc72b1e209524d038b4d5b92b35e998e}

**元件檢視器的使用者端瀏覽器最低需求：**

* 支援下列作業系統版本或更新版本：
   * Microsoft® Windows® 7
   * macOS X 10.12
* 支援下列瀏覽器/平台版本或更新版本：
   * Android™作業系統4.x
   * 原生瀏覽器上的BlackBerry® 10。 僅支援視訊播放。
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 （僅限Safari和Chrome瀏覽器）
   * iPhone 3GS
   * Safari 11
* 不支援行動裝置上的Internet Explorer。
* *全景檢視器* 支援下列瀏覽器/平台版本或更新版本：
   * Android™ 4.4 （僅限手機裝置）
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Video360Viewer* 和 *維度檢視器* 支援下列瀏覽器/平台版本或更新版本：
   * Android™ 5 （僅限手機裝置）
   * Chrome 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* 支援下列瀏覽器/平台版本或更新版本：
   * Android™ 4.x
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## 終止支援TLS 1.0和1.1 {#tls}

<!-- CQDOC-19433 -->

自2022年9月30日起，AdobeDynamic Media檢視器將停止支援下列專案：

* TLS （傳輸層安全性） 1.0和1.1
* TLS 1.2中的下列弱加密：
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
   * TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
   * TLS_RSA_WITH_AES_256_GCM_SHA384
   * TLS_RSA_WITH_AES_256_CBC_SHA256
   * TLS_RSA_WITH_AES_256_CBC_SHA
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
   * TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_AES_128_GCM_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA256
   * TLS_RSA_WITH_AES_128_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_256_CBC_SHA
   * TLS_RSA_WITH_CAMELLIA_128_CBC_SHA
   * TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA
   * TLS_RSA_WITH_SDES_EDE_CBC_SHA

## Dynamic Media檢視器不支援的網頁瀏覽器和作業系統組合 {#browser-os-support}

<!-- CQDOC-19433 -->

AdobeDynamic Media檢視器不支援下列網頁瀏覽器和作業系統組合：

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Internet Explorer 11 + Windows Phone 8.1更新
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9小牛隊
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android™ 2.3.7
* Android™ 4.0.4
* Android™ 4.1.1
* Android™ 4.2.2
* Android™ 4.3
* Internet Explorer 7 on Window Vista®
* Internet Explorer 8 on Windows® XP
* Internet Explorer 8-10 on Windows® 7
* Internet Explorer 10 on Windows® Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java™ 6u45
* Java™ 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->

