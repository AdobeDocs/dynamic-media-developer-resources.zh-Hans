---
title: Scene7 2016年秋季版
description: 「Adobe Scene7 2016年秋季版的最新發行說明，屬於Adobe Experience Cloud中Adobe Experience Manager解決方案的一部分。」
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '2209'
ht-degree: 0%

---

# Scene7 2016年秋季版{#scene-fall-release}

Adobe Scene7 2016年秋季版的最新發行說明 — Adobe Experience Cloud中Adobe Experience Manager解決方案的一部分。

## Scene7 2016年秋季版 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

的最新版本注意事項 [!DNL Adobe Scene7] 2016年秋季版 —  [!DNL Adobe Experience Manager] 中的解決方案 [!DNL Adobe Experience Cloud].

* [常规](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [场景 7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [檢視器（影像伺服5.5.3）](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [檢視器（影像伺服5.5.2）](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [檢視器（影像伺服5.5.1）](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5檢視器SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic影像提供6.3.2和影像轉譯6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 常规 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe很高興宣佈推出HTTP/2內容傳送，並擁有提升效能的整體優點。

另請參閱 [HTTP2傳送內容常見問答](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

如需完整檔案，請參閱 [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**新功能、增強功能和錯誤修正**

* 移除的視訊重新剪輯功能 [!DNL Adobe Scene7 Publishing System] 使用者介面。
* 在必要和可能的情況下，新增驗證至所有Scene7 servlet
* 垃圾桶中涉及清單檢視的錯誤修正。
* 已移除 **建立Dynamic Media Classic (Scene7)管理員** 基於安全性考量，從「使用者管理」取得使用者功能。
* FTP WebAdmin現在支援OKTA驗證。
* 移除為新Media Portal使用者建立的預設密碼功能。
* 涉及新增使用者時產生的暫時密碼的錯誤修正。 密碼不符合必要的密碼要求。
* 已解決WebAdmin根磁碟已滿的問題。
* 使用者介面中不會立即反映停用使用者的錯誤修正。
* 有關刪除使用者的錯誤修正，但您稍後無法重新建立使用者。
* 錯誤修正：傳送給新Scene7使用者的歡迎電子郵件未包含驗證以控制特定設定。
* 若任何檔案夾名稱中包含特殊字元，則修復無法擷取FTP檔案夾清單的錯誤。
* 設定Scene7環境的OKTA服務提供者。
* 新增對Viewer Analytics的Experience Cloud組織ID的支援。
* 實作Scene7 SAML消費者。

## 檢視器（影像伺服5.5.3） {#section-1d59bcd5825d487b80b59a6d1a08ed30}

如需完整檔案，請參閱 [檢視器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**影像伺服5.5.3的錯誤修正**

* 與RequireJS和DOJO程式庫的相容性。

   在檢視器部署期間整合的SDK JS快取。

## 檢視器（影像伺服5.5.2） {#section-9932c988cfee45749594af481dfc6476}

如需完整檔案，請參閱 [檢視器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**影像伺服5.5.2的錯誤修正**

* 無法在Windows 7上的Internet Explorer 11中播放視訊。
* `initialframe` 不會影響HTML5 eCatalog行動裝置上的縱向模式。

## 檢視器（影像伺服5.5.1） {#section-833ab92c91c941d2bfdc27f233f582ad}

如需完整檔案，請參閱 [檢視器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**影像伺服5.5.1的新功能、增強功能和錯誤修正**

* HTML5具有搜尋功能的eCatalog檢視器。
* 新增HLS串流視訊播放，作為大部分案頭系統的預設視訊傳送方法。 Flash式HDS視訊串流仍可作為替代播放選項。
* 新增對具有執行Chrome瀏覽器的滑鼠和觸控輸入裝置的支援。
* 將Experience Cloud組織ID支援新增至Analytics整合。
* 將AppMeasurement JavaScript程式庫更新至1.6.1版。
* 在eCatalog檢視器中新增從右至左方向的支援。
* 已修正以下問題： `tip=0,-1,0` 造成超出範圍的錯誤。

**相容性說明**

* BlackBerry®

   * 與舊版AVS集不相容。 使用者端必須重新上傳AVS集才能允許播放。

* 常规

   * 瀏覽器端縮放可能會造成使用者放大至頁面時，UI和影像變得模糊。 視縮放而定，UI格式也可能顯示不正確。 此效果會延續至全熒幕。
   * 由於行動裝置上的大小限制，混合媒體檢視器會使用滑動手勢來交換內嵌影像集中的影格，而非點選內嵌色票元件。 元件會以視覺指示器的形式存在。
   * 在Internet Explorer瀏覽器和某些觸控裝置中，全熒幕模式不會佔據整個裝置熒幕。 而是將應用程式的大小調整為瀏覽器視窗的大小。
   * 「關閉」按鈕在iOS 8.0和8.1中無法運作，但在iOS 8.2中不再出現

* Galaxy SIII

   * 使用Zoom和eCatalogHTML5檢視器時發現記憶體流失。 重複瀏覽畫面可能會造成瀏覽器當機。
   * 在檢視器上點兩下可能會導致整個頁面縮放，而不僅僅是啟用瀏覽器端縮放的檢視器。

* Galaxy S4

   * 在直向模式中偵測到裝置為平板電腦，且瀏覽器設定中勾選全熒幕。

* Galaxy Nexus

   * 在檢視器上點兩下可能會導致整個頁面縮放，而不僅僅是啟用瀏覽器端縮放的檢視器。

* Galaxy Nexus 10和Galaxy平板電腦

   * eCatalog顯示不正確的頁面跨頁，具有直向和橫向方向。

* HTC行動裝置

   * HTC行動裝置Adobe的調查結果顯示，無法停用原生縮放，這是HTC UI包裝函式(HTC Sense)的「功能」。 在檢視器上使用「捏合縮放」手勢時，此問題可能會導致整個頁面縮放。 建議改用點兩下。
   * 如果影像地圖很小且很接近，則影像地圖圖示可能會重疊。

* HTML5影片

   * Internet Explorer 9：不顯示自訂海報影像。
   * `IntialBitRate` 修飾元僅支援軟體HLS和FlashHDS播放。 使用原生播放器播放時無法運作。
   * 目前不支援OGG和WebM漸進式播放。
   * 瀏覽器縮放可能會導致視訊播放器以不正確的大小顯示（包括Windows作業系統控制面板顯示設定）。
   * 在Safari上使用HLS串流的視訊搜尋可能不一致。

* Internet Explorer

   * 目前不支援Quirks模式。
   * 目前不支援相容模式。
   * 目前不支援行動裝置上的Internet Explorer。

* iOS

   * 大型的eCatalog可能會導致iPad 2上的瀏覽器當機。
   * 檢視器偵測到iPhone 6+手機為平板電腦。

* Safari

   * Safari 6.1或更新版本：網際網路外掛程式設定可能會導致Flash影片無法播放。
   * 在Safari上使用HLS串流的視訊「搜尋」可能不一致。
   * 無法使用HLS串流在Safari 6上搜尋視訊結尾。

**已知問題和限制**

* 影像伺服修飾元來自 `iscommands` 不會新增至 `req=set` 依設計要求。 只影響影像顯示的修飾元可以正常運作。 影響大小的修飾元必須用於複雜資產。 例如︰

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [彈出] 滑鼠關閉後，IE9有時仍會留在熒幕上。
* 瀏覽器縮放會導致重新調整大小錯誤。
* iPad 2：iOS上的大型eCatalog資產導致Safari當機。
* 所有檢視器

   * 不支援浮水印、模糊化及鎖定。
   * 不支援影像預設集。
   * 使用在DOM中新增或移除檢視器 `display:none` 目前不支援CSS或透過將其從父節點動態分離的方式來建立。

* HTML5所有檢視器

   * 將檢視器內嵌在表格中，可能會導致檢視器大小或位置不正確，無法置於非原生全熒幕模式。 建議改用DIV。
   * 程式碼中具有明確執行個體名稱的引數需要URL中的執行個體名稱也被覆寫(例如， `zoomView.iconfeffect=0`)。
   * 目前不支援「影像伺服」命令裁切。
   * 只有在子視窗中開啟檢視器時，「關閉」按鈕才有效。
   * 此 `iscommands` 修飾元不支援影響影像大小的「影像伺服」修飾元。

* HTML5 eCatalog

   * 導覽至其他HTML頁面並偶爾回訪，會導致檢視器重設回第一頁。
   * 旋轉iOS裝置後，頁面配置偶爾會顯示不正確。 放大至頁面可更正版面。
   * 僅連至多頁跨頁中最左側頁面的內部連結。 影響直向模式中的行動裝置。
   * InitialFrame僅連結至多頁跨頁中最左邊的頁面。 影響直向模式中的行動裝置。
   * 由於瀏覽器限制，IE9中無法使用列印功能。

* HTML5 MixedMedia

   * 不支援音軌播放。

* HTML5社交

   * 若要正確呈現傳出電子郵件中的縮圖，請 `serverurl` 修飾元必須具有絕對URL。

* HTML5影片

   * 海報影像可能發生「大小上限」錯誤。 公司必須增加「影像伺服發佈」的限制。
   * 如果從外部伺服器(而不是Scene7伺服器)提供託管HTML頁面，則視訊字幕需要公司規則集。 請聯絡Adobe支援以尋求協助。
   * 由於緩衝，Analytics追蹤可能會報告不正確的播放百分比
   * iPad或Android™裝置上可能會顯示黑色影格而非海報影像。
   * 在iPad或Android™裝置上載入檢視器時，黑色影格可能會在熒幕上閃爍。
   * 當iPad裝置上的背景設定為白色/透明時，VideoPlayer元件的一側會顯示黑色框線。
   * 使用iOS 7時，iPad上的最後一個視訊影格可能會失真。
   * 在Chrome、Firefox和Internet Explorer瀏覽器中，以HLS串流模式搜尋視訊時，可能會偶爾發生巨集封鎖。
      * 首次造訪的訪客可能無法在Microsoft® Edge瀏覽器中顯示海報影像。
      * 使用漸進式播放時，在Internet Explorer 9中載入視訊後，海報影像可能會隱藏。

## Scene7 HTML5檢視器SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

使用手冊位於使用者端安裝的Adobe HTML5 Viewer SDK資料夾中。 在使用者端安裝的檔案子資料夾中找到元件API檔案。

**3.0.2的錯誤修正**

* VideoPlayer — 無法在Windows 7上的Internet Explorer 11中播放視訊。
* 目錄 —   `initialframe` 並未影響HTML5 eCatalog檢視器行動裝置上的縱向模式。

**3.0.1的新功能、增強功能和錯誤修正**

* 常规

   * 新增HLS串流視訊播放，作為大部分案頭系統的預設視訊傳送方法。 Flash式HDS視訊串流仍可作為替代播放選項。
   * 新增SearchManager、SearchPanel、SearchEffect和SearchButton元件，以支援eCatalog檢視器的新搜尋功能。
   * 新增對在Chrome瀏覽器上執行滑鼠和觸控輸入之裝置的支援。
   * 重構Android™版本偵測，以支援未來版本的作業系統。
   * 在eCatalog專屬的SDK元件中新增從右至左方向的支援。

* 控制列

   * 新增選擇性的ControlBar內容捲動，以防其不符合可用寬度。

* FlyoutzoomView

   * 修正案例 `tip=0,-1,0` 造成超出範圍的錯誤。

**相容性說明**

* Android™ 4.x

   * 若要停用預設值，必須為元件新增藍色反白顯示下列CSS規則：

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * 變更AVS集中的位元速率資料流時，視訊播放可能會停止。

* 鉻黃

   * 任何強制元件重建的API呼叫可能會因Chrome的內部快取而遭到忽略。

* Galaxy SIII

   * 檢視器有時無法載入全熒幕。
   * 目前裝置上的Pageview發生記憶體洩漏問題。
   * 當瀏覽器端縮放作用中時，點兩下手勢可縮放檢視器和頁面。

* Galaxy Nexus

   * 某些檢視元件上會顯示成品。
   * 當瀏覽器端縮放作用中時，點兩下手勢可縮放檢視器和頁面。

* IPAD 3

   * iPad 3的原始解析度為2048x1536。 如果公司的IS發佈、影像大小限制設定得較低，此解析度可能會導致顯示問題。

* iPhone4

   * Iconeffect重播圖示已在捲動頁面後取代為播放圖示。

* Internet Explorer

   * 在IE 10和舊版全熒幕模式中，不會佔用整個熒幕，而是根據瀏覽器視窗的大小來調整應用程式的大小。
   * 不支援Quirks演算模式。
   * 目前不支援行動裝置上的Internet Explorer。
   * 如果以非同步方式包含，Util.js可能無法載入。
   * IconEffect圖示會封鎖SpinView和ZoomView元件上的點選事件。

* 原生裝置影片播放程式

   * 使用VideoPlayer呼叫裝置的原生播放器時，不支援透過VideoPlayer來分層UI元件。
   * Safari 6上原生模式的視訊播放不一致。
   * 原生的播放會在捲動頁面後以播放圖示取代重播圖示。

* 觸控裝置

   * 全熒幕模式不會佔據整個裝置熒幕，而只是將應用程式大小調整為符合瀏覽器視窗的大小。
   * 自訂游標不適用於觸控裝置。
   * 目前不支援觸控裝置上的頁面縮放。 內嵌HTML5檢視器需要具備適當設定的檢視區meta標籤。

* Xoom

   * 當瀏覽器端縮放作用中時，點兩下手勢可縮放檢視器和頁面。

**已知問題和限制**

* 所有元件

   * 在2.7.2版和更早版本中，有些元件是使用新增至DOM `insertBefore()` API。 因此，無論元件例項是相對於其他元件建立的，此類元件都會置於棧疊順序的底部。 在2.8.1版中，所有元件都使用 `appendChild()` 現在API，這表示元件棧疊順序會符合執行個體建立的順序。

   * 使用 `iscommand` 不支援用來設定影像alpha色版格式的修飾元。 使用元件 `FMT` 引數。
   * 目前不支援CSS轉換屬性。

* 觸控裝置

   * 觸控裝置上的夾捏手勢不會產生縮放事件

* 容器

   * 不支援容器的邊框、邊框間距和邊界。 Adobe建議將樣式元素新增至父項DIV。
   * 必須明確設定容器大小，否則元件大小可能不正確。

* 列印元件

   * 由於瀏覽器限制，在Internet Explorer 9中，列印元件可能無法正確地縮放紙張上的內容。

* IconEffect元件

   * IconEffect會在Internet Explorer上產生指令碼錯誤，如果 `autohide` 已停用(設定為 `0`)。

* ImageMapEffect元件

   * 在檢視元件上平移影像時，重新定點陣圖示延遲顯示。

* MediaSet元件

   * 內嵌資產要求與URL上相同的編碼。

* NavigationView元件

   * 元件目前不支援調整大小。

* PageScrubber元件

   * 在iPhone 5上，當PageScrubber泡泡設定為文字時，它會在沿著軌道滑動按鈕時顯示成品。 使用 `-webkit-background-clip: content;` 在樣式中可解決此問題。

* SpinView元件

   * 影像旋轉時，SpinView在滑動手勢和旋轉裝置後有時會顯示為凍結。

* 色票元件

   * 選取超出範圍的色票時，會顯示兩個反白專案。
   * 自動捲動 `selectSwatch()` 方法運作不正確。

* videoplayer

   * 如果搜尋設為100%且後援設為auto，則視訊影格不會更新。
   * 在Chrome、Firefox和Internet Explorer瀏覽器中，以HLS串流模式搜尋視訊時，可能會偶爾發生巨集封鎖。
   * 首次造訪的訪客可能無法在Microsoft® Edge瀏覽器中顯示海報影像。
   * 使用漸進式播放時，在Internet Explorer 9中載入視訊後，海報影像可能會隱藏。

## Dynamic Media影像提供6.3.2和影像轉譯6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC公用程式 —  `downsample2x2` 不再支援標幟。 此旗標是品質較差的2x2縮減取樣器，IPS已不再使用。
* CORS標頭 — 目前，CORS標頭設定為 `/is/content/` 要求。
