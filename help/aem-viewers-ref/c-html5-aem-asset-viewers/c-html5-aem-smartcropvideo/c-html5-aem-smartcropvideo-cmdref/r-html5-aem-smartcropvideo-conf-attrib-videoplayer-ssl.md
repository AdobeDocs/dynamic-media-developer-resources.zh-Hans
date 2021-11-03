---
title: SmartCropVideoPlayer.ssl
description: 智能裁剪视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: f7d832f3-e9b1-4161-a572-851e538bb245
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# SmartCropVideoPlayer.ssl{#smartcropvideoplayer-ssl}

智能裁剪视频查看器的配置属性。

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[SmartCropVideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|开启</span> </p> </td> 
   <td colname="col2"> <p> 控制视频是通过安全SSL连接(HTTPS)还是不安全的连接(HTTP)传送。 </p> <p>当设置为 <span class="codeph"> 自动</span> 视频交付协议继承自嵌入网页的协议。 如果网页是通过HTTPS加载的，则视频也会通过HTTPS发送，反之，则会通过HTTPS发送。 如果网页位于HTTP上，则视频将通过HTTP进行传输。 </p> <p>当设置为 <span class="codeph"> on</span>，则视频交付始终通过安全连接进行，而与网页协议无关。 </p> <p>仅影响已发布的视频交付，在创作模式下，视频预览会被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

另请参阅 [安全视频交付](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
