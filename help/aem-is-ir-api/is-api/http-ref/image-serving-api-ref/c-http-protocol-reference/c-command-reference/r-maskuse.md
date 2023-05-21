---
description: 影像遮色片使用方式。 指定影像的遮色片或Alpha色版如何用於影像上的操作（例如，colorize=）。 在效果圖層指定時，它允許將效果套用至父圖層的背景區域或整個父圖層矩形。
solution: Experience Manager
title: 遮色片使用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e99101a1-1747-454c-b0c0-3af3335c0497
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# 遮色片使用{#maskuse}

影像遮色片使用方式。 指定影像的遮色片或Alpha色版如何用於影像上的操作（例如，colorize=）。 在效果圖層指定時，它允許將效果套用至父圖層的背景區域或整個父圖層矩形。

`maskUse=norm|invert|off`

下表說明 `maskUse=` 視與圖層影像相關之遮色片（alpha色版）的可用性和型別而定。

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 無遮色片</b> </th> 
   <th class="entry"> <b> 未關聯的Alpha （或個別的遮色片影像）</b> </th> 
   <th class="entry"> <b> 相關（預乘） Alpha</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 關閉 </span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 在填滿實心黑色的矩形上的影像前景區域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 標準 </span> </p> </td> 
   <td> <p> 不透明影像矩形 </p> </td> 
   <td> <p> 影像的前景區域 </p> </td> 
   <td> <p> 影像或圖層的前景區域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 反轉 </span> </p> </td> 
   <td> <p> 隱藏圖層 </p> </td> 
   <td> <p> 影像的背景區域 </p> </td> 
   <td> <p> 以純黑色填滿的影像或圖層的背景區域 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f36ad1af348e45aeb3eb336544df30b0}

影像或圖層屬性。 套用至圖層0，如果 `layer=comp`. 如果在效果圖層指定，該指令會修改從父圖層繼承的遮色片。

的行為 `maskUse=` 未定義，且當無影像遮色片適用時，不支援使用文字或純色圖層(指定為 `mask=` 或 `catalog::Mask`)。

## 默认 {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## 示例 {#section-daa371e9be5547368ff6772342acba0a}

為影像的背景區域上色；影像前景是由單獨的遮色片影像所定義。 如果影像未修改，將彩色化的影像背景圖層放在上方即可達到此目的：

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## 另请参阅 {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
