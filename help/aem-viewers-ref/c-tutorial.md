---
title: Viewer SDK教學課程
description: Viewer SDK提供了一組JavaScript型元件，用於自訂檢視器開發。 檢視器是網頁型應用程式，可將Adobe Dynamic Media提供的多媒體內容內嵌在網頁中。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Viewer SDK教學課程{#viewer-sdk-tutorial}

Viewer SDK提供了一組JavaScript型元件，用於自訂檢視器開發。 檢視器是網頁型應用程式，可將Adobe Dynamic Media提供的多媒體內容內嵌在網頁中。

例如，SDK提供互動式縮放和平移。 此外，影片還能讓您以全方位的視角檢視和影片播放，透過名為Dynamic Media Classic的後端應用程式，上傳至Adobe Dynamic Media的資產。

即使元件依賴HTML5功能，但設計上卻能搭配Android™和Apple iOS裝置，以及桌上型電腦（包括Internet Explorer和更新版本）使用。 這類體驗表示您可以為所有支援的平台提供單一工作流程。

SDK包含構成檢視器內容的UI元件。 您可以透過CSS以及具有某種支援角色（例如設定定義擷取以及剖析或追蹤）的非UI元件，為這些元件設定樣式。 所有元件行為都可透過修飾元進行自訂，您可以透過各種方式指定修飾元，例如 `name=value` URL中的配對。

本教學課程包含下列工作順序，可協助您建立基本縮放檢視器：

* [從Adobe Developer Connection下載最新的Viewer SDK](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [載入檢視器SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [新增樣式至檢視器](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [包含容器和ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [將MediaSet和色票元件新增至檢視器](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [將按鈕新增至檢視器](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [垂直設定色票](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## 從Adobe Developer Connection下載最新的Viewer SDK {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. 從Adobe Developer Connection下載最新的Viewer SDK <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->.

   >[!NOTE]
   >
   >您可以完成本教學課程，而不需要下載Viewer SDK套件，因為此SDK已從遠端載入。 不過，Viewer套件包含其他範例和API參考指南，可協助您建立自己的檢視器。

## 載入檢視器SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. 首先，請設定一個新頁面，以開發您要建立的基本縮放檢視器。

   請考量這個全新頁面，您用來設定空SDK應用程式的Bootstrap（或載入器）代碼。 開啟您最愛的文字編輯器，並在其中貼上下列HTML標示：

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   將下列JavaScript程式碼新增至 `script` 標籤時，它會將 `ParameterManager`. 這麼做可協助您準備在內建立和例項化SDK元件 `initViewer` 函式：

   ```javascript {.line-numbers}
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. 將檔案儲存為空白範本。 您可以使用任何想要的檔案名稱。

   日後建立任何檢視器時，都會使用此空白範本檔案作為參考。 此範本在本機運作，且可從網頁伺服器提供服務。

現在將樣式新增至檢視器。

## 新增樣式至檢視器 {#section-3783125360a1425eae5a5a334867cc32}

1. 對於您正在建立的這個完整頁面檢視器，您可以新增一些基本樣式。

   新增下列專案 `style` 封鎖至底部 `head`：

   ```html {.line-numbers}
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

現在包含元件 `Container` 和 `ZoomView`.

## 包含容器和ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. 包含元件以建立實際的檢視器 `Container` 和 `ZoomView`.

   插入下列內容 `include` 陳述式至底部 `<head>` 元素 — 在 [!DNL Utils.js] 指令碼已載入：

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. 現在可建立變數來參考各種SDK元件。

   將下列變數新增至主要匿名函式的頂端（就在上方） `s7sdk.Util.init()`：

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. 將下列內容插入 `initViewer` 函式中，以便您可以定義一些修飾元並將個別元件例項化：

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. 為了讓上述程式碼正確執行，請新增 `containerResize` 事件處理常式和helper函式：

   ```javascript {.line-numbers}
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. 預覽頁面，以便檢視您已建立的內容。 您的頁面應如下所示：

   ![檢視器範例一個影像](assets/viewer-1.jpg)

現在新增元件 `MediaSet` 和 `Swatches` 至您的檢視器。

## 將MediaSet和色票元件新增至檢視器 {#section-02b8c21dd842400e83eae2a48ec265b7}

1. 若要讓使用者能夠從影像集中選取影像，您可以新增元件 `MediaSet` 和 `Swatches`.

   新增下列SDK包含：

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 使用以下專案更新變數清單：

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. 具現化 `MediaSet` 和 `Swatches` 內的元件 `initViewer` 函式。

   請務必將 `Swatches` 之後的執行個體 `ZoomView` 和 `Container` 元件，否則棧疊順序會隱藏 `Swatches`：

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. 現在新增下列事件處理常式函式：

   ```javascript {.line-numbers}
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. 將下列CSS新增至，將色票置於檢視器底部 `style` 元素：

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. 預覽您的檢視器。

   請注意，色票位於檢視器的左下方。 若要讓色票取得整個檢視器寬度，請新增呼叫，以便在使用者調整瀏覽器大小時手動調整色票大小。 將下列專案新增至 `resizeViewer` 函式：

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   您的檢視器現在看起來像以下影像。 請嘗試調整檢視器瀏覽器視窗的大小，並注意產生的行為。

   ![檢視器範例2影像](assets/viewer-2.jpg)

現在新增放大、縮小和縮放重設按鈕到您的檢視器。

## 將按鈕新增至檢視器 {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 目前，使用者只能使用點按或觸控手勢進行縮放。 因此，請將一些基本縮放控制按鈕新增至檢視器。

   新增下列按鈕元件：

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. 使用以下專案更新變數清單：

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. 將按鈕例項化在底部 `initViewer` 函式。

   請記住，順序很重要，除非您指定 `z-index` 在CSS中：

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. 現在，將下列內容新增至，以定義按鈕的一些基本樣式 `style` 封鎖您的檔案頂端：

   ```CSS {.line-numbers}
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. 預覽您的檢視器。 它應如下所示：

   ![檢視器範例三影像](assets/viewer-3.jpg)

   現在請設定「色票」，讓色票垂直對齊右側。

## 垂直設定色票 {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 您可以直接在 `ParameterManager` 執行個體。

   將下列專案新增至 `initViewer` 函式中，以便您設定 `Swatches` 以單列顯示縮圖版面：

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. 在內更新下列調整大小呼叫 `resizeViewer`：

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. 編輯下列專案 `s7swatches` 中的規則 `ZoomViewer.css`：

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. 預覽您的檢視器。 它看起來像這樣：

   ![檢視器範例4影像](assets/viewer-4.jpg)

   您的基本縮放檢視器現已完成。

   此檢視器教學課程會說明Dynamic Media Viewer SDK提供的基本知識。 當您使用SDK時，可以使用各種標準元件來輕鬆為目標受眾建置豐富的檢視體驗並打造樣式。
