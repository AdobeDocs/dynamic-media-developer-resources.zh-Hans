---
title: 量化
description: 色彩量化。 指定GIF輸出轉換的色彩量化屬性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# 量化{#quantize}

色彩量化。 指定GIF輸出轉換的色彩量化屬性。

` quantize= *`type`*[, *`遞色`*[, *`numColors`*[, *`顏色清單`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>指定調色盤型別。 </p> <p>設定為 <span class="codeph"> 最適化 </span> 以計算影像的最佳調色盤。 </p> <p>設定為 <span class="codeph"> 網頁 </span> 或 <span class="codeph"> mac </span> 以選擇預先定義的調色盤。 </p> <p> <p>注意： <span class="codeph"> mac </span> 僅GIF和PNG8格式支援托盤型別，但GIFAlpha和PNG8 Alpha格式則不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 遞色 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {擴散|關閉} </span> </p> <p>指定遞色選項。 </p> <p>設定為 <span class="codeph"> 擴散 </span> 對於Floyd-Steinberg誤差擴散 </p> <p>設定為 <span class="codeph"> 關閉 </span> 以停用遞色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>輸出色彩數量(2-256) </p> <p>指定包含多少顏色 <span class="codeph"> 最適化 </span> 調色盤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 顏色清單 </span> </span> </p> </td> 
   <td colname="col2"> <p>以逗號分隔的hex6格式強制RGB顏色清單 </p> <p>可讓您指定要包含在 <span class="codeph"> 最適化 </span> 調色盤。 如果指定的顏色數目小於 <span class="codeph"> <span class="varname"> numColors </span> </span>，會根據影像內容計算其他顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-8ab5035055b24b858270d260912a7f3d}

要求屬性。 無論目前的圖層設定為何，均適用。 僅在以下情況下使用： `fmt=gif`， `fmt=gif-alpha`， `fmt=png8`，或 `fmt=png8-alpha`. 否則會忽略。

指定的顏色 *`colorList`* 必須包含十六進位6格式的RGB值(請參閱 [顏色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) 不含 `0x` 前置詞。 不允許使用其他顏色指定字。 *`numColors`* 必須介於2到256之間。

## 默认 {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## 示例 {#section-e34aca7587d548a7ae9d4266b80c9451}

使用產生GIF縮圖 `web` 浮動視窗且無遞色：

` http:// *`伺服器`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

將影像轉換為具有關鍵色彩透明度的雙調GIF，並強制將色彩轉換為黑白：

` http:// *`伺服器`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## 另请参阅 {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ， [顏色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
