---
description: HTTPS视频交付
solution: Experience Manager
title: HTTPS视频交付
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,Business Practitioner
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# HTTPS视频交付{#https-video-delivery}

>[!NOTE]
>
>HTTP安全视频交付仅适用于安装了[Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2和安装了[Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

如果查看器按照本节开头所述的配置工作，则可以在HTTPS（安全）和HTTP（不安全）模式下发布视频交付。 在默认配置中，视频传输协议严格遵循嵌入网页的传输协议。 但是，可以强制HTTPS视频传送，而不考虑使用[Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md)配置属性嵌入网页时使用的协议。 （请注意，在创作模式下，视频预览始终通过HTTPS安全地交付。）

根据您在AEM中使用的发布Dynamic Media视频的方法，`Video360Player.ssl`配置属性的应用方式有所不同，如下所示：

* 如果您发布带有URL的Dynamic Media视频，则会将`Video360Player.ssl`附加到该URL。 例如，要强制安全视频交付，请在以下查看器URL示例的末尾附加`&Video360Player.ssl=on`:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   另请参阅[将URL关联到Web应用程序](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)。

* 如果发布包含嵌入代码的Dynamic Media视频，则需将`Video360Player.ssl`添加到嵌入代码片段中其他查看器配置参数的列表。 例如，要强制HTTPS视频交付，请按照以下示例附加`&Video360Player.ssl=on`:

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Video", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }).init(); 
   </script>
   ```

   另请参阅[在网页上嵌入视频](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)
