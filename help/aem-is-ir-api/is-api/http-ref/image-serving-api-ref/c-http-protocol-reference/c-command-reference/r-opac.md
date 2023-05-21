---
description: 調整影像不透明度。 允許減少影像、文字、純色或效果圖層的前景不透明度。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38e0e1dc-46c0-48a4-b676-f7e6d262392f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---

# opac{#opac}

調整影像不透明度。 允許減少影像、文字、純色或效果圖層的前景不透明度。

`opac= *`不透明度`*[, *`填色不透明度`*]`

<table id="simpletable_DA4B5D86C496480886FADB284AD6047F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 不透明度</span> </p> </td> 
  <td class="stentry"> <p>主要不透明度（0到100位元整數）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 填色不透明度</span> </p></td> 
  <td class="stentry"> <p>填色不透明度（0到100位元整數）。 </p></td> 
 </tr> 
</table>

影像圖層的前景不透明度由影像的圖層遮色片或Alpha色版決定，如果兩者都不存在，則為100%。 文字圖層的前景不透明度為100%，而純色圖層的前景不透明度則由 `color=`.

`opac=` 絕不修改填入區域的不透明度 `color=` 或 `bgColor=`，但純色和效果圖層的前景區域除外(設定為 `color=`)。

在影像、文字或純色圖層中指定時， *`opacity`* 套用整個圖層，包括所有關聯的效果圖層，同時 *`fillOpacity`* 僅套用至主要圖層內容。 在效果圖層中指定時， *`opacity`* 套用至效果圖層，而 *`fillOpacity`* 會忽略。

主要圖層內容的有效不透明度是( *`opacity`* &#42; *`fillOpacity`* / 100)。 效果圖層的有效不透明度為（主要） *`opacity`* &#42; 效果 *`opacity`* / 100)。

## 屬性 {#section-ac3f136ff1584a2eab87500b7164f7fa}

圖層屬性。 套用至目前圖層或複合影像，如果 `layer=comp`.

## 默认 {#section-abba67ed028049048ae43405ea69b164}

`opac=100,100`，不會改變圖層不透明度。

## 示例 {#section-9710810e96af40538652e8ae4aadd3be}

… `&layer=1&text=variable%20opacity&opac=90,70&effect=-1&opac=50&`…

此範例中的文字不透明度為90&#42;70/100=63%，而效果圖層不透明度為90&#42;50/100=45%。

## 另请参阅 {#section-dbdad35ccd544590b4b11d31a9ab062e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ， [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)
