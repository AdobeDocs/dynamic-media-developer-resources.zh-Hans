---
description: 圖層位置。
solution: Experience Manager
title: pos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---

# pos{#pos}

圖層位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 座標</span> </p> </td> 
  <td class="stentry"> <p>從這個圖層原點到圖層0原點的畫素位移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>從此圖層原點到圖層0原點的標準化位移（實數、實數）。 </p></td> 
 </tr> 
</table>

如果是影像、文字和純色圖層， `pos=` 指定圖層錨點相對於圖層0錨點的位置。 `posN=` 座標值會相對於實際圖層0的矩形大小進行標準化。

如果是效果層， `pos=` 相對於父圖層移動效果圖層。

正值會向右/下移動圖層，而負值則會向左/上移動。 `posN=0.5,0.5` 將圖層上下移動一半的寬度和高度，即圖層0。

## 屬性 {#section-51a60cdc52d040538fef378ace7c2e7d}

圖層屬性。 忽略條件 `layer=0` 或 `layer=comp`.

## 默认 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 如果是影像、文字或純色圖層，這會把圖層錨點放在與0層錨點相同的位置。 將效果圖層直接置於其父圖層之上或之下。

## 示例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

請參閱中的範例A [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
