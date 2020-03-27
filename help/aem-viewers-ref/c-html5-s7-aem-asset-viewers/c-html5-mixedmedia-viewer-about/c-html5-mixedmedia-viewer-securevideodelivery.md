---
description: 'null'
seo-description: 'null'
seo-title: HTTPS视频投放
solution: Experience Manager
title: HTTPS视频投放
topic: Dynamic media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# HTTPS视频投放{#https-video-delivery}

>[!NOTE]
>
>安全视频投放仅适用于安装了 [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) 的AEM 6.2和安装了 [Feature Pack NPR-15011的AEM 6.1](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)。

如果查看器按照本节开头所述的配置工作，则发布的视频投放可以在HTTPS（安全）和HTTP（不安全）模式下进行。 在默认配置中，视频投放协议严格遵循嵌入网页的投放协议。 但是，可以强制HTTPS视频投放，而不考虑使用 [VideoPlayer.ssl配置属性嵌入网页所使用的协议](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) 。 (请注意，在创作模式下，视频预览始终通过HTTPS安全交付。)

根据您在AEM中使用的发布Dynamic Media视频的方法，配置属性的应用方 `VideoPlayer.ssl` 式会有所不同，如下所示：

* 如果您发布包含URL的Dynamic Media视频，则需在该URL `VideoPlayer.ssl` 后面追加。 例如，要强制进行安全视频投放，请 `&VideoPlayer.ssl=on` 在以下查看器URL示例的末尾追加：

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   See also [(Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* 如果发布包含嵌入代码的Dynamic Media视频，则需在嵌入代 `VideoPlayer.ssl` 码片断中添加其他查看器配置参数的列表。 例如，要强制HTTPS视频投放，请 `&VideoPlayer.ssl=on` 像以下示例中一样附加：

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

   See also [(Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

