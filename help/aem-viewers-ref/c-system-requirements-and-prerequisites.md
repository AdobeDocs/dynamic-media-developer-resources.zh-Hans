---
title: Dynamic Media HTML5查看器的系统要求
description: Dynamic Media HTML5查看器的系统要求。
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Dynamic Media HTML5 Viewers系统要求{#system-requirements}

Dynamic Media HTML5查看器的系统要求。

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## 服务器硬件和软件 {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media图像服务6.7.1或更高版本。
* HTML5查看器需要SDK JavaScript服务器端库3.11.5或更高版本。
* *向Friend发送电子邮件*&#x200B;社交功能需要s7ondemand 5.0.9或更高版本。
* eCatalog查看器 — [信息面板弹出窗口](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md)支持需要信息服务器2.1.8或更高版本。
* 搜索功能组件需要s7search 2.3.0或更高版本。

## 查看器系统要求 {#section-cc72b1e209524d038b4d5b92b35e998e}

**组件查看器的客户端浏览器最低要求：**

* 在以下操作系统版本或更高版本上受支持：
   * Microsoft® Windows® 7
   * macOS X 10.12
* 在以下浏览器/平台版本或更高版本上受支持：
   * Android™操作系统4.x
   * 本机浏览器上的BlackBerry® 10。 仅支持视频播放。
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * IOS6
   * iPad 2(仅限Safari和Chrome浏览器)
   * iPhone 3GS
   * Safari 11
* 不支持移动设备上的Internet Explorer。
* 以下浏览器/平台版本或更高版本支持&#x200B;*PanoramicViewer*：
   * Android™ 4.4（仅限电话设备）
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* 以下浏览器/平台版本或更高版本支持&#x200B;*Video360Viewer*&#x200B;和&#x200B;*DimensionalViewer*：
   * Android™ 5（仅限电话设备）
   * Chrome 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* 以下浏览器/平台版本或更高版本支持&#x200B;*ZoomVerticalViewer*：
   * Android™ 4.x
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

## 停止对TLS 1.0和1.1的支持 {#tls}

<!-- CQDOC-19433 -->

自2022年9月30日起，Adobe Dynamic Media查看器已终止对以下内容的支持：

* TLS（传输层安全性） 1.0和1.1
* TLS 1.2中的以下弱加密：
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

## Dynamic Media查看器不支持的Web浏览器和操作系统组合 {#browser-os-support}

<!-- CQDOC-19433 -->

Adobe Dynamic Media查看器不支持以下Web浏览器和操作系统的组合：

* Internet Explorer 11 + Windows 7
* Internet Explorer 11 + Windows 8.1
* Internet Explorer 11 + Windows Phone 8.1
* Internet Explorer 11 + Windows Phone 8.1更新
* Safari 6 + iOS 6.0.1
* Safari 7 + iOS 7.1
* Safari 7 + OS X 10.9小牛
* Safari 8 + iOS 8.4
* Safari 8 + OS X 10.10 Yosemite

<!-- CQDOC-19433 -->

<!-- 
NOTE
Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android&trade; 2.3.7
* Android&trade; 4.0.4
* Android&trade; 4.1.1
* Android&trade; 4.2.2
* Android&trade; 4.3
* Internet Explorer 7 on Window Vista&reg;
* Internet Explorer 8 on Windows&reg; XP
* Internet Explorer 8-10 on Windows&reg; 7
* Internet Explorer 10 on Windows&reg; Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java&trade; 6u45
* Java&trade; 7u25
* OpenSSL 0.9.8y
* Baidu January 2015

NOTE
FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->

