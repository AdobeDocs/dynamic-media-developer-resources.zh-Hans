---
title: 互動視訊
description: 互動式視訊檢視器是一種視訊播放器，可播放以H.264格式編碼的串流和漸進式視訊。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2211'
ht-degree: 0%

---

# 互動視訊{#interactive-video}

互動式視訊檢視器是一種視訊播放器，可播放以H.264格式編碼的串流和漸進式視訊。

檢視器也會在視訊內容旁顯示互動式產品色票。 同時支援單一視訊和自我調整視訊集。 專為支援HTML5視訊的桌上型與行動網頁瀏覽器所設計。 檢視器支援在視訊內容、視訊章節導覽和社交分享工具上方顯示的選擇性隱藏式字幕。 此檢視器的用途是協助您實作「可購視訊」體驗。 也就是說，使用者可以選取與特定視訊時區相關聯的色票，並重新導向至客戶網站上的快速檢視或產品詳細資料頁面。

檢視器型別為510。

## 示範URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

和

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## 系统要求 {#section-b7270cc4290043399681dc504f043609}

另請參閱 [系統需求](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 使用互動式視訊檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

互動式視訊檢視器代表主要JavaScript檔案和一組由檢視器在執行階段下載的helper檔案。 單一JavaScript包含在此特定檢視器、資產和CSS使用的所有Viewer SDK元件中。

互動式視訊檢視器可使用透過「影像伺服檢視器」提供的生產就緒HTML頁面，以快顯視窗模式使用。 它也可用於內嵌模式，在此模式下會使用檔案說明的API將其整合到目標網頁中。

設定和外觀設定類似於本指南中說明的其他檢視器。 所有外觀設定都是透過自訂(CSS)階層式樣式表來達成。

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器通用的命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與互動式視訊檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

Interactive Video Viewer提供一組標準的使用者介面控制項來播放視訊，例如「播放/暫停」按鈕、視訊清除程式、視訊時間泡泡、播放時間/總時間指標、音量控制、全熒幕按鈕和隱藏式字幕切換。 所有這些控制項都會分組到直接位於主檢視下的控制項列中。

在觸控裝置上，音量控制會隱藏在使用者介面中，因為只能使用裝置的硬體按鈕來控制音量。

當檢視器在快顯視窗模式下操作時，全熒幕按鈕在使用者介面中不可用。

檢視器會在視訊檢視區域的右側，顯示含有互動式色票的面板。 色票清單會在視訊播放時自動前進，以便顯示與目前視訊區域對應的色票。 在製作期間，按一下或點選色票會觸發與此色票相關聯的動作。 根據您的設定方式，觸發器可能會重新導向至網站上的不同頁面。 或者，它可能會將產品資訊傳回網頁邏輯，進而觸發顯示相關產品內容的Quickview開啟。

當視訊章節啟動時，您可以快速導覽視訊內容。 視訊章節在視訊筆畫壓感追蹤中會顯示為標籤，並在滑鼠指向效果時顯示章節標題和說明（或在觸控系統上點一下滑鼠指向效果時）。 客戶可以按一下章節標籤或點選章節說明泡泡圖，以「搜尋」特定章節。

檢視器也支援各種社群媒體分享工具。 它們可作為使用者介面中的單一按鈕使用，當使用者按一下或點選共用工具列時，該按鈕會展開為共用工具列。 共用工具列包含每個支援的共用管道型別圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟動電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示包含對應資料輸入表單的強制回應對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者從社群媒體服務重新導向至標準共用對話方塊。 此外，當共用工具啟動時，影片播放會自動暫停。 由於網頁瀏覽器安全限制，共用工具無法用於全熒幕模式。

檢視器可使用完整的鍵盤。 另請參閱 [鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 內嵌互動式視訊檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

互動式視訊檢視器內嵌於託管頁面。 這類網頁可能具有靜態版面，也可能是「回應式」的，且在不同裝置或不同瀏覽器視窗大小中顯示的方式不同。

為因應這些需求，檢視器支援兩種主要操作模式：固定大小內嵌和回應式內嵌。

**關於固定大小內嵌模式和回應式設計內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，該網頁可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可依裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此功能是擁有靜態版面之網頁的最佳選擇。

回應式設計內嵌假設檢視器在執行階段需要調整大小來回應其容器的大小變更 `DIV`. 最常見的使用案例是將檢視器新增至使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器的方式而異 `DIV`. 如果網頁僅設定容器的寬度 `DIV`，只要其高度不受限制，檢視器就會根據所使用資產的外觀比例，自動選擇其高度。 此功能可確保資產完全符合檢視要求，而不需在兩側加上任何邊框間距。 此使用案例最常用於使用回應式網頁設計版面架構(例如Bootstrap和Foundation)的網頁。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，檢視器只會填滿該區域，並遵循網頁版面提供的大小。 一個好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗大小調整大小。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器 `DIV`.
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至網頁。

   建立檢視器需要您在HTML標頭中新增指令碼標籤。 在使用檢視器API之前，請務必先包含 [!DNL InterativeVideoViewer.js]. 此 [!DNL InteractiveVideoViewer.js] 檔案位於 [!DNL html5/js/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

如果檢視器部署在某個Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，則可以使用相對路徑。 否則，您需要指定已安裝IS-Viewers的其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>僅參照主要檢視器JavaScript `include` 檔案時。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由檢視器的邏輯在執行階段下載）。 尤其請勿直接參照HTML5 SDK `Utils.js` 檢視器從載入的程式庫 `/s7viewers` 內容路徑（所謂的整合SDK） `include`)。 原因在於 `Utils.js` 或類似的執行階段檢視器程式庫完全由檢視器的邏輯管理，且位置會在檢視器版本之間變更。 Adobe不會保留次要檢視器的舊版本 `includes` 在伺服器上。
>
>
>因此，直接參照任何次要JavaScript `include` 當日後部署新產品版本時，頁面上檢視器使用的檢視器功能會中斷檢視器。

1. 定義容器 `DIV`.

   新增空白 `DIV` 元素至您要顯示檢視器的頁面。 此 `DIV` 元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定的。

   預留位置 `DIV` 是定位元素，這表示 `position` CSS屬性已設定為 `relative` 或 `absolute`.

   若要讓全熒幕功能在Internet Explorer中正常運作，請確定DOM中沒有其他元素的棧疊順序高於預留位置 `DIV`.

   以下是已定義預留位置的範例 `DIV` 元素：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以宣告檢視器的靜態大小，將它設為 `.s7interactivevideoviewer` 以絕對單位表示的頂層CSS類別，或是使用 `stagesize` 修飾元。

   您可以直接在HTML頁面上放入CSS的大小調整。 或者，您也可以將其放在自訂檢視器CSS檔案中，稍後再將該檔案指派給Adobe Experience Manager Assets中的檢視器預設集記錄（隨選），或明確使用以下專案傳遞： `style` 命令。

   另請參閱 [自訂互動式視訊檢視器](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 以取得有關使用CSS設定檢視器樣式的詳細資訊。

   以下是在「HTML」頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   您可以設定 `stagesize` Experience Manager Assets檢視器預設集記錄中的修飾元 — 隨選。 或者，您可以使用檢視器初始化程式碼明確傳遞 `params` 集合，或作為API呼叫，如命令參考區段中所述，如下所示：

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   建議使用以CSS為基礎的方法，並用於此範例。

1. 建立和初始化檢視器。

   完成上述步驟後，您會建立 `s7viewers.InteractiveVideoViewer` 類別，將所有設定資訊傳遞至其建構函式，並呼叫 `init()` 檢視器例項的方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應具有 `containerId` 包含檢視器容器ID名稱且以巢狀顯示的欄位 `params` 具有檢視器支援之設定引數的JSON物件。

   在此案例中， `params` 物件至少必須將影像伺服URL傳遞為 `serverUrl` 屬性，並將初始資產設為 `asset` 引數。 JSON型初始化API可讓您透過以下傳遞的一行程式碼、視訊伺服器URL建立及啟動檢視器： `videoserverurl` 屬性，初始資產為 `asset` 引數，以及互動式資料作為 `interactivedata` 屬性。 JSON型初始化API可讓您使用單行程式碼建立及啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾。 如需最大相容性，請呼叫 `init()` 方法（在結尾之前） `BODY` 標籤或內文 `onload()` 事件。

   同時，容器元素未必是網頁版面配置的一部分。 例如，它可能會使用以下專案隱藏： `display:none` 樣式已指派給它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 之後，檢視器會自動繼續載入。

   以下範例說明如何建立檢視器例項、將最低必要的設定選項傳遞至建構函式，並呼叫 `init()` 方法。 此範例假設以下情況：

   * 檢視器例項為 `interactiveVideoViewer`.
   * 預留位置名稱 `DIV` 是 `s7viewer`.
   * 影像伺服URL為 `https://aodmarketingna.assetsadobe.com/is/image/`.
   * 視訊伺服器URL為 `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * 內容URL `https://aodmarketingna.assetsadobe.com/`.
   * 資產是 `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * 互動式資料為 `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   下列程式碼為將互動式視訊檢視器嵌入固定大小的簡單網頁的完整範例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高度不受限制的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，可指定檢視器容器的執行階段大小 `DIV`. 對於以下範例，假設網頁允許檢視器的容器 `DIV` 以取得網頁瀏覽器視窗大小的40%，其高度不受限制。 網頁HTML程式碼如下所示：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

將檢視器新增至這類頁面，類似於固定大小內嵌的步驟。 唯一的區別是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟與固定大小內嵌的步驟相同。 將容器DIV新增至現有 `"holder"` DIV. 下列程式碼為完整範例。 請注意瀏覽器調整大小時檢視器大小的變化，以及檢視器外觀比例與資產相符的方式。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下範例頁面說明高度不受限制的回應式設計內嵌在實際應用中的更多情況：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[替代示範位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定義寬度和高度的回應式內嵌**

如果有已定義寬度和高度的回應式內嵌，則網頁樣式會不同。 它提供兩種大小給 `"holder"` 在瀏覽器視窗中進行DIV和置中。 此外，網頁會設定 `HTML` 和 `BODY` 元素至100%。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

其餘的內嵌步驟與高度不受限制的回應式內嵌所使用的步驟相同。 產生的範例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用Setter型API內嵌**

您可以使用setter型API和no-args建構函式，而不使用JSON型初始化。 使用此API建構函式不接受任何引數，而且設定引數是透過以下方式指定的： `setContainerId()`， `setParam()`、和 `setAsset()` 具有個別JavaScript呼叫的API方法。

下列範例說明如何將固定大小內嵌與setter型API搭配使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```
