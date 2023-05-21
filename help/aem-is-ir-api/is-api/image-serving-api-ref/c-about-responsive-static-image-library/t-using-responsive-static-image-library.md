---
title: 使用Responsive影像資料庫
description: 若要將Responsive影像庫新增至網頁，並使用庫管理現有影像，請完成下列步驟。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# 使用Responsive影像資料庫{#using-responsive-image-library}

若要將Responsive影像庫新增至網頁，並使用庫管理現有影像，請完成下列步驟。

**若要使用Responsive影像資料庫**

1. 在Dynamic Media Classic中， [建立影像預設集](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) 以防您計畫搭配預設集使用回應式影像資料庫。

   定義與Responsive影像資料庫一起使用的影像預設集時，請勿使用任何會影響影像大小的設定，例如 `wid=`， `hei=`，或 `scl=`. 請勿在影像預設集中指定任何大小欄位。 請改為保留為空白值。
1. 將資料庫JavaScript檔案新增至您的網頁。

   使用程式庫API之前，請務必先包含 `responsive_image.js`. 此JavaScript檔案位於 `libs/` 標準IS-Viewers部署的子資料夾：

   `<s7viewers_root>/libs/responsive_image.js`
1. 設定現有影像。

   程式庫會從正在使用的影像執行個體讀取某些設定屬性。 在之前定義屬性 `s7responsiveImage` 這類影像會呼叫API函式。

   也建議您將現有的影像URL放入 `data-src` 屬性。 然後，設定現有的 `src` 屬性，將1x1GIF影像編碼為資料URI。 如此一來，可減少網頁在載入時傳送的HTTP要求數目。 不過請注意，如果需要SEO （搜尋引擎最佳化），最好設定 `title` 屬性。

   以下範例為定義 `data-breakpoints` 屬性，並使用編碼為資料URI的1x1GIF：

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 呼叫 `s7responsiveImage` 適用於資料庫管理的每個影像例項的API函式。

   呼叫 `s7responsiveImage` 適用於資料庫管理的每個影像例項的API函式。 進行這類呼叫後，資料庫會根據的執行階段大小，以從「影像伺服」下載的影像取代原始影像。 `IMG` 元素以及裝置熒幕的密度。

   下列程式碼是呼叫的範例 `s7responsiveImage` 影像上的API函式，假設 `responsiveImage` 是該影像的ID：

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 示例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

資料庫支援同時使用網頁上的許多影像執行個體。 因此，請針對您想要資料庫管理的每個影像，重複上述步驟1和2。

網頁應負責設定影像元素的樣式，使其大小可彈性調整。 Responsive影像資料庫本身不會區分固定大小和「流動」影像。 如果套用至固定大小的影像，則只會載入新影像一次。

下列程式碼為簡單網頁的完整範例，該網頁具有由Responsive Image資料庫管理的單一Fluid影像。 此範例包含額外的CSS樣式，可讓影像「回應」網頁瀏覽器視窗大小：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**使用智慧型裁切**

AEM 6.4和Dynamic Media Viewers 5.9提供兩種智慧型裁切模式：

* **手動**  — 使用者定義的中斷點和對應的影像服務命令會在影像元素的屬性內定義。
* **智慧型裁切**  — 系統會自動從傳遞伺服器擷取運算智慧型裁切轉譯。 最佳轉譯是使用影像元素的執行階段大小來選取。

若要使用智慧型裁切模式，請設定 `data-mode` 屬性至 `smart crop`. 例如：

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

關聯的影像元素會傳送 `s7responsiveViewer` 執行階段中斷點變更時的事件。

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
