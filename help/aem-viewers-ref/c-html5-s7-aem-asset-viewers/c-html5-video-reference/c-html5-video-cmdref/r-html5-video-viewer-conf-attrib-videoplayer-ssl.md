---
description: 视频查看器的配置属性。
seo-description: 视频查看器的配置属性。
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
uuid: 969da9ea-c97c-4fa8-9207-21d6302609e5
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# VideoPlayer.ssl{#videoplayer-ssl}

视频查看器的配置属性。

>[!NOTE]
>
>此配置属性仅适用于安装了[功能包NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2和安装了[功能包NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|开启</span> </p> </td> 
   <td colname="col2"> <p> 控制是通过安全SSL连接(HTTPS)还是不安全连接(HTTP)传送视频。 </p> <p>设置为<span class="codeph"> auto</span>时，视频投放协议继承自嵌入网页的协议。 如果网页是通过HTTPS加载的，则视频也会通过HTTPS传输，反之亦然。 如果网页在HTTP上，则视频通过HTTP传送。 </p> <p>当在</span>上设置为<span class="codeph">时，视频投放始终在安全连接上发生，而与网页协议无关。 </span></p> <p>仅影响已发布的投放，在“创作”模式下，对于视频预览，将忽略该效果。 </p> </td> 
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

另请参阅[安全视频投放](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff)。
