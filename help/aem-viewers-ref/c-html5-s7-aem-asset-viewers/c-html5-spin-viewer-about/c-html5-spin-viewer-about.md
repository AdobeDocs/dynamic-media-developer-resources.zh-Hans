---
title: Spin
description: 「迴轉檢視器」是一種影像檢視器，可提供360度的影像檢視，甚至多維度檢視（如果使用適當的迴轉集）。 它有縮放和迴轉工具、全熒幕支援以及選用的關閉按鈕。 專為桌上型電腦和行動裝置所設計。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---

# Spin{#spin}

「迴轉檢視器」是一種影像檢視器，可提供360度的影像檢視，甚至多維度檢視（如果使用適當的迴轉集）。 它有縮放和迴轉工具、全熒幕支援以及選用的關閉按鈕。 專為桌上型電腦和行動裝置所設計。

>[!NOTE]
>
>此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。

檢視器型別503。

另請參閱 [系統需求和先決條件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## 示範URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## 使用迴轉檢視器 {#section-e6c68406ecdc4de781df182bbd8088b4}

迴轉檢視器代表一個主要JavaScript檔案和一組協助程式檔案（單一JavaScript包含此特定檢視器使用的所有Viewer SDK元件、資產、CSS），由檢視器在執行階段下載。

「迴轉檢視器」既可透過隨IS-Viewers提供的生產就緒HTML頁面在快顯視窗模式使用，也可透過內嵌模式使用，透過已記錄的API整合至目標網頁。

設定和外觀設定與其他檢視器的設定和外觀設定類似。 所有外觀設計都可透過自訂CSS來達成。

另請參閱 [所有檢視器通用的命令參考 — 設定屬性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 和 [所有檢視器通用的命令參考 — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## 與迴轉檢視器互動 {#section-642e66ca38cd4032992840ec6c0b0cd2}

迴轉檢視器支援下列其他行動應用程式中常見的觸控手勢。 當檢視器無法處理使用者的撥動手勢時，會將事件轉送給網頁瀏覽器，以執行原生頁面捲動。 此功能可讓使用者在頁面中導覽，即使檢視器佔據裝置熒幕區域的大部分割槽域亦然。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>手势 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>點兩下 </p> </td> 
   <td colname="col2"> <p> 放大一個層級，直到達到最大放大倍數。 下一個點兩下手勢會將檢視器重設為初始檢視狀態。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>捏合 </p> </td> 
   <td colname="col2"> <p>放大或縮小影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水準撥動或輕觸 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重設狀態，它會水準旋轉設定。 </p> <p> 如果影像被放大，它會水準移動影像。 如果影像移至檢視邊緣，且仍在該方向完成撥動，手勢會執行原生頁面捲動。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直撥動或輕觸 </p> </td> 
   <td colname="col2"> <p> 如果影像處於重設狀態，則會在使用多維度迴轉集時變更垂直檢視角度。 在一維迴轉集中，手勢會執行原生頁面捲動。 或者，當多維度迴轉集位於最後一個或第一個軸上，使得垂直撥動不會導致垂直檢視角度變更時，手勢也會執行原生頁面捲動。 </p> <p> 如果影像放大，則會垂直移動影像。 如果影像移至檢視邊緣，且仍在該方向完成撥動，手勢會執行原生頁面捲動。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>該檢視器也支援觸控式輸入和滑鼠輸入，適用於具有觸控熒幕和滑鼠的Windows裝置。 不過，這項支援僅限Chrome、Internet Explorer 11和Edge網頁瀏覽器。

此檢視器可使用完整的鍵盤。

另請參閱 [鍵盤協助工具與導覽](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## 內嵌迴轉檢視器 {#section-6bb5d3c502544ad18a58eafe12a13435}

不同的網頁對檢視器行為有不同的需求。 有時，網頁會提供連結，在選取時會在個別瀏覽器視窗中開啟檢視器。 在其他情況下，必須直接將檢視器內嵌在託管頁面中。 在後一種情況下，網頁可能具有靜態頁面佈局，或使用回應式設計，在不同裝置或不同瀏覽器視窗大小上顯示不同。 為了滿足這些需求，檢視器支援三種主要操作模式：快顯視窗、固定大小內嵌和回應式設計內嵌。

**關於彈出式模式**

在快顯視窗模式中，檢視器會在個別的網頁瀏覽器視窗或標籤中開啟。 它會取用整個瀏覽器視窗區域，並在瀏覽器調整大小或行動裝置的方向變更時進行調整。

快顯視窗模式最常用於行動裝置。 網頁會使用載入檢視器 `window.open()` JavaScript呼叫，已正確設定 `A` HTML元素或任何其他合適的方法。

建議您使用現成的HTML頁面作為快顯視窗操作模式。 在此案例中，其名稱為 [!DNL SpinViewer.html] 且位於 [!DNL html5/] 標準IS-Viewers部署的子資料夾：

[!DNL <s7viewers_root>/html5/SpinViewer.html]

您可以套用自訂CSS來實現視覺化自訂。

以下是在新視窗中開啟檢視器的HTML程式碼範例：

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**關於固定大小內嵌模式和回應式設計內嵌模式**

在內嵌模式中，檢視器會新增至現有網頁，該網頁可能已有某些與檢視器無關的客戶內容。 檢視器通常只會佔用網頁的一部分空間。

主要使用案例是針對桌上型電腦或平板電腦裝置的網頁，以及可依裝置型別自動調整版面的回應式設計頁面。

當檢視器在初始載入後未變更其大小時，會使用固定大小內嵌。 此動作是擁有靜態版面之網頁的最佳選擇。

回應式設計內嵌假設檢視器必須在執行階段調整大小來回應其容器的大小變更 `DIV`. 最常見的使用案例是將檢視器新增至使用彈性頁面配置的網頁。

在回應式設計內嵌模式中，檢視器的行為會因網頁大小其容器的方式而異 `DIV`. 如果網頁僅設定容器的寬度 `DIV`，只要其高度不受限制，檢視器就會根據所使用資產的外觀比例，自動選擇其高度。 此功能可確保資產完全符合檢視要求，而不需在兩側加上任何邊框間距。 此使用案例最常用於使用回應式設計配置架構(例如Bootstrap或Foundation)的網頁。

否則，如果網頁同時設定檢視器容器的寬度和高度 `DIV`，檢視器只會填滿該區域，並遵循網頁版面提供的大小。 一個很好的範例可能是將檢視器內嵌到強制回應覆蓋圖中，其中覆蓋圖會根據網頁瀏覽器視窗大小調整大小。

**固定大小內嵌**

您可以執行下列動作，將「迴轉檢視器」新增至網頁：

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器 `DIV`.
1. 設定檢視器大小。
1. 建立和初始化檢視器。

1. 將檢視器JavaScript檔案新增至網頁。

   建立檢視器需要您在HTML標頭中新增指令碼標籤。 在使用檢視器API之前，請務必先包含 `SpinViewer.js`. `SpinViewer.js` 位在 [!DNL html5/js/] 標準IS-Viewers部署的子資料夾：

   `<s7viewers_root>/html5/js/SpinViewer.js`

   如果檢視器部署在某個AdobeDynamic Media伺服器上，且從相同網域提供服務，則可以使用相對路徑。 否則，您需要指定已安裝IS-Viewers的其中一個AdobeDynamic Media伺服器的完整路徑。

   相對路徑如下所示：

   ```html {.line-numbers}
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >僅參照主要檢視器JavaScript `include` 檔案時。 請勿在網頁程式碼中參考任何其他JavaScript檔案（這些檔案可能由檢視器的邏輯在執行階段下載）。 尤其請勿直接參照HTML5 SDK `Utils.js` 檢視器從載入的程式庫 `/s7viewers` 內容路徑（所謂的整合SDK） `include`)。 原因在於 `Utils.js` 或類似的執行階段檢視器程式庫完全由檢視器的邏輯管理，且位置會在檢視器版本之間變更。 Adobe不會保留次要檢視器的舊版本 `includes` 在伺服器上。
   >
   >
   >因此，直接參照任何次要JavaScript `include` 當日後部署新產品版本時，頁面上檢視器使用的檢視器功能會中斷檢視器。

1. 定義容器DIV。

   新增空的DIV元素至您要檢視器出現的頁面。 DIV元素必須定義其ID，因為此ID稍後會傳遞至檢視器API。

   預留位置DIV是定位元素，這表示 `position` CSS屬性已設定為 `relative` 或 `absolute`.

   以下是已定義預留位置DIV元素的範例：

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. 設定檢視器大小

   您可以宣告檢視器的靜態大小，將它設為 `.s7spinviewer` 以絕對單位表示的頂層CSS類別，或是使用 `stagesize` 修飾元。

   您可以將CSS的大小直接放在HTML頁面上，或放在自訂檢視器CSS檔案中。 它稍後會指派給Dynamic Media Classic中的檢視器預設集記錄，或使用樣式命令明確傳遞。

   另請參閱 [自訂迴轉檢視器](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) 以取得有關使用CSS設定檢視器樣式的詳細資訊。

   以下是在HTML頁面中定義靜態檢視器大小的範例：

   ```html {.line-numbers}
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   您可以設定 `stagesize` 修飾元(位於Dynamic Media Classic中的檢視器預設集記錄中)。 或者，您可以使用檢視器初始化程式碼明確傳遞 `params` 集合，或作為API呼叫，如命令參考一節中所述，如下所示：

   ```html {.line-numbers}
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   建議使用以CSS為基礎的方法，並用於此範例。

1. 建立和初始化檢視器。

   完成上述步驟後，您會建立 `s7viewers.SpinViewer` 類別，將所有設定資訊傳遞至其建構函式，並呼叫 `init()` 檢視器例項的方法。 設定資訊會以JSON物件的形式傳遞至建構函式。 此物件至少具有 `containerId` 包含檢視器容器ID名稱且已巢狀的欄位 `params` 包含檢視器支援之設定引數的JSON物件。 在此案例中 `params` 物件，至少必須將影像伺服URL傳遞為 `serverUrl` 屬性和初始資產為 `asset` 引數。 JSON型初始化API可讓您使用單行程式碼建立及啟動檢視器。

   請務必將檢視器容器新增至DOM，讓檢視器程式碼可依其ID找到容器元素。 有些瀏覽器會延遲建立DOM，直到網頁結尾。 如需最大相容性，請呼叫 `init()` 方法（在結尾之前） `BODY` 標籤或內文 `onload()` 事件。

   同時，容器元素不一定會成為網頁版面配置的一部分。 例如，您可以使用 `display:none` 樣式已指派給它。 在此情況下，檢視器會延遲其初始化程式，直到網頁將容器元素帶回版面配置為止。 當此動作發生時，檢視器載入會自動繼續。

   以下範例說明如何建立檢視器例項、將最低必要的設定選項傳遞至建構函式，並呼叫 `init()` 方法。 範例假設 `spinViewer` 是檢視器例項， `s7viewer` 是預留位置的名稱 `DIV`， [!DNL http://s7d1.scene7.com/is/image/] 是「影像伺服」URL，以及 [!DNL Scene7SharedAssets/SpinSet_Sample] 是資產。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   下列程式碼為將「迴轉檢視器」嵌入固定大小的簡單網頁的完整範例：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高度不受限制的回應式設計內嵌**

透過回應式設計內嵌，網頁通常會有某種彈性的版面配置，可指定檢視器容器的執行階段大小 `DIV`. 在此範例中，假設網頁允許檢視器的容器 `DIV` 以取得網頁瀏覽器視窗大小的40%，其高度不受限制。 產生的網頁HTML代碼如下所示：

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

將檢視器新增至這類頁麵類似於固定大小內嵌，唯一的差異是您不需要明確定義檢視器大小。

1. 將檢視器JavaScript檔案新增至網頁。
1. 定義容器DIV。
1. 建立和初始化檢視器。

上述所有步驟與固定大小內嵌的步驟相同。 新增容器 `DIV` 至現有的「持有者」 `DIV`. 下列程式碼為完整範例。 您可以檢視瀏覽器調整大小時檢視器大小的變化情況，以及檢視器外觀比例與資產相符的方式。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下範例頁面說明高度不受限制的回應式設計內嵌的更多實際使用案例：

[即時示範](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[替代示範位置](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**定義寬度和高度的彈性大小內嵌**

如果有定義寬度和高度的彈性大小內嵌，則網頁樣式會不同。 也就是說，它為「托架」提供兩種尺寸 `DIV` 並將其置中於瀏覽器視窗中。 此外，網頁會設定 `HTML` 和 `BODY` 元素至100%：

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**使用Setter型API內嵌**

您可以使用setter型API和no-args建構函式，而不使用JSON型初始化。 使用該API建構函式不會接受任何引數，而且會使用下列專案指定設定引數： `setContainerId()`， `setParam()`、和 `setAsset()` 具有個別JavaScript呼叫的API方法。

以下範例顯示固定大小內嵌以setter為基礎的API：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
