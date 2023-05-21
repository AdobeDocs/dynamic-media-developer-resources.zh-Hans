---
description: 調整色彩平衡。 分別調整每個RGB色彩元件的值。
solution: Experience Manager
title: op_colorbalance
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 93476778-97b0-4ad5-b22a-093239e845f0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 1%

---

# op_colorbalance{#op-colorbalance}

調整色彩平衡。 分別調整每個RGB色彩元件的值。

`op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>紅色元件調整(-100...+100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>綠色元件調整(-100...+100 int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>藍色元件調整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

灰階和CMYK輸入影像資料會使用簡單轉換轉換為RGB，這在啟用色彩管理時是不準確的。

## 屬性 {#section-dff9c934f7c1442bbd02379b688d82e2}

圖層指令。 套用至目前圖層或複合影像，如果 `layer=comp`. 被效果圖層忽略。 CMYK影像和圖層會在套用作業之前轉換為RGB。

## 默认 {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` 不會變更顏色。

## 示例 {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

將色彩平衡朝紅色推進：

… `&op_colorBalance=100,0,0&`…
