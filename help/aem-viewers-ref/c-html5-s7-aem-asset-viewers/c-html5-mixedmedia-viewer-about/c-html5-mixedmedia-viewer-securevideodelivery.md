---
title: HTTPS视频交付
description: HTTPS视频交付
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# HTTPS视频交付{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

如果查看器按本节开头所述的配置工作，则发布的视频投放可能会在HTTPS（安全）和HTTP（不安全）模式下发生。 在默认配置中，视频投放协议严格遵循嵌入网页的投放协议。 但是，可以使用[VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e)配置属性来强制执行HTTPS视频交付，而不考虑嵌入网页所使用的协议。 （创作模式下的视频预览始终通过HTTPS安全交付。）

根据您在Adobe Experience Manager中使用的Dynamic Media视频发布方法，`VideoPlayer.ssl`配置属性的应用有所不同，如以下所示：

* 如果您发布带有URL的Dynamic Media视频，则会将`VideoPlayer.ssl`附加到URL。

<!-- For example, to force secure video delivery, you append `&VideoPlayer.ssl=on` to the end of the following viewer URL example: -->

<!--

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
  ```

-->

另请参阅[(将URL链接到您的Web应用程序](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)。

* 如果您使用嵌入代码发布Dynamic Media视频，则在嵌入代码片段中将`VideoPlayer.ssl`添加到其他查看器配置参数列表中。

<!-- For example, to force HTTPS video delivery, you append `&VideoPlayer.ssl=on` as in the following example: -->

<!--

  ```
  <style type="text/css"> 
   #s7mixedmedia_div.s7mixedmediaviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
  <div id="s7mixedmedia_div"></div> 
  <script type="text/javascript"> 
   var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
    "containerId" : "s7mixedmedia_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
   }).init(); 
  </script>
  ```

-->

另请参阅[(在网页上嵌入视频](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)。
