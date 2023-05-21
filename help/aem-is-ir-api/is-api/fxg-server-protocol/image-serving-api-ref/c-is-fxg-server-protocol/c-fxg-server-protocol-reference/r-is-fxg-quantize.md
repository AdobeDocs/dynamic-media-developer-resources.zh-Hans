---
description: 色彩量化。 指定GIF輸出轉換的色彩量化屬性。
solution: Experience Manager
title: 量化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---

# 量化{#quantize}

色彩量化。 指定GIF輸出轉換的色彩量化屬性。

` quantize= *`type`*[, *`遞色`*[, *`numColors`*[, *`顏色清單`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> 調色盤型別 </p> <p>選取' <span class="codeph"> 網頁 </span>'或' <span class="codeph"> mac </span>'以選擇預先定義的調色盤，或設為' <span class="codeph"> 最適化 </span>'以計算影像的最佳調色盤。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 遞色 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {擴散|關閉} </span> 遞色選項 </p> <p>選取Floyd-Steinberg誤差擴散的「擴散」或「關閉」以停用遞色。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>「 」中包含的輸出顏色數量（整數） <span class="codeph"> 最適化 </span>'調色盤。 </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> 必須介於2到256之間。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 顏色清單 </span> </span> </p> </td> 
  <td class="stentry"> <p>以逗號分隔的hex6格式強制RGB顏色清單。 可讓您指定要包含在「 <span class="codeph"> 最適化 </span>'調色盤。 如果指定的顏色數目小於 <span class="codeph"> numColors </span>，會根據影像內容計算其他顏色。 </p> <p>僅在以下情況下使用： <span class="codeph"> fmt=gif </span> 或 <span class="codeph"> fmt=gif-alpha </span>. 否則會忽略。 指定的顏色 <span class="codeph"> <span class="varname"> 顏色清單 </span> </span> 必須是十六進位6格式的RGB值(請參閱 <span class="codeph"> 顏色 </span>)；不允許使用其他顏色指定元。 </p> </td> 
 </tr> 
</table>

## 默认 {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## 示例 {#section-b3a979dc9ae3459baa093bf17310988f}

使用「 」產生GIF縮圖 `web`&#39;浮動視窗且無遞色：

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

將影像轉換為具有關鍵色彩透明度的雙調GIF，並強制將色彩轉換為黑白：

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
