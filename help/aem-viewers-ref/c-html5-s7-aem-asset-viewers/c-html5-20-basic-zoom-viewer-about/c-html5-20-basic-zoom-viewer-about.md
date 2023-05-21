---
title: 基本縮放
description: 基本縮放檢視器是顯示單一可縮放影像的影像檢視器。 它有縮放工具、全熒幕支援和選用的關閉按鈕。 此檢視器是最輕量級的。 專為桌上型電腦和行動裝置所設計。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ee15ce21-20c4-428b-9512-050115e4c322
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2028'
ht-degree: 0%

---

# 基本縮放{#basic-zoom}

基本縮放檢視器是顯示單一可縮放影像的影像檢視器。 它有縮放工具、全熒幕支援和選用的關閉按鈕。 此檢視器是最輕量級的。 專為桌上型電腦和行動裝置所設計。

>[!NOTE]
>
>此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。

檢視器型別501。

另請參閱 [系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B](https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B)

## 使用基本縮放檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

基本縮放檢視器代表JavaScript檔案和一組協助程式檔案，供檢視器在執行階段下載。 基本上，這是單一JavaScript包含，以及此特定檢視器、資產和CSS使用的所有Viewer SDK元件。

您可以在快顯視窗模式中使用基本縮放檢視器，只要使用隨IS-Viewers提供的生產就緒HTML頁面，或是在內嵌模式中，使用檔案說明的API將其整合至目標網頁。

設定和外觀設定與其他檢視器的設定和外觀設定類似。 所有外觀設定都是透過自訂CSS來達成。

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器通用的命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與基本縮放檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

基本縮放檢視器支援下列其他行動應用程式中常見的觸控手勢。

當檢視器無法處理使用者的撥動手勢時，會將事件轉送給網頁瀏覽器，以執行原生頁面捲動。 即使檢視器佔據裝置的熒幕區域大部分，此類功能仍可讓使用者導覽頁面。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手势 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>點選一次 </p> </td> 
   <td colname="col2"> <p>隱藏或顯示使用者介面元素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>點兩下 </p> </td> 
   <td colname="col2"> <p> 放大一個層級，直到達到最大放大倍數。 下一個點兩下手勢會將檢視器重設為初始檢視狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏合 </p> </td> 
   <td colname="col2"> <p>放大或縮小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>滑动 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重設狀態，手勢會執行原生頁面捲動。 </p> <p> 放大影像時，它會移動影像。 如果將影像移至檢視邊緣，並朝該方向執行撥動，手勢會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

該檢視器也支援觸控式輸入和滑鼠輸入，適用於Windows裝置上的觸控式熒幕和滑鼠。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可使用完整的鍵盤。

另請參閱 [鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 內嵌基本縮放檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 有時，網頁會提供連結，在選取時會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，必須直接將檢視器內嵌在託管頁面中。 在後一種情況下，網頁可能具有靜態頁面佈局，或使用回應式設計，在不同裝置或不同瀏覽器視窗大小上顯示不同。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

**關於彈出式模式**

在快顯視窗模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

快顯視窗模式最常用於行動裝置。 網頁會使用載入檢視器 `window.open()` JavaScript呼叫，已正確設定 `A` HTML元素或任何其他合適的方法。

建議您使用現成的HTML頁面作為快顯視窗操作模式。 在此案例中，其名稱為 [!DNL BasicZoomViewer.html] 且位於 [!DNL html5/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/html5/BasicZoomViewer.html]

您可以套用自訂CSS來實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B" target="_blank">Open popup viewer</a>
```

**關於固定大小內嵌模式和回應式設計內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，該網頁可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可依裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此方法適用於具有靜態配置的網頁。

回應式設計內嵌假設檢視器必須在執行階段調整大小來回應其容器的大小變更 `DIV`. 最常見的使用案例是將檢視器新增至使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器的方式而異 `DIV`. 如果網頁僅設定容器的寬度 `DIV`，只要其高度不受限制，檢視器就會根據所使用資產的外觀比例，自動選擇其高度。 此功能可確保資產完全符合檢視要求，而不需在兩側加上任何邊框間距。 此使用案例最常用於使用回應式網頁設計版面架構(例如Bootstrap和Foundation)的網頁。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，檢視器只會填滿該區域，並遵循網頁版面提供的大小。 一個好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗大小調整大小。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器DIV。
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至網頁。

   建立檢視器需要您在HTML標頭中新增指令碼標籤。 在使用檢視器API之前，請務必先包含 [!DNL BasicZoomViewer.js]. 此 [!DNL BasicZoomViewer.js] 檔案位於 [!DNL html5/js/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/BasicZoomViewer.js]

如果檢視器部署在某個Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，則可以使用相對路徑。 否則，您需要指定已安裝IS-Viewers的其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/BasicZoomViewer.js"></script>
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

   以下是已定義預留位置DIV元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以宣告檢視器的靜態大小，將它設為 `.s7basiczoomviewer` 以絕對單位表示的頂層CSS類別，或是使用 `stagesize` 修飾元。

   將CSS的大小直接放在HTML頁面或自訂檢視器CSS檔案中。 之後會將其指派給Dynamic Media Classic中的檢視器預設集記錄，或明確使用樣式命令傳遞。

   另請參閱 [自訂基本縮放檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) 以取得有關使用CSS設定檢視器樣式的詳細資訊。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以設定 `stagesize` 修飾元(在Dynamic Media Classic的檢視器預設集記錄中)。 或者，您可以使用檢視器初始化程式碼明確傳遞 `params` 集合，或如命令參考一節中所述，以API呼叫形式執行，如下所示：

   ```html {.line-numbers}
   basicZoomViewer.setParam("stagesize", "640,480");
   ```

   建議使用以CSS為基礎的方法，並用於此範例。

1. 建立和初始化檢視器。

   完成上述步驟後，您會建立 `s7viewers.BasicZoomViewer` 類別，將所有設定資訊傳遞至其建構函式，並呼叫 `init()` 檢視器例項的方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有containerId欄位，其中包含檢視器的名稱 `container ID` 和巢狀 `params` 具有檢視器支援之設定引數的JSON物件。 在此案例中， `params` 物件至少必須將影像伺服URL傳遞為 `serverUrl` 屬性，並將初始資產設為 `asset` 引數。 JSON型初始化API可讓您使用一行程式碼建立及啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾。 如需最大相容性，請呼叫 `init()` 方法（在結尾之前） `BODY` 標籤或內文 `onload()` 事件。

   同時，容器元素不一定會成為網頁版面的一部分。 例如，它可能會使用以下專案隱藏： `display:none` 樣式已指派給它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 發生此事件時，檢視器會自動繼續載入。

   以下範例說明如何建立檢視器例項、將最低必要的設定選項傳遞至建構函式，以及呼叫 `init()` 方法。 範例假設 `basicZoomViewer` 是檢視器例項； `s7viewer` 是預留位置的名稱 `DIV`； `http://s7d1.scene7.com/is/image/` 是「影像伺服」URL，以及 `Scene7SharedAssets/Backpack_B` 為資產：

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Backpack_B", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   下列程式碼為將基本縮放檢視器嵌入固定大小的簡單網頁的完整範例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
    "params":{ 
     "asset":"Scene7SharedAssets/Backpack_B", 
     "serverurl":"http://s7d1.scene7.com/is/image/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下範例頁面說明高度不受限制的回應式設計內嵌在實際應用中的更多情況：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**定義寬度和高度的彈性大小內嵌**

如果有定義寬度和高度的彈性大小內嵌，則網頁樣式會不同。 它提供兩種大小給 `"holder"` 在瀏覽器視窗中進行DIV和置中。 此外，網頁會設定 `HTML` 和 `BODY` 元素至100%。

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用Setter型API內嵌**

您可以使用setter型API和no-args建構函式，而不使用JSON型初始化。 使用此API建構函式不接受任何引數，而且設定引數是透過以下方式指定的： `setContainerId()`， `setParam()`、和 `setAsset()` 具有個別JavaScript呼叫的API方法。

以下範例說明如何將固定大小內嵌與setter型API搭配使用：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7basiczoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var basicZoomViewer = new s7viewers.BasicZoomViewer(); 
basicZoomViewer.setContainerId("s7viewer"); 
basicZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
basicZoomViewer.setAsset("Scene7SharedAssets/Backpack_B"); 
basicZoomViewer.init(); 
</script> 
</body> 
</html>
```
