---
description: JPEG品質。 指定JPEG編碼屬性來控制壓縮等級。 這進而會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 6%

---

# qlt{#qlt}

JPEG品質。 指定JPEG編碼屬性來控制壓縮等級。 這進而會改變檔案大小（回覆資料量），並間接改變結果影像的視覺品質。

` qlt= *`品質`*[, *`色度`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 质量 </span> </p> </td> 
  <td class="stentry"> <p>編碼品質JPEG(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度縮減取樣（0=一般，1=停用）；選擇性，預設為0。 </p> </td> 
 </tr> 
</table>

較高 *`quality`* 值會增加檔案大小和品質，值越低會減少檔案大小並降低感知的影像品質。 如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

設定 *`chroma`* 此旗標可停用典型RGB編碼器所採用的JPEG色度縮減取樣。 當邊緣是由色相變化而不是亮度所定義時，這可能會增加影像中邊緣的感知銳利度。 設定此旗標可能會導致檔案大小稍微增加。 如果文字看起來有點模糊，請嘗試使用此設定。

## 屬性 {#section-925a44cbdc9042db8d4eb149cd073d21}

要求屬性。 無論目前的圖層設定為何，均適用。 如果輸出影像檔案格式不支援JPEG編碼，則忽略。 請參閱 `fmt=` 以取得哪些輸出影像格式支援的資訊 `qlt=`.

*`chroma`* 如果輸出畫素型別為CMYK或灰色，則會被忽略。

## 默认 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 示例 {#section-d7d33871d401433aa51d028823eae7a9}

降低品質，透過低頻寬連線加快傳輸速度：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

提高高頻寬連線的品質：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 另请参阅 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ， [attribute：：JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
