---
description: 圖層影像。
solution: Experience Manager
title: src
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# src{#src}

圖層影像。

` src= *`物件`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>影像物件。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>巢狀影像伺服、影像演算或外部請求。 </p> </td> 
 </tr> 
</table>

## 说明 {#section-59ec6dc2afcb43efb34dbb0f7733543f}

指定影像圖層的來源影像。

*`object`* 可以是目錄專案或影像/SVG檔案。

另請參閱 [物件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

巢狀或內嵌請求會以大括弧括住。 為內嵌影像伺服請求加上前置詞 `is`，內嵌影像演算要求，具有 `ir`，以及包含下列專案的FXG圖形轉譯請求： `fxg`. 如果未指定前置詞，則會假設對外來伺服器的要求。

另請參閱 [請求巢狀內嵌與內嵌](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## 屬性 {#section-2c22bb89a35d470f833df8ba898efd93}

圖層屬性。 套用至 `layer=0` 如果 `layer=comp`. 互斥 `text=` 和 `textPs=` 在相同圖層中；最後出現的 `text=`， `textPs=`，或 `src=` 會取勝並判斷這是影像還是文字圖層。 被效果圖層忽略。

*`object`*可能無法解析為其他包含 `src=` 或 `mask=` 命令在其中 `catalog::Modifier`. （使用請求巢狀可達到類似的效果。）

此 `is`， `ir`、和 `fxg` 首碼區分大小寫。

## 默认 {#section-a92f3882041b4d43ae2caf014647165f}

針對第0層，使用URL的路徑元件中的物件，如果 `src=` 未指定。 沒有其他圖層的預設值。

## 另请参阅 {#section-e467e03330564796932ac081f1c9c1d0}

[catalog：：Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ， [attribute：：RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)， [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f)， [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [物件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)， [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)， [請求巢狀內嵌與內嵌](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
