---
description: 圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=套用至圖層。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# 大小{#size}

圖層大小。 指定圖層的大小或最大圖層大小，然後將rotate=、perspective=和extend=套用至圖層。

` size= *`寬度`*, *`高度`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度 </span>， <span class="varname"> 高度 </span> </span> </p> </td> 
  <td class="stentry"> <p>以畫素為單位的圖層大小限制（int、int、0或更大）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>， <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>相對於圖層0大小標準化圖層大小限制（實數、實數、0.0...1.0）。 </p> </td> 
 </tr> 
</table>

指定影像圖層時，size=會限制圖層影像的寬度或/或高度。 影像會縮放為不大於 `size=`. 如果指定了標準化大小，則它是相對於圖層0的大小。 若兩者皆有 *`width`* 和 *`height`* 指定時，會縮放來源影像(在 `crop=` 套用)，以使任何維度都不會超過指定的大小。 在所有情況下，來源矩形的外觀比例都會保持不變。 兩者之一 *`width`* 或 *`height`* 可設為0；在此情況下，值由伺服器根據影像的外觀比例計算。

指定文字圖層時， `size=` 指定文字方塊大小。 *`width`* 為必要項； *`height`* 可設為0，在此情況下，會使用已配置文字的高度作為圖層高度。 依預設，文字版面引擎會插入分行符號，以確保文字永遠水準符合可用的空間。 若 *`height`* 指定，不符合可用空間的行會被裁剪( `text=`)或省略( `textPs=`)。 `text=` 支援其他配合模式；請參閱 `textAttr=` 以取得詳細資訊。

指定純色圖層時， `size=` 定義確切的圖層大小；必須同時指定這兩個值（除非提供遮色片）。 若 `mask=` 也會指定，遮色片影像會調整大小以符合 `size=` 影像圖層中的影像縮放方式相同。

## 屬性 {#section-5f254b66fcba49bcb63f9c9ea40b230c}

圖層屬性。 套用至圖層0，如果 `layer=comp`. `sizeN=` 不允許用於 `layer=0` 或 `layer=comp`. `sizeN=` 允許用於 `layer=0` 和 `layer=comp` 僅限定義浮水印影像的目錄記錄中。 在這種情況下， `sizeN` 會定義相對於要套用浮水印之複合影像的浮水印影像縮放比例。 若 `size=` 已指定， `res=` 和 `scale=` 會忽略此圖層的。 被效果圖層忽略。

## 默认 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`，圖層大小不受限制。 如果是影像圖層，圖層大小會根據圖層影像大小來決定 `crop=`， `scale=`，或 `res=` 已套用作業。 對於文字圖層，如果 `size=` 未指定，則會自動調整圖層大小以符合演算後的文字。

純色圖層需要完全指定的 `size=`， a `mask=`，或 `clipPath=`.

## 示例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

另請參閱 [範例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 在 [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ， [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55)， [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)， [文字圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
