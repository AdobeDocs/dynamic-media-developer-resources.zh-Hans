---
title: SmartCropVideoPlayer.ssl
description: 智慧型裁切視訊檢視器的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 590ef156-0afe-4e65-b84b-b33f7c7d7b02
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# SmartCropVideoPlayer.ssl{#smartcropvideoplayer-ssl}

智慧型裁切視訊檢視器的設定屬性。

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[SmartCropVideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動|開啟</span> </p> </td> 
   <td colname="col2"> <p> 控制視訊是透過安全SSL連線(HTTPS)或不安全連線(HTTP)傳送。 </p> <p>當設定為 <span class="codeph"> 自動</span> 視訊傳送通訊協定繼承自內嵌網頁的通訊協定。 如果網頁是透過HTTPS載入，影片也會透過HTTPS傳送，反之亦然。 如果網頁位於HTTP上，則會透過HTTP傳送影片。 </p> <p>當設定為 <span class="codeph"> 於</span>，無論網頁通訊協定為何，影片傳送一律會透過安全連線進行。 </p> <p>只會影響已發佈的視訊傳送，且在作者模式中預覽視訊時會被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

另請參閱 [安全視訊傳送](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
