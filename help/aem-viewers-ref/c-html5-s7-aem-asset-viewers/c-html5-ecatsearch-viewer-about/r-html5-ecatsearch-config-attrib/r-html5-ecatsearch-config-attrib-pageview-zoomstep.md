---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
topic: Dynamic media
uuid: 27eb2a48-008b-455e-9a03-41bb4030271b
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 7%

---


# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`斯`*[, *`特普利特`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步骤</span></span> </p> </td> 
   <td colname="col2"> <p> 配置增大或减小分辨率所需的放大和缩小操作数（2倍）。 每个缩放操作的分辨率更改是每步2^1。 设置为<span class="codeph"> 0</span>，通过单个缩放操作缩放到完整分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相对于全分辨率图像的最大缩放分辨率。 默认值为<span class="codeph"> 1.0</span>，它不允许缩放超出完整分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-636d35a4791447039f1902973f568320}

可选。

## 默认 {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## 示例 {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
