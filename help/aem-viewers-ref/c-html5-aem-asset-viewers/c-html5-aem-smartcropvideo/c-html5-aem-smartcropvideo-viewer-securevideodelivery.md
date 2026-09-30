---
title: HTTP视频交付
description: HTTP视频交付
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: b809a11f-3c2d-4abd-b317-fabb36245b1b
TQID: 'https://experienceleague.adobe.com/GEFBNZe72VvcI9VXDusYjbDghMmsaFaIAWJWcFuwFps'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%
---
# HTTP视频交付{#http-video-delivery}

<!--
 >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).
-->

如果查看器按本节开头所述的配置工作，则发布的视频投放可能会在HTTPS（安全）和HTTP（不安全）模式下发生。 在默认配置中，视频投放协议严格遵循嵌入网页的投放协议。 但是，可以使用[SmartCropVideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e)配置属性嵌入网页，而不考虑所使用的协议，强制进行HTTPS视频交付。 （创作模式下的视频预览始终通过HTTPS安全交付。）

根据您在Adobe Experience Manager中使用的Dynamic Media视频发布方法，`SmartCropVideoPlayer.ssl`配置属性的应用有所不同，如以下所示：

* 如果您发布带有URL的Dynamic Media视频，则会将`SmartCropVideoPlayer.ssl`附加到URL。

<!-- For example, to force secure video delivery, you append `&SmartCropVideoPlayer.ssl=on` to the end of the following viewer URL example: -->

<!--

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/SmartCropVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&SmartCropVideoPlayer.ssl=on
  ```

  -->

另请参阅[将URL链接到您的Web应用程序](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=zh-Hans#dynamic)。

* 如果您使用嵌入代码发布Dynamic Media视频，则在嵌入代码片段中将`SmartCropVideoPlayer.ssl`添加到其他查看器配置参数列表中。

<!-- For example, to force HTTPS video delivery, you append `&SmartCropVideoPlayer.ssl=on` as in the following example: -->

<!--

  ```
  <style type="text/css"> 
   #s7video_div.s7videoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
  <div id="s7video_div"></div> 
  <script type="text/javascript"> 
   var s7videoviewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId" : "s7video_div", 
    "params" : {  
     "SmartCropVideoPlayer.ssl" : "on", 
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

  -->

另请参阅[在网页上嵌入视频](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=zh-Hans#dynamic)。
