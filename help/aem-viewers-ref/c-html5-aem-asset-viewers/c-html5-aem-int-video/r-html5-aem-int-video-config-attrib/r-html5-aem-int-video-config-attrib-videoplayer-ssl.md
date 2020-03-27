---
description: 交互式视频查看器的配置属性。
seo-description: 交互式视频查看器的配置属性。
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: b4929e14-8712-4923-b9b1-62aa6721fc99
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# VideoPlayer.ssl{#videoplayer-ssl}

交互式视频查看器的配置属性。

>[!NOTE]
>
>此配置属性仅适用于安装了 [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) 的AEM 6.2和安装了 [Feature Pack NPR-15011的AEM 6.1](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)。

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动|开启</span> </p> </td> 
   <td colname="col2"> <p> 控制视频是通过安全SSL连接(HTTPS)还是不安全连接(HTTP)传送的。 </p> <p>当设置为 <span class="codeph"> 自动</span> ，视频投放协议将从嵌入网页的协议继承。 如果网页通过HTTPS加载，则视频也通过HTTPS传送，反之亦然。 如果网页位于HTTP上，则视频通过HTTP传送。 </p> <p>设置为开启 <span class="codeph"> 时</span>，视频投放始终通过安全连接进行，而与网页协议无关。 </p> <p>仅影响已发布的视频投放，在“作者”模式下，对于视频预览，将忽略该影响。 </p> </td> 
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

另请参阅安 [全视频投放](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)。
