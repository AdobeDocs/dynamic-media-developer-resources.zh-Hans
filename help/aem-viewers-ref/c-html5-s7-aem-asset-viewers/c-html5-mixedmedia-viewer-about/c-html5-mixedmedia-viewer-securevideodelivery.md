---
title: HTTPS視訊傳送
description: HTTPS視訊傳送
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# HTTPS視訊傳送{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

如果檢視器在設定中依本節開頭所述的方式運作，則發佈的視訊傳送可能會同時在HTTPS （安全）和HTTP （不安全）模式中發生。 在預設設定中，視訊傳送通訊協定會嚴格遵循內嵌網頁的傳送通訊協定。 不過，不論使用內嵌網頁所使用的通訊協定，還是強制HTTPS視訊傳送是可能的。 [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) 設定屬性。 （作者模式下的視訊預覽一律會透過HTTPS安全地傳送。）

根據您在Adobe Experience Manager中使用的Dynamic Media影片發佈方法， `VideoPlayer.ssl` 組態屬性的套用方式不同，如下所示：

* 如果您使用URL發佈Dynamic Media影片，您會附加 `VideoPlayer.ssl` 到URL。 例如，若要強制進行安全視訊傳送，您需在 `&VideoPlayer.ssl=on` 至下列檢視器URL範例結尾：

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   另請參閱 [(將URL連結至您的網頁應用程式](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* 如果您使用內嵌程式碼發佈Dynamic Media影片，請新增 `VideoPlayer.ssl` 至內嵌程式碼片段中其他檢視器設定引數的清單。 例如，若要強制HTTPS視訊傳送，您需附加 `&VideoPlayer.ssl=on` 如下列範例所示：

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

   另請參閱 [(將影片內嵌在網頁上](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
