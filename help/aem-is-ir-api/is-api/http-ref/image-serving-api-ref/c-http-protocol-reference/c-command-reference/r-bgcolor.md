---
description: 圖層背景顏色。 指定目前圖層的背景色彩和不透明度。
solution: Experience Manager
title: bgColor
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 22c957e6-1a82-43a7-8467-871a150e7453
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# bgColor{#bgcolor}

圖層背景顏色。 指定目前圖層的背景色彩和不透明度。

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 顏色</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK色彩值（含或不含Alpha）。 </p></td> 
 </tr> 
</table>

圖層邊界矩形內的透明和半不透明區域會在*之後以指定的顏色*填滿 `opac=`， `rotate=`、和 `extend=` 中所有規則的URL區段。

## 屬性 {#section-19dfc13e997f4a33889a1df1e4ad50b9}

圖層屬性。 套用至目前圖層，或套用至圖層0，如果 `layer=comp`. 被效果圖層忽略。

*`color`* 會假設存在於與下列畫素型別對應的工作色域中 *`color`*. *`color`* 如果最終圖層影像的畫素型別不同，則會精確轉換。

## 默认 {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0，0,0 （完全透明）。

## 示例 {#section-6e14fcf1d31e432dbdb56b9320904453}

另請參閱 [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## 另请参阅 {#section-64b3f153c6d94ab58f46e77324697818}

[顏色](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)， [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423)， [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172)， [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)， [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)， [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)， [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
