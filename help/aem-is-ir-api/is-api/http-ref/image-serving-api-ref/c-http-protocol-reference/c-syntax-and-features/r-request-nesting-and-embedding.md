---
description: 「影像伺服」支援對「影像伺服」請求進行無限巢狀內嵌、內嵌影像演算請求，以及內嵌從外部伺服器擷取的影像。 只有圖層影像和圖層遮色片支援這些機制。
solution: Experience Manager
title: 請求巢狀內嵌與內嵌
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# 請求巢狀內嵌與內嵌{#request-nesting-and-embedding}

「影像伺服」支援對「影像伺服」請求進行無限巢狀內嵌、內嵌影像演算請求，以及內嵌從外部伺服器擷取的影像。 只有圖層影像和圖層遮色片支援這些機制。

>[!NOTE]
>
>某些電子郵件使用者端和Proxy伺服器可能會為用於巢狀和內嵌語法的大括弧進行編碼。 有問題的應用程式應使用括弧，而非大括弧。

## 巢狀影像伺服請求 {#section-6954202119e0466f8ff27c79f4f039c8}

您可以在「 」中指定整個「影像伺服」請求，以作為圖層來源 `src=` (或 `mask=`)命令，語法如下：

`…&src=is( nestedRequest)&…`

此 `is` Token區分大小寫。

巢狀要求不可包含伺服器根路徑(通常是 ` http:// *[!DNL server]*/is/image/'`)。

>[!NOTE]
>
>巢狀請求分隔符號字元( `'(',')'`)和命令分隔符號字元( `'?'`， `'&'`， `'='`)不可以HTTP編碼。 實際上，巢狀要求的編碼必須與外部（巢狀）要求相同。

預先處理規則會套用至巢狀請求。

在巢狀請求中指定時(在請求URL中或在 `catalog::Modifier` 或 `catalog::PostModifier`)：

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

如果巢狀請求的結果影像包含遮色片(alpha)資料，則會將其傳遞至內嵌圖層，作為圖層遮色片。

同樣被忽略的是 `attribute::MaxPix`和 `attribute::DefaultPix` 套用至巢狀請求的影像目錄的。

可選擇快取巢狀IS要求的影像結果，方法是包含 `cache=on`. 依預設，會停用中繼資料的快取。 只有在預期中繼影像會在合理時段內於不同請求中重複使用時，才應啟用快取。 標準伺服器端快取管理適用。 資料會以無損格式快取。

## 內嵌影像演算請求 {#section-69c5548db930412b9b90d9b2951a6969}

在伺服器上啟用Dynamic Media影像演算後，您可以在src= （或mask=）命令中指定演算請求，以將其作為圖層來源使用。 使用下列語法：

` …&src=ir( *[!DNL renderRequest]*)&…`

此 `ir` Token區分大小寫。

*[!DNL renderRequest]* 是常見的影像演算要求，不包括HTTP根路徑 ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>巢狀請求分隔符號字元( `'(',')'`)和命令分隔符號字元( `'?'`， `'&'`， `'='`)不可以HTTP編碼。 實際上，內嵌請求的編碼必須與外部（內嵌）請求相同。

在巢狀要求中指定時，會忽略下列影像演算命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

同樣被忽略的是 `attribute::MaxPix` 和 `attribute::DefaultPix` 套用至巢狀轉譯器請求的材質目錄的。

可選擇快取巢狀IR要求的影像結果，方法是包含 `cache=on`. 依預設，會停用中繼資料的快取。 只有在預期中繼影像會在合理時段內於不同請求中重複使用時，才應啟用快取。 標準伺服器端快取管理適用。 資料會以無損格式快取。

## 內嵌FXG轉譯器請求 {#section-c817e4b4f7da414ea5a51252ca7e120a}

當FXG圖形轉譯器(亦稱為 [!DNL AGMServer])安裝並啟用影像伺服時，FXG請求可透過在中指定來作為圖層來源 `src=` (或 `mask=`)命令。 使用下列語法：

`…&src=fxg( renderRequest)&…`

此 `fxg` Token區分大小寫。

>[!NOTE]
>
>FXG圖形呈現僅適用於Dynamic Media代管環境，且可能需要額外的授權。 如需詳細資訊，請聯絡Dynamic Media技術支援。

*[!DNL renderRequest]* 是常見的FXG轉譯器要求，不包括HTTP根路徑 ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>分隔符號字元( `'(',')'`)和命令分隔符號字元( `'?'`， `'&'`， `'='`)不可以HTTP編碼。 實際上，內嵌請求的編碼必須與外部（內嵌）請求相同。

在巢狀要求中指定時，會忽略下列FXG命令：

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## 外部影像來源 {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

「影像伺服」支援對外國HTTP伺服器上的來源影像的存取。

>[!NOTE]
>
>遠端URL僅支援HTTP通訊協定。

若要為指定外部URL `src=` 或 `mask=` 命令，請使用括弧分隔外部URL或URL片段：

`…&src=( foreignUrl)&…`

重要分隔符號字元( `'(',')'`)和命令分隔符號字元( `'?'`， `'&'`， `'='`)不可以HTTP編碼。 實際上，內嵌請求的編碼必須與外部（內嵌）請求相同。

完整絕對URL (若 `attribute::AllowDirectUrls` 設定)，以及相對於 `attribute::RootUrl` 允許。 如果內嵌絕對URL且屬性為： `AllowDirectUrls` 為0，或如果已指定相對URL，且 `attribute::RootUrl` 空白。

雖然不能直接在要求URL的路徑元件中指定外部URL，但可以設定預先處理規則，以允許將相對路徑轉換為絕對URL （請參閱以下範例）。

伺服器會根據HTTP回應隨附的快取標頭快取外部影像。 如果兩者都不 `ETag` 不存在Last-Modified HTTP回應標頭，也不會快取回應。 這可能會導致重複存取相同外部影像的效能不佳，因為「影像伺服」在每次存取時都需要重新擷取和重新驗證影像。

此機制支援的影像檔案格式與影像轉換(IC)公用程式支援的格式相同，但每個元件有16位元的來源影像除外。

>[!NOTE]
>
>「影像伺服」會在第一次使用外部影像時自動執行驗證公用程式，以確保影像有效且未在傳輸期間損毀。 這可能會造成首次存取的輕微延遲。 為獲得最佳效能，建議限制這類影像的大小，及/或使用可妥善壓縮的影像檔案格式。

## 限制 {#section-fb68e3f0d40947feb94d7bf183b64929}

巢狀/內嵌請求產生的影像大小通常會自動最佳化。 如果已啟用巢狀要求影像的快取，則透過指定巢狀影像的確切大小可取得遞增的效能增益，如此當重複使用快取專案時，就不需要進一步縮放。

重要影像伺服不支援巢狀或內嵌請求雙重編碼。 巢狀內嵌請求必須像簡單請求一樣進行HTTP編碼。

## 示例 {#section-d800cfc31abe46d2a964f8e7929231f1}

**具有快取的分層範本：**

使用巢狀將快取加入至分層範本。 有限的背景影像上覆蓋有高度可變的文字。 初始範本字串看起來可能像這樣：

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

稍加修改，我們就能預先縮放第0層影像，並持續快取，藉此降低伺服器負載：

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Dynamic Media影像演算的內嵌請求**

使用儲存在中的範本 [!DNL myCatalog/myTemplate]；使用Dynamic Media影像演算為範本的layer2產生影像：

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

請注意巢狀大括弧。 「影像演算」請求會將呼叫內嵌回「影像伺服」，以擷取可重複的紋理。

## 另请参阅 {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [要求預先處理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3)，影像演算參考， [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)， [影像伺服公用程式](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
