---
title: 颜色
description: 圖層色彩。 指定純色和效果圖層的前景色和不透明度，以及文字圖層的文字方塊填色顏色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 3%

---

# 颜色{#color}

圖層色彩。 指定純色和效果圖層的前景色和不透明度，以及文字圖層的文字方塊填色顏色。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 顏色 </span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK色彩值（含或不含Alpha）。 </p> </td> 
 </tr> 
</table>

如果是影像和文字圖層， `color=` 在*之前，以指定的顏色*填滿圖層邊界矩形內的透明和半不透明區域 `rotate=` 和 `extend=` 中所有規則的URL區段。

## 屬性 {#section-d6e74c36a49547849212e4db8927e678}

圖層屬性。 套用至目前圖層，或套用至圖層0，如果 `layer=comp`.

*`color`* 會假設存在於與下列畫素型別對應的工作色域中 *`color`*. *`color`* 如果圖層影像在合併時具有不同的畫素型別，則會精確轉換。

## 默认 {#section-60611c72876b4c45b5c85ce35608e5ec}

純色和效果圖層沒有預設值；必須指定顏色。 影像和文字圖層的預設值為0,0，0,0 （完全透明）。

## 示例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在下列範本片段中，我們將文字背景設定為50%不透明顏色，並使用相同顏色在第2層影像周圍新增半透明10畫素邊框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另请参阅 {#section-f0e059f857b64b61ab4f23312b8dc619}

[顏色](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)， [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)， [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)， [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)， [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
