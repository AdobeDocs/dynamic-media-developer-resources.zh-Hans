---
description: 使用Dynamic Media影像伺服時，有一些限制和已知問題需要考量。
solution: Experience Manager
title: 限制和已知問題
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# 限制和已知問題{#restrictions-and-known-issues}

使用Dynamic Media影像伺服時，有一些限制和已知問題需要考量。

## 檔案勘誤表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行數不會超過 `\copyfitmaxlines` 設定和文字輸入中的明確行數。
* 影像集中必須搭配大括弧與括弧。 如果大括弧與括弧不相符，則須將URL編碼。
* 伺服器端全域回應時間警報包含錯誤回應。
* 此 `id=` 目前在使用時，需要命令 `rect=` 命令加上影像或遮色片要求。

## 已知差異textPs=與text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 合成斜體呈現的斜體比使用時少 `text=`.
* 底線比使用時稍微低一點且更薄 `text=`.
* `\expnd` 和 `\expndtw` 與高負值一起使用時，會導致字元在使用時彼此排在前 `text=`.

* `\charscaley` 縮放方式與使用時不同 `text=` 但不影響行高。

* 如果文字的最後一行不符合，則會捨棄整行，而不會顯示為截線。
* `\slmult` 和 `\sl` 與MS Word的行為方式不同，而且 `text=`，它們只會對目前和後續段落生效。

* `\sb` 適用於MS Word和的第一段落 `text=`、Adobe InDesign和 [!DNL Photoshop] 請勿這麼做。

* `\sa` 適用於MS Word和的最後一個段落 `text=`、Adobe InDesign和 [!DNL Photoshop] 請勿這麼做。

## 回溯相容性 {#section-a76842f751944f4fb664af296d064122}

* 逸出底線字元( `\_`)無法搭配所有使用的字型使用 `textPs=`

* 支援不區分大小寫的巨集處理。
* 目錄快取已從60秒減少到10秒。
* 錯誤重新導向功能現在只會重新導向參考目錄中已發佈但在磁碟上找不到之損毀影像、字型、色彩設定檔和影像的請求。
* `posN=`， `anchor=`， `anchorN=`， `origin=`、和 `originN=` 現在，如果任何修飾元值大於2147483648，則會傳回剖析錯誤。

* 不支援巢狀要求的編碼。 轉換至新行為，並對在網站上的URL請求和公司目錄中找到的任何巢狀請求值進行取消編碼。
* DefaultImage現在會在使用時套用縮圖屬性 `req=tmb`.
* 在舊版中，使用 `flip=`，無論錨點為何，都不會重新定位影像。

## 適用於協力廠商程式庫的限制 {#section-79768b96bf634e44ab672c5b893f343d}

Digimarc程式庫拒絕將Digimarc浮水印套用至已偵測到的影像。 如果對主要影像進行了足夠的編輯，Digimarc程式庫仍可識別已套用浮水印。 但是，它可能無法讀取該資訊。 這會導致無法取得套用至原始影像的原始Digimarc資訊的新影像。 「影像伺服」現在可以套用公司目錄中定義的Digimarc浮水印。

## 適用於影像提供與影像轉譯的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 超過4個CPU可供使用時，「影像伺服」和「影像演算」可能無法充分利用所有CPU。 在這些電腦上模擬您的流量，以瞭解使用4個以上CPU的優勢。
* 傳回重新導向（HTTP狀態301、302或303）的遠端URL會遭到拒絕。
* 設定時 `errorRedirect.rootUrl` 此屬性中定義的IP位址必須包含在規則集中 `<addressfilter>` 標籤值。

   *示例*:

   伺服器A已定義 `errorRedirect.rootUrl=10.10.10.10` .

   IP位址為10.10.10.10的伺服器B會將 `<addressfilter>` 標籤值，以包含其IP位址(10.10.10.10)。

* 具有定位的點文字和文字路徑可能會顯示剪裁。
* `text=` 僅適用 `\sa` 和 `\sb` 至整個文字區塊，而非每個段落。

* 使用URL中定義的一家公司，以及針對定義的另一家公司時 `src=` 或 `mask=` 修飾元，您必須在為定義的公司加上正斜線作為前置詞 `src=` 或 `mask=` 讓此請求表單運作。

   *示例*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   而非： `/is/image/MyCompany?src=YourCompany/MyImage` .

* 非金字塔Tiff或暈映請求會產生類似的錯誤訊息，並傳送至

   *&quot;影像 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 沒有有效的DSF，且2.25MPixel的面積超過2MPixel的最大值」* .

   最佳實務建議使用金字塔Tiff和暈映。 如果您需要使用非金字塔tifff或暈映，請依照下列指示增加大小限制。

   *解決方法*：

   對於影像演算非金字塔暈映，請將IrMaxNonPyrVignetteSize的屬性值增加到 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 設定檔。

   對於「影像伺服」非金字塔TIFF，請增加 `MaxNonDsfSize` 在 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 設定檔。

* Adobe [!DNL Photoshop] 根據預設，CS3不會儲存圖層PSD檔案為複合影像。

   *症狀*：

   Adobe [!DNL Photoshop] CS3分層PSD檔案顯示為黑色，文字指出：「此分層 [!DNL Photoshop] 檔案未與複合影像一起儲存。」 用於「影像伺服」回覆影像或IPS。

   *解決辦法*︰

   儲存Adobe [!DNL Photoshop] 已啟用最大相容性的CS3檔案。

* 將ICC設定檔指派給CMYK/JPEG回覆影像會導致某些瀏覽器中的顏色反轉。*解決方法*：

   使用變更回覆影像格式 `fmt=`

* 壓縮後HTTP回應影像資料（包括檔案標頭）的大小上限為16 MB。
* 「 ..」 不允許在HTTP要求的任何路徑元素中使用。
* 解除安裝可能會從移除使用者建立或修改的檔案 *[!DNL install_root]* 或任何子資料夾。 在解除安裝之前，請將這類檔案複製到其他位置。

## 僅適用於影像伺服的限制 {#section-b08ad535e4454265b8157dec244c4faf}

* RTF中的前景色彩( `\cf`)命令不支援PhotoFont文字。
* 合成粗體、斜體和粗體/斜體會因為PhotoFont文字的錯誤而被拒絕。
* PhotoFont文字不支援垂直文字排列。
* PhotoFont文字不支援16bpc PNG影像。
* 內嵌色彩設定檔的PNG影像色彩校正使用硬式編碼選項。 「演算色彩比對方式」為相對比色，且已為PhotoFont文字開啟「黑點補償」。
* 在公司中啟用地區設定翻譯時，不支援檔案型查詢 [!DNL ini] 檔案。
* 「影像伺服」不會寫入未關閉的專案 [!DNL Photoshop] 正確路徑。
* 「影像伺服」目前不支援處理使用Adobe Media Encoder 4.0.1或更舊版本匯出的TIFF檔案。 Adobe Media Encoder包含在Premiere ProCS4、After Effects CS4和Creative Suite4 Production Premium中。
* 使用 `text=` 使用自行調整大小的圖層不支援使用多個設定進行行對齊的RTF字串。

   *示例*

   RTF字串不能同時使用左右行對齊來調整文字圖層的大小。

* SVG對於未內嵌在SVG檔案中的參照字型的字型查閱路徑，有其自己的屬性。

   *症狀*

   包含字型定義的演算SVG影像使用不正確的字型。

   *因應措施*

   設定屬性 `svgProvider.fontRoot=` 在 [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* 裁切目前正在使用 `bgColor=` 而非 `color=` 填滿任何新展開的區域。

* 色彩轉換可能不正確，當 `bgColor=` 不符合涉及色彩設定檔的基本色域。
* 如果圖層沒有遮色片或Alpha資料，則不會呈現外層效果。

## 僅適用於影像演算的限制 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 貼花和牆壁材料無法移除。
* 紋理大小相對於暈映檢視的大小是有限的。 在極少數情況下，檢視大小的425%預設限制可能會干擾使用非常大的不可重複紋理的應用程式。 如果無法將應用程式或內容變更為在預先定義的限制內運作，則百分比可以依照以下方式增加。 使用文字編輯器，開啟 [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]，找到 `IrMaxTextureSizeFactor` 並輸入新的百分比值。 此變更會立即生效，而不需重新啟動影像伺服器。

* Netscape和Opera快取回應資料中的JavaScript引擎，即使已設定nocache標頭亦然。 這會干擾有狀態要求的正常運作。

   *因應措施*

   將時間戳記或其他唯一識別碼附加至請求字串，例如 `"&.ts=currentTime`.

## 僅適用於公用程式的限制 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`使用停止時，有時會因分段錯誤而當機 `control-c`.
