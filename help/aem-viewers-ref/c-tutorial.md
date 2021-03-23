---
description: 查看器SDK为自定义查看器开发提供了一组基于JavaScript的组件。 查看器是基于Web的应用程序，允许将Adobe Dynamic Media提供的富媒体内容嵌入网页中。
solution: Experience Manager
title: 查看器SDK教程
feature: Dynamic Media Classic，查看器，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 0%

---


# 查看器SDK教程{#viewer-sdk-tutorial}

查看器SDK为自定义查看器开发提供了一组基于JavaScript的组件。 查看器是基于Web的应用程序，允许将Adobe Dynamic Media提供的富媒体内容嵌入网页中。

例如，SDK提供交互式缩放和平移。 它还提供了360°视图和视频回放，这些资源通过称为Dynamic Media Classic的后端应用程序上传到Adobe Dynamic Media。

即使这些组件依赖HTML5功能，它们设计为可用于Android和Apple iOS设备以及桌面（包括Internet Explorer及更高版本）。 这种体验意味着您可以为所有受支持的平台提供一个工作流。

SDK由构成查看器内容的UI组件组成。 您可以通过CSS和具有某种支持角色的非UI组件设置这些组件的样式，如设置定义获取、分析或跟踪。 所有组件行为都可通过修饰符进行自定义，您可以通过多种方式指定，例如，作为URL中的`name=value`对。

本教程包括以下任务顺序，帮助您创建基本的缩放查看器：

* [从Adobe Developer Connection下载最新的Viewer SDK](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [加载查看器SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [向查看器添加样式](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [包括容器和ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [将MediaSet和色板组件添加到查看器](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [向查看器添加按钮](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [垂直配置色板](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## 从Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}下载最新的Viewer SDK

1. 从Adobe Developer Connection [此处](https://marketing.adobe.com/developer/devcenter/scene7/show)下载最新的Viewer SDK。

   >[!NOTE]
   >
   >您无需下载查看器SDK包即可完成本教程，因为SDK实际上是远程加载的。 但是，查看器包中包含其他示例和API参考指南，在您创建自己的查看器时，该指南会很有帮助。

## 加载查看器SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. 开始，可通过设置新页面来开发您要创建的基本缩放查看器。

   可以将它视为用于设置空SDK应用程序的引导程序（或加载程序）代码。 打开您喜爱的文本编辑器，并将以下HTML标记粘贴到其中：

   ```
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

   在`script`标记内添加以下JavaScript代码以初始化`ParameterManager`。 这有助于您准备在`initViewer`函数中创建和实例化SDK组件：

   ```
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

1. 将文件另存为空模板。 可以使用任何所需的文件名。

   将来创建任何新查看器时，您将使用此空模板文件作为引用。 此模板在本地工作，并且从Web服务器提供时也可正常工作。

您现在将向查看器添加样式。

## 将样式添加到查看器{#section-3783125360a1425eae5a5a334867cc32}

1. 对于您正在创建的整个页面查看器，可以添加一些基本样式。

   在`head`的底部添加以下`style`块：

   ```
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

您现在将包含组件`Container`和`ZoomView`。

## 包括容器和ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. 通过包含组件`Container`和`ZoomView`创建实际查看器。

   在加载[!DNL Utils.js]脚本后，在`<head>`元素底部插入以下`include`语句：

   ```
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. 现在创建变量以引用各种SDK组件。

   将以下变量添加到主匿名函数的顶部，就在`s7sdk.Util.init()`上方：

   ```
   var container, zoomView;
   ```

1. 在`initViewer`函数中插入以下内容，以定义一些修饰符并实例化各个组件：

   ```
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

1. 要使上述代码正常运行，请添加`containerResize`事件处理程序和帮助函数：

   ```
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

1. 预览页面，以便查看已创建的内容。 您的页面将如下所示：

   ![](assets/viewer-1.jpg)

您现在将组件`MediaSet`和`Swatches`添加到查看器中。

## 将MediaSet和色板组件添加到查看器{#section-02b8c21dd842400e83eae2a48ec265b7}

1. 要允许用户从集中选择图像，可以添加组件`MediaSet`和`Swatches`。

   添加以下SDK包括：

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 使用以下内容更新变量列表:

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. 在`initViewer`函数中实例化`MediaSet`和`Swatches`组件。

   请务必在`ZoomView`和`Container`组件之后实例化`Swatches`实例，否则堆叠顺序会隐藏`Swatches`:

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. 现在添加以下事件处理函数：

   ```
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

1. 将以下CSS添加到`style`元素，将色板放置在查看器底部：

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. 预览您的查看器。

   请注意，色板位于查看器的左下角。 要使色板具有整个查看器宽度，请添加一个调用，在用户调整其浏览器大小时手动调整色板大小。 在`resizeViewer`函数中添加以下内容：

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   您的查看器现在类似于下图。 尝试调整查看器的浏览器窗口大小，并注意结果行为。

   ![](assets/viewer-2.jpg)

现在，您将向查看器添加放大、缩小和缩放重置按钮。

## 将按钮添加到查看器{#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 当前，用户只能使用单击或触控手势进行缩放。 因此，向查看器添加一些基本的缩放控制按钮。

   添加以下按钮组件：

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. 使用以下内容更新变量列表:

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. 实例化`initViewer`函数底部的按钮。

   请记住，顺序很重要，除非您在CSS中指定`z-index`:

   ```
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. 现在，通过向文件顶部的`style`块添加以下内容，为按钮定义一些基本样式：

   ```
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

1. 预览您的查看器。 它将如下所示：

   ![](assets/viewer-3.jpg)

   您现在将配置色板，以便它们在右侧垂直对齐。

## 垂直配置色板{#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 您可以直接在`ParameterManager`实例上配置修饰符。

   在`initViewer`函数顶部添加以下内容，以将`Swatches`缩略图布局配置为单行：

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. 在`resizeViewer`内更新以下调用大小：

   ```
   swatches.resize(swatches.getWidth(), height);
   ```

1. 在`ZoomViewer.css`中编辑以下`s7swatches`规则：

   ```
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. 预览您的查看器。 它将如下所示：

   ![](assets/viewer-4.jpg)

   基本的缩放查看器现已完成。

   此查看器教程涉及Dynamic Media查看器SDK提供的基本功能。 使用SDK时，您可以使用各种标准组件轻松为您的目标受众构建丰富的查看体验并为其添加样式。

