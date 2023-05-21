---
title: 全景檢視器
description: HTML5全景檢視器是一種顯示全景影像的影像檢視器。 此檢視器的用途是顯示球面全景，也稱為等矩形影像。 它支援透過陀螺儀移動自動平移和平移。 專為桌上型電腦和行動裝置所設計。 支援行動裝置的使用者可使用虛擬實境觀看模式。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 0%

---

# 全景{#panoramic}

HTML5全景檢視器是一種顯示全景影像的影像檢視器。 此檢視器的用途是顯示球面全景，也稱為等矩形影像。 它支援透過陀螺儀移動自動平移和平移。 專為桌上型電腦和行動裝置所設計。 支援行動裝置的使用者可使用虛擬實境觀看模式。

另請參閱 [系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


檢視器型別514。

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## 使用全景檢視器 {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramic Viewer代表主要JavaScript檔案和一組協助程式檔案，由檢視器在執行階段下載。 協助程式檔案集是單一JavaScript包含，以及此特定檢視器、資產、CSS使用的所有HTML5 Viewer SDK元件。
HTML5全景檢視器既可透過隨IS-Viewers提供的生產就緒HTML頁面在快顯視窗模式使用，也可透過內嵌模式使用，透過已記錄的API整合至目標網頁。
設定和外觀設定與其他HTML5檢視器的設定和外觀設定類似。 所有外觀設計都可透過自訂CSS來達成。

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器通用的命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與HTML5全景檢視器互動 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5全景檢視器支援透過拖曳或陀螺移動自動平移和導覽。

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>导航 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>桌面 </p> </td> 
   <td colname="col2"> <p>自動平移和拖曳以導覽。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>觸控裝置 </p> </td> 
   <td colname="col2"> <p>依預設，自動平移和拖曳以導覽。 在VR演算模式中透過陀螺儀移動進行導覽(vrrender=true)。
 </p> </td> 
  </tr> 
 </tbody> 
</table>

檢視器支援觸控式輸入和滑鼠輸入（使用觸控熒幕和滑鼠的Windows裝置），不過這項支援僅適用於Chrome、Internet Explorer 11和Edge網頁瀏覽器。
全景檢視器可以透過指定vrrender修飾元在虛擬現實(VR)模式下轉譯全景影像。 啟用vrrender時，全景影像會顯示在分割畫面中。 常見的使用案例是透過掛載於虛擬現實頭戴式耳機中的行動電話提供影像，為每隻眼睛提供個別影像。 檢視器會回應頭部的迴轉運動，並導覽整個影像。

## 內嵌HTML5全景檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 有時網頁會提供連結。 選取該連結會在單獨的瀏覽器視窗中開啟檢視器。 在其他情況下，可能有必要將檢視器內嵌在託管頁面中。 在後一種情況下，網頁可能具有靜態佈局，或「回應式」並在不同裝置或不同瀏覽器視窗大小上以不同方式顯示。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式內嵌。

**關於彈出式模式**

在彈出式模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或裝置方向變更時進行調整。

此模式最常用於行動裝置。 網頁會使用載入檢視器 `window.open()` JavaScript呼叫、正確設定的HTML元素或任何其他適當方式。

建議您使用現成的HTML頁面作為快顯視窗操作模式。 其名稱為 [!DNL PanoramicViewer.html] 而且它位於 [!DNL html5/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

視覺化自訂可透過套用自訂CSS來達成。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**關於固定大小嵌入模式和回應式嵌入模式**

在內嵌模式中，檢視器會新增至現有網頁，而現有網頁可能已有某些與檢視器無關的客戶內容。 檢視器通常只佔用網頁的一部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可依裝置型別自動調整版面的回應式網頁。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此方法適用於具有靜態配置的網頁。

回應式內嵌假設檢視器必須在執行階段調整大小來回應其容器DIV的大小變更。 最常見的使用案例是將檢視器新增至使用彈性配置的網頁。

在回應式模式中，檢視器的行為會因網頁大小其容器DIV的方式而異。 如果網頁僅設定容器DIV的寬度，而不限制其高度，則檢視器會根據所使用資產的外觀比例自動選擇其高度。 此方法可確保資產完全符合檢視，而不會在兩側加上任何邊框間距。 此使用案例最常用於使用回應式版面配置架構(例如Bootstrap、Foundation等)的網頁。

否則，如果網頁同時設定檢視器容器DIV的寬度和高度，則檢視器會填滿該區域，並遵循網頁版面配置所提供的大小。 一個好的範例是內嵌檢視器至強制回應覆蓋圖，其中覆蓋圖會根據網頁瀏覽器視窗大小調整大小。

**固定大小內嵌**

您可以執行下列動作，將檢視器新增至網頁：

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器 `DIV`.
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至網頁。

   建立檢視器需要您在HTML標頭中新增指令碼標籤。 在使用檢視器API之前，請務必先包含 [!DNL PanoramicViewer.js]. 此 [!DNL PanoramicViewer.js] 檔案位於 [!DNL html5/js/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

如果檢視器部署在某個Adobe Dynamic Media Classic伺服器上，且從相同網域提供服務，則可以使用相對路徑。 否則，您需要指定已安裝IS-Viewers的其中一個Adobe Dynamic Media Classic伺服器的完整路徑。

相對路徑如下所示：

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
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

   您可以宣告檢視器的靜態大小，將它設為 `.s7panoramicviewer` 以絕對單位或修飾元表示的頂層CSS類別 `stagesize`.

   CSS大小調整可直接放在HTML頁面或自訂檢視器CSS檔案中，稍後會將其指派給AOD中的檢視器預設集記錄，或明確使用樣式命令傳遞。 如需使用CSS設定檢視器樣式的詳細資訊，請參閱自訂檢視器區段。 以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` 修飾元可以透過params集合明確與檢視器初始化程式碼一起傳遞，或作為API呼叫傳遞，如命令參考一節中所述，如下所示：

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   建議使用CSS型方法，並在此範例中使用。

1. 建立和初始化檢視器。

   完成上述步驟後，您會建立 `s7viewers.PanoramicViewer` 類別，將所有設定資訊傳遞至其建構函式，並呼叫 `init(`)方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少應有containerId欄位，其中包含檢視器容器ID和巢狀引數JSON物件的名稱，以及檢視器支援的設定引數。 在此情況下，params物件必須至少將「影像伺服」URL傳遞為 `serverUrl` 屬性和初始資產做為資產引數。 JSON型初始化API可讓您使用單行程式碼建立及啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾。 如需最大相容性，請呼叫 `init()` 方法（在結尾之前） `BODY` 標籤或內文 `onload()` 事件。

   同時，容器元素不一定會成為網頁版面的一部分。 例如，它可能會使用以下專案隱藏： `display:none` 樣式已指派給它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

   以下範例說明如何建立檢視器例項、將最低必要的設定選項傳遞至建構函式，以及呼叫 `init()` 方法。 此範例假設 `panoramicViewer` 是檢視器例項， `s7viewer` 是預留位置的名稱 `DIV`， [!DNL http://s7d1.scene7.com/is/image/] 是「影像伺服」URL，以及 [!DNL Scene7SharedAssets/PanoramicImage-Sample] 是資產。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   下列程式碼是嵌入具有固定大小的全景檢視器的簡單網頁的完整範例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**高度不受限制的回應式設計內嵌**

透過回應式內嵌，網頁通常會有某種彈性的版面配置，可指定檢視器容器DIV的執行階段大小。 就本範例而言，假設網頁允許檢視器的容器DIV取得網頁瀏覽器視窗大小的80%，其高度不受限制。 網頁HTML代碼可能如下所示：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 
```

將檢視器新增至這類頁面類似於內嵌固定大小，唯一的差異是您不需要明確定義檢視器大小：

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟與固定大小內嵌的步驟相同。 容器DIV應新增至現有的「持有者」DIV。 下列程式碼是完整的範例，您可能會看到瀏覽器調整大小時檢視器大小的變化情況，以及檢視器外觀比例與資產相符的情況。

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
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

其餘的內嵌步驟等同於高度不受限制的回應式內嵌。 產生的範例為

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
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
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
