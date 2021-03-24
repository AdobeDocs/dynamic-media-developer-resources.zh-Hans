---
description: Video360查看器的配置属性。
solution: Experience Manager
title: Video360Player.ssl
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '187'
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

另请参阅[安全视频投放](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)。
