---
title: opac
description: 不透明度. 指定材質不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# opac{#opac}

不透明度. 指定材質不透明度。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>材質不透明度（百分比）；0到100 </p> </td> 
 </tr> 
</table>

下列材質/物件組合支援可變不透明度：

* 套用至紋理重疊物件的純色和可重複紋理。
* 套用至視窗覆蓋物件之視窗覆蓋物材料。
* 貼花套用到紋理物件或牆物件。

如果材質包含具有Alpha色版的影像， `opac=` 可用來讓影像更透明，但不是更不透明。

## 屬性 {#section-352f7b82ede54159b6afb90ae4b559ec}

材質屬性。 如果目前物件選取範圍或材料不支援不透明度，則忽略。

## 默认 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`，適用於完全不透明的材質（如果影像不包含Alpha色版）。
