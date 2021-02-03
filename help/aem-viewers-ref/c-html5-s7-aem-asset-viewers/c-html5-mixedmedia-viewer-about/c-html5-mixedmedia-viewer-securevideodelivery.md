---
description: HTTPS视频投放
solution: Experience Manager
title: HTTPS视频投放
topic: Dynamic Media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
translation-type: tm+mt
source-git-commit: d38df1eb4713c034727ad0eb10834dc156122beb
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---


# HTTPS视频投放{#https-video-delivery}

>[!NOTE]
>
>安全视频投放仅适用于安装[功能包-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2和安装[功能包NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

如果查看器按照本节开头概述的配置工作，则发布的视频投放可以在HTTPS（安全）和HTTP（不安全）模式下进行。 在默认配置中，视频投放协议严格遵循嵌入网页的投放协议。 但是，可以强制HTTPS视频投放，而不考虑使用[VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e)配置属性嵌入网页所使用的协议。 (请注意，在“创作”模式下，视频预览始终通过HTTPS安全交付。)

根据您在AEM中使用的发布Dynamic Media视频的方法，`VideoPlayer.ssl`配置属性的应用方式不同，如下所示：

* 如果发布带有URL的Dynamic Media视频，则在URL后面附加`VideoPlayer.ssl`。 例如，要强制进行安全视频投放，请在以下查看器URL示例的末尾附加`&VideoPlayer.ssl=on`:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   另请参阅[(将URL关联到您的Web 应用程序](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)。

* 如果发布包含嵌入代码的Dynamic Media视频，则在嵌入代码片断中将`VideoPlayer.ssl`添加到其他查看器配置参数的列表。 例如，要强制HTTPS视频投放，请按照以下示例追加`&VideoPlayer.ssl=on`:

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

   另请参阅[(在网页上嵌入视频](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)。

