---
title: HTTPS视频交付
description: HTTPS视频交付
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 68d37b5d-5015-4a98-84b8-8911ace327ed
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# HTTPS视频交付{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

如果查看器按本节开头所述的配置工作，则发布的视频投放可能会在HTTPS（安全）和HTTP（不安全）模式下发生。 在默认配置中，视频投放协议严格遵循嵌入网页的投放协议。 但是，无论使用嵌入网页所使用的协议如何，都可以强制HTTPS视频交付 [VideoPlayer.ssl](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771) 配置属性。 （创作模式下的视频预览始终通过HTTPS安全交付。）

取决于发布方法 [!DNL Dynamic Media] 您在Adobe Experience Manager中使用的视频， `VideoPlayer.ssl` 配置属性的应用方式有所不同，如下图所示：

* 如果您发布 [!DNL Dynamic Media] 带URL的视频，需在 `VideoPlayer.ssl` 到URL。 例如，要强制安全视频交付，您需要 `&VideoPlayer.ssl=on` 到以下查看器URL示例结尾：

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
  ```

  另请参阅 [将URL关联到您的Web应用程序](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)

* 如果您发布 [!DNL Dynamic Media] 包含嵌入代码的视频，您添加 `VideoPlayer.ssl` 嵌入代码片段中其他查看器配置参数的列表。 例如，要强制HTTPS视频交付，您需要 `&VideoPlayer.ssl=on` 如以下示例所示：

  ```html {.line-numbers}
  <style type="text/css"> 
   #s7interactivevideo_div.s7interactivevideoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
  <div id="s7interactivevideo_div"></div> 
  <script type="text/javascript"> 
   var s7interactivevideoviewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId" : "s7interactivevideo_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/Shoppable_Video_light", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "interactivedata": "content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt", 
     "VideoPlayer.contenturl": "https://adobedemo62-h.assetsadobe.com/is/content", 
     "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
   }) 
   /* // Example of interactive video event for quick view. 
     s7interactivevideoviewer.setHandlers({  
     "quickViewActivate": function(inData) { 
       var sku=inData.sku; //SKU for product ID 
      //To pass other parameter from the hotspot, you must add custom parameter during the hotspot setup as parameterName=value 
      loadQuickView(sku); //Replace this call with your quickview plugin 
      //Please refer to your quickviewer plugin for the quickview call 
      },  
  "initComplete":function() {  
      //--- Attach quickview pop-up to viewer container so pop-up works in fullscreen mode --- 
      var popup = document.getElementById('quickview_div'); // get custom quick view container 
      popup.parentNode.removeChild(popup); // remove it from current DOM 
      var sdkContainerId = s7interactivevideoviewer.getComponent("container").getInnerContainerId(); // get viewer container component 
      var inner_container = document.getElementById(sdkContainerId);  
      inner_container.appendChild(popup); //Attach custom quick view container to viewer 
      }  
     }); 
   */ 
   s7interactivevideoviewer.init(); 
  </script>
  ```

  另请参阅 [在网页上嵌入视频](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
