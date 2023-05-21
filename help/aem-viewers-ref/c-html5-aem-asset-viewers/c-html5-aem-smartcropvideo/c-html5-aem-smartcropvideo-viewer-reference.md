---
title: 智慧型裁切視訊檢視器
description: 智慧型裁切視訊檢視器可播放以H.264格式編碼的串流及漸進式視訊，並額外支援智慧型裁切。 它是從Dynamic Media Classic或Adobe Experience Manager透過Dynamic Media提供。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
source-git-commit: 96504ebdc86ff81e9ce69e2d708ede1d0a88d9b5
workflow-type: tm+mt
source-wordcount: '2403'
ht-degree: 0%

---

# 智慧型裁切視訊{#smart-crop-video}

智慧型裁切視訊檢視器可播放以H.264格式編碼的串流及漸進式視訊，並額外支援智慧型裁切。 它是從Dynamic Media Classic或使用Dynamic Media的Experience Manager提供。

另請參閱 [系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

同時支援單一視訊和自我調整視訊集。 此外，檢視器支援使用託管於外部位置的漸進式視訊和HLS資料流。 專為支援HTML5視訊的桌上型與行動網頁瀏覽器所設計。 此檢視器也支援在視訊內容、視訊章節導覽和社群媒體分享工具上方顯示的選擇性隱藏式字幕。

只要基礎系統支援，「智慧型裁切視訊檢視器」就會在其預設設定中使用HLS格式的HTML5串流視訊播放。 在不支援HTML5串流的系統上，檢視器會回到HTML5漸進式視訊傳送。

檢視器型別518。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## 使用智慧型裁切視訊檢視器 {#section-f21ac23d3f6449ad9765588d69584772}

智慧型裁切視訊檢視器代表主要JavaScript檔案和一組協助程式檔案。單一JavaScript包含此特定檢視器使用的所有Viewer SDK元件、資產，以及檢視器在執行階段下載的CSS。

您可以使用透過IS-Viewers提供的生產就緒HTML頁面，在快顯視窗模式中使用智慧型裁切視訊檢視器。 或者，您也可以在內嵌模式下使用檢視器，也就是使用記錄的API將其整合到目標網頁中。

設定檢視器及設定檢視器外觀的任務與其他檢視器類似。 所有外觀設定都是透過自訂CSS來達成。

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器通用的命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與智慧型裁切視訊檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

智慧型裁切視訊檢視器提供一組用於視訊播放的標準使用者介面控制項，例如：

* 播放/暫停按鈕。
* 視訊筆畫壓感視訊時間泡泡。
* 播放時間/總時間指標。
* 音量控制。
* 全熒幕按鈕。
* 隱藏式字幕切換。

所有這些控制項都會分組到檢視器使用者介面底部的控制項列中。

在觸控裝置上，音量控制會隱藏在使用者介面中，因為只能使用硬體按鈕來控制音量。

當檢視器在快顯視窗模式下操作時，全熒幕按鈕在使用者介面中不可用。

當視訊章節啟動時，您可以快速導覽視訊內容。 視訊章節會在視訊筆畫壓感追蹤中顯示為標籤，並在滑鼠滑鼠指向效果上或點一下觸控系統時，顯示章節標題和相關說明。 使用者可以選取章節標籤或選取章節說明泡泡來搜尋特定章節。

檢視器支援觸控式輸入和滑鼠輸入，適用於Windows裝置上的觸控式熒幕和滑鼠。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可使用完整的鍵盤。

另請參閱 [鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 使用智慧型裁切視訊檢視器的社群媒體分享工具 {#section-907d316fe1da4b87abb9775f02464704}

智慧型裁切視訊檢視器支援社群媒體分享工具。 它們可作為使用者介面中的單一按鈕使用，當使用者按一下或點選共用工具列時，該按鈕會展開為共用工具列。

共用工具列包含每個支援共用管道型別的圖示，例如Facebook、Twitter、電子郵件共用、內嵌程式碼共用和連結共用。 啟動電子郵件共用、內嵌共用或連結共用工具時，檢視器會顯示包含對應資料輸入表單的強制回應對話方塊。 呼叫Facebook或Twitter時，檢視器會將使用者從社群媒體服務重新導向至標準共用對話方塊。 當共用工具啟動時，也會自動暫停視訊播放。

由於網頁瀏覽器安全限制，共用工具無法用於全熒幕模式。

## 內嵌智慧型裁切視訊檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 有時，網頁會提供連結，在選取時會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，必須直接將檢視器內嵌在託管頁面上。 在後一種情況下，網頁可能具有靜態頁面佈局，或使用回應式設計，在不同裝置或不同瀏覽器視窗大小上顯示不同。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

平板電腦和行動裝置支援在同一頁面上內嵌多個影片。 通常一次只能播放一個視訊。 當使用者開始播放一個影片，然後嘗試播放另一個影片時，會自動暫停第一個影片。 已自動暫停的視訊會記住其目前的播放時間，因此使用者可以隨時返回視訊並繼續播放。 此規則的唯一例外是Android™ 4.x裝置上的Chrome瀏覽器，該瀏覽器可同時播放視訊。

**關於彈出式模式**

在快顯視窗模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式最常用於行動裝置。 網頁會使用載入檢視器 `window.open()` JavaScript呼叫，已正確設定 `A` HTML元素或任何其他合適的方法。

建議您使用現成的HTML頁面作為快顯視窗操作模式。 其名稱為 [!DNL SmartCropVideoViewer.html] 而且它位於 [!DNL html5/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

您可以套用自訂CSS來實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**關於固定大小嵌入模式和回應式嵌入模式**

在內嵌模式中，檢視器會新增至現有網頁，該網頁可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可依裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此選項最適合使用具有靜態頁面配置的網頁。

回應式設計內嵌假設檢視器必須在執行階段調整大小來回應其容器的大小變更 `DIV`. 最常見的使用案例是將檢視器新增至使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器的方式而異 `DIV`. 如果網頁僅設定容器的寬度 `DIV`，只要其高度不受限制，檢視器就會根據所使用資產的外觀比例，自動選擇其高度。 此方法可確保資產完全符合檢視，而不會在兩側加上任何邊框間距。 此使用案例最常用於使用回應式設計版面架構(例如Bootstrap或Foundation)的網頁。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，檢視器會填滿該區域，並遵循網頁版面配置所提供的大小。 一個好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗的大小而調整大小。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器 `DIV`.
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至網頁。

   建立檢視器需要您在HTML標頭中新增指令碼標籤。 在使用檢視器API之前，請務必先包含 [!DNL SmartCropVideoViewer.js]. 此 [!DNL SmartCropVideoViewer.js] 檔案位於 [!DNL html5/js/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

如果檢視器部署在某個Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，則可以使用相對路徑。 否則，您需要指定已安裝IS-Viewers的其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
```

>[!NOTE]
>
>僅參照主要檢視器JavaScript `include` 檔案時。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由檢視器的邏輯在執行階段下載）。 尤其請勿直接參照HTML5 SDK `Utils.js` 檢視器從載入的程式庫 `/s7viewers` 內容路徑（所謂的整合SDK） `include`)。 原因在於 `Utils.js` 或類似的執行階段檢視器程式庫完全由檢視器的邏輯管理，且位置會在檢視器版本之間變更。 Adobe不會保留次要檢視器的舊版本 `includes` 在伺服器上。
>
>
>因此，直接參照任何次要JavaScript `include` 當日後部署新產品版本時，頁面上檢視器使用的檢視器功能會中斷檢視器。

1. 定義容器DIV。

   新增空的DIV元素至您要檢視器出現的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。 DIV的大小是透過CSS指定的。

   預留位置DIV是定位元素，這表示 `position` CSS屬性已設定為 `relative` 或 `absolute`.

   請確定Internet Explorer中的全熒幕功能正常運作。 確認DOM中沒有其他元素的棧疊順序高於預留位置DIV。

   以下是已定義預留位置DIV元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. 設定檢視器大小

   您可以宣告檢視器的靜態大小，將它設為 `.s7videoviewer` 以絕對單位或修飾元表示的頂層CSS類別 `stagesize`.

   您可以在HTML頁面或自訂檢視器CSS檔案中置入CSS大小。 它稍後會指派給Dynamic Media Classic中的檢視器預設集記錄，或是使用樣式命令明確傳遞。

   另請參閱 [自訂智慧型裁切視訊檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) 以取得使用CSS設定檢視器樣式的詳細資訊。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以設定 `stagesize` 修飾元(在Dynamic Media Classic的檢視器預設集記錄中)，或透過檢視器初始化程式碼明確傳遞 `params` 集合。 或者，如命令參考一節中所述，以API呼叫形式執行，如下所示：

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   建議使用以CSS為基礎的方法，並用於此範例。

1. 建立和初始化檢視器。

   完成上述步驟後，您會建立 `s7viewers.SmartCropVideoViewer` 類別，將所有設定資訊傳遞至其建構函式，並呼叫 `init()` 檢視器例項的方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應具有 `containerId` 包含檢視器容器ID名稱且以巢狀顯示的欄位 `params` 具有檢視器支援之設定引數的JSON物件。 在這種情況下， `params` 物件至少必須將影像伺服URL傳遞為 `serverUrl` 屬性，視訊伺服器URL傳遞為 `videoserverurl` 屬性，並將初始資產設為 `asset` 引數。 JSON型初始化API可讓您使用一行程式碼建立及啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾。 如需最大相容性，請呼叫 `init()` 方法（在結尾之前） `BODY` 標籤或內文 `onload()` 事件。

   同時，容器元素不一定會成為網頁版面的一部分。 例如，它可能會使用以下專案隱藏： `display:none` 樣式已指派給它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

   以下範例說明如何建立檢視器例項、將最低必要的設定選項傳遞至建構函式，以及呼叫 `init()` 方法。 此範例假設 `smartCropVideoViewer` 是檢視器例項， `s7viewer` 是預留位置的名稱 `DIV`， [!DNL http://s7d1.scene7.com/is/image/] 是影像伺服URL， [!DNL http://s7d1.scene7.com/is/content/] 是視訊伺服器URL，以及 [!DNL html5automation/frisbee-AVS] 是資產。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   下列程式碼是嵌入固定大小智慧型裁切視訊檢視器的簡單網頁的完整範例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高度不受限制的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，可指定檢視器容器的執行階段大小 `DIV`. 在此範例中，假設網頁允許檢視器的容器 `DIV` 以取得網頁瀏覽器視窗大小的40%，其高度不受限制。 網頁HTML程式碼如下所示：

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

將檢視器新增至這類頁面類似於內嵌固定大小；唯一的差異是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟與固定大小內嵌的步驟相同。 新增容器 `DIV` 至現有的「持有者」 `DIV`. 下列程式碼為完整範例。 您可以檢視瀏覽器調整大小時檢視器大小的變化情況，以及檢視器外觀比例與資產相符的方式。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

以下範例頁面說明高度不受限制的回應式設計嵌入在現實生活中的更多用法：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[替代示範位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定義寬度和高度的回應式設計內嵌**

如果有定義寬度和高度的回應式設計內嵌，則網頁樣式會不同；它會同時提供兩種大小給「托架」 `DIV` 並將其置中於瀏覽器視窗中。 此外，網頁會設定 `HTML` 和 `BODY` 元素至100%：

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

其餘的內嵌步驟與高度不受限制的回應式設計內嵌相同。 產生的範例如下：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**使用Setter型API內嵌**

您可以使用setter型API和no-args建構函式，而不使用JSON型初始化。 使用該API，建構函式不會接受任何引數，而且會使用下列專案指定設定引數： `setContainerId()`， `setParam()`、和 `setAsset()` 具有個別JavaScript呼叫的API方法。

以下範例說明使用setter型API嵌入固定大小內容：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
