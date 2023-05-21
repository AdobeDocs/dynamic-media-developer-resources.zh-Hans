---
description: 「影像伺服」支援可縮放的向量圖形(SVG)檔案作為來源資料。 必須符合SVG1.1。
solution: Experience Manager
title: SVG支援
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# SVG支援{#svg-support}

「影像伺服」支援可縮放的向量圖形(SVG)檔案作為來源資料。 必須符合SVG1.1。

「影像伺服」只會辨識靜態SVG內容，不支援動畫、指令碼和其他互動式內容。

可以在允許影像檔案的地方指定SVG(URL路徑、 `src=`、和 `mask=`)。 點陣化SVG檔案的內容後，其處理方式與影像相同。

與影像類似，SVG檔案也可以指定為影像目錄專案或相對檔案路徑。

## 替代變數 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 替代變數可包含在值字串的SVG檔案中 `<text>` 元素和任何元素屬性。

內嵌影像伺服請求的查詢部分的重要變數不會直接被取代。 而是將所有可用的變數定義附加至請求，讓「影像伺服」可在剖析請求時取代變數。

另請參閱 [替代變數](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) 以取得其他資訊。

## 影像參考 {#section-a7680f9e6aca4b1a83560637cc9fac66}

可以使用將影像插入SVG `<image>` 元素。 由參照的影像 `xlink::href` 的屬性 `<image>` 元素必須是有效的影像伺服請求。 不允許外部URL。

指定完整的「影像伺服」請求，從 `http://`或相對url，開頭為 `/is/image`. 如果指定完整的HTTP路徑，則會從路徑中移除網域名稱，以轉換為相對格式。 使用完整HTTP路徑可能有所助益，因為此路徑可讓協力廠商SVG轉譯器預覽檔案。

>[!NOTE]
>
>在這個版本的「影像伺服」中，對轉譯影像的支援有限。 只有在傳統「影像伺服」分層和範本化機制不足以達成所要的結果時，才應使用從SVG內參照影像。 在任何情況下都不應使用SVG來產生多影像合成。

>[!NOTE]
>
>SVG中內嵌的影像目前不會自動調整大小。 請確定所有影像href都包含必要的「影像伺服」命令，以設定所需的影像大小(例如 `wid=`)。 如果未明確設定影像大小， `attribute::DefaultPix` 「 」已套用。

## 色彩管理 {#section-ea76e2bc4e1842638aa97a2d470c8a68}

所有內嵌在SVG檔案中，並透過替代變數傳遞至SVG範本的顏色值，都會被假設為存在於 `sRgb` 色域。

將影像內嵌至SVG時，不會執行任何色彩轉換。 若要確保色彩保真度，請務必指定 `icc=sRgb` 用於所有內嵌影像要求。

點陣化之後，SVG影像會像其他影像一樣參與色彩管理。

## 示例 {#section-036cdd45abd449849ee00a8f21788c28}

下列SVG範本說明影像參照和變數的使用。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

此SVG範本的使用方式如下：

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 限制 {#section-daa5eccd07204aaf993be41e87822d54}

SVG檔案必須是獨立檔案，不得參考任何次要檔案或資源，但影像伺服或影像演算請求（請參閱上文）所參考的外部影像除外。

只會呈現靜態內容。 動畫、互動功能（例如按鈕）等。 可能存在，但可能不會如預期般呈現。

目前不支援ICC設定檔色彩規格。

`<script>` 元素可能存在，但一律會忽略。

## 另请参阅 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [SVG1.1規格](https://www.w3.org/TR/SVG11/)
