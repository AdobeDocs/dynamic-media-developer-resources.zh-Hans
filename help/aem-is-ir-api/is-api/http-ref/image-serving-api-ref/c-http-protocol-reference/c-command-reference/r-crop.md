---
description: 裁切影像。 指定矩形裁切區域，以畫素表示，或相對於完整解析度來源影像或遮色片影像進行標準化。
solution: Experience Manager
title: 裁切
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# 裁切{#crop}

裁切影像。 指定矩形裁切區域，以畫素表示，或相對於完整解析度來源影像或遮色片影像進行標準化。

`crop= *`座標`*, *`大小`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 座標</span></span> </p> </td> 
  <td class="stentry"> <p>從來源影像左上角到裁切矩形(int， int)左上角的畫素位移。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>從來源影像左上角到裁切矩形左上角的標準化位移（真實、真實）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大小</span></span> </p></td> 
  <td class="stentry"> <p>裁切矩形的大小，以畫素為單位(int、int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>相對於來源影像大小的裁切矩形標準化大小（實數、實數）。 </p></td> 
 </tr> 
</table>

也可以用來透過指定負的x、y值和/或寬度、高度值來延伸影像超過其邊界，大於影像寬度、高度。 在這種情況下，延伸區域是完全透明的(除非 `bgColor=` （已指定）。

## 屬性 {#section-632e0405bb9940679b5f8b1c10e0902e}

來源影像/遮色片屬性。 套用至0層來源影像，如果 `layer=comp`. 被與來源影像或遮色片無關的圖層忽略。

## 默认 {#section-41f62d386c664f77952bc22e7286bb88}

整個影像( `cropN=0,0,1,1`)。

## 示例 {#section-2c99b481c0a04321979a3b522aa295d1}

**裁切左側10%和右側10%：**

`…&cropN=0.1,0,0.8,1&…`

**裁切影像底部邊緣20%：**

`…&cropN=0,0,1,0.8&…`

## 另请参阅 {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[裁切路徑](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ， [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
