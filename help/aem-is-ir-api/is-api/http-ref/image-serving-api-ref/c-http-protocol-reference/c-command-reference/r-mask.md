---
description: 影像遮色片。 指定要做為未關聯遮色片使用的個別遮色片影像。
solution: Experience Manager
title: 遮色片
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5785844b-945b-4dd0-ac59-efbf1360b7cd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 1%

---

# 遮色片{#mask}

影像遮色片。 指定要做為未關聯遮色片使用的個別遮色片影像。

`mask= *`物件`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>用作影像或圖層遮色片的影像物件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>巢狀影像伺服、影像演算或外部請求。 </p></td> 
 </tr> 
</table>

*`object`* 可以是目錄專案或影像/SVG檔案。 可以為影像圖層和純色圖層指定。

若 *`object`* 解析為影像目錄專案， `catalog::MaskPath` 已使用，或 `catalog::MaskPath` 未定義，則 `catalog::Path` 已使用。 若 *`object`* 無法解析為目錄專案，則會將其解譯為檔案路徑。

在所有情況下，如果來源影像有Alpha色版，則會使用它。 否則，如有必要，影像會先轉換為灰階，然後再用作圖層遮色片。

如果將遮色片附加至純色圖層，則可以使用與影像圖層中的影像相同的規則來裁切和縮放遮色片。 `size=`， `scale=`，或 `res=` 可用來縮放遮色片。

圖層遮色片也可以以下列形式指定 *`nestedRequest`*. 巢狀或內嵌請求會以大括弧括住。 為內嵌影像伺服請求加上前置詞 `is` 以及內嵌影像演算請求，具有 `ir`. 如果未指定前置詞，則會假設對外來伺服器的要求。 請參閱 [請求巢狀內嵌與內嵌](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) 以取得詳細資訊。

## 屬性 {#section-a093043dc249423b8ae322cefb0d545d}

影像或圖層屬性。 套用至圖層0，如果 `layer=comp`. 被效果圖層忽略。

*`object`* 不得解析為包含 `src=` 或 `mask=` 中的命令 `catalog::Modifier`.

此 `is` 和 `ir` 首碼不區分大小寫。

## 默认 {#section-10cf793c665f49deb1b248faa3b618a9}

若 `mask=` 未明確指定，而且如果圖層影像與目錄專案相關聯，則 `catalog::MaskPath` 已使用。 否則，會使用圖層影像的Alpha色版（如果存在）。 如果沒有Alpha色版，圖層就沒有遮色片，圖層矩形會呈現為完全不透明。

## 示例 {#section-1bbe623f7c744bdf97b596458d8e7ea3}

使用數個個別的遮色片為影像的不同區域著色。 著色的遮色區域會圖層化在原始未修改影像上：

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## 另请参阅 {#section-7ed5201d91594e5f872438a92eaf1c89}

[遮色片使用=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) ， [catalog：：MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)， [物件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) ， [請求巢狀內嵌與內嵌](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
