---
description: Video360查看器的配置属性。
solution: Experience Manager
title: Video360Player.ssl
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,User
exl-id: 44efa378-c911-4449-8a10-61212d4392c6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 4%

---

# Video360Player.ssl{#video-player-ssl}

Video360查看器的配置属性。

>[!NOTE]
>
>此配置属性仅适用于安装了[功能包NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)的AEM 6.2和安装了[功能包NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)的AEM 6.1。

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|开启</span> </p> </td> 
   <td colname="col2"> <p> 控制视频是通过安全SSL连接(HTTPS)还是不安全的连接(HTTP)传送。 </p> <p>当设置为<span class="codeph"> auto</span>时，视频传输协议继承自嵌入网页的协议。 如果网页是通过HTTPS加载的，则视频也会通过HTTPS传送，反之亦然。 如果网页位于HTTP上，则视频将通过HTTP进行传输。 </p> <p>在</span>上设置为<span class="codeph">时，视频传输始终通过安全连接进行，而与网页协议无关。 </span></p> <p>仅影响已发布的视频交付，在创作模式下，视频预览会被忽略。 </p> </td> 
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

另请参阅[安全视频交付](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)。
