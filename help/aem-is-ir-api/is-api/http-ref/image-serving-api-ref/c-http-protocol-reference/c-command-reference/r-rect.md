---
description: 最終檢視矩形。 可將最終檢視影像拆解成數個區塊或圖磚，這些區塊或圖磚可單獨提供，並由使用者端無縫重組，邊緣不會產生任何不自然感。
solution: Experience Manager
title: 矩形
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 1%

---

# 矩形{#rect}

最終檢視矩形。 可將最終檢視影像拆解成數個區塊或圖磚，這些區塊或圖磚可單獨提供，並由使用者端無縫重組，邊緣不會產生任何不自然感。

`rect= *`座標`*, *`大小`*[, *`縮放`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 座標</span> </p> </td> 
  <td class="stentry"> <p>從檢視影像左上角到檢視矩形(int， int)左上角的畫素位移（以畫素表示），在後方 <span class="varname"> 縮放</span> 「 」已套用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小（以畫素為單位，例如int、int）。 指定回覆影像大小。 影像已填滿 <span class="codeph"> bgc=</span> 在檢視影像未覆蓋的區域中(或如果是 <span class="codeph"> fmt=*-alpha</span> 存在於請求中)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>縮放因數（實數）。 小於1.0的值會降低解析度，大於1.0的值會提高解析度。 </p></td> 
 </tr> 
</table>

使用此命令，「影像伺服」可以透過HTTP傳送大型影像，否則會超過設定的大小限制 `attribute::MaxPix`.

>[!NOTE]
>
>為達到使用JPEG壓縮的最佳效果，條紋或並排大小應為JPEG編碼並排大小（16x16畫素）的倍數。

## 示例 {#section-932fcfcb41d74a29bc929e4430c49601}

將可列印的CMYK影像分割成數個全解析度分段以減少下載檔案大小。 如果我們要請求連續影像：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

首先，取得影像的相關資訊：

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

文字回應包含下列屬性：

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

根據此資訊，我們決定想要四條600x2000畫素的色條。 此 `rect=` 指令用於描述分段大小和位置。

由於此影像經常變更，因此我們將包含 `id=` 指令來儘量減少我們在CDN或Proxy伺服器中快取的舊版影像中，出現一或多個分割的可能性。 的值 `image.version` 屬性會用於此目的。

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## 屬性 {#section-aae223cee13e46d38b74680c048d945b}

檢視屬性。 無論目前的圖層設定為何，均適用。

任何延伸至檢視影像外部的ROI區域皆以填補 `bgc=`.

重要 `rect=` 已套用 *晚於* 最終縮放與彎管頭 `scl=`， `wid=`， `hei=`， `fit=`， `rgn=`、和 `align=`.

## 默认 {#section-b296d3bbfb19441f87137a452b70f19a}

完整、未修改的檢視影像( `rect=0,0,width,height,1.0`)。

## 另请参阅 {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)， [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)， [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)， [attribute：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)， [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
