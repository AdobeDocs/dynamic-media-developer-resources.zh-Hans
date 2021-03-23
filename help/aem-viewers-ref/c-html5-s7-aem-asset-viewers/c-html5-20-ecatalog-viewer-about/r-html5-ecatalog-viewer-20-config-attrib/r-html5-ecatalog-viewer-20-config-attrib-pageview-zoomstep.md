---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
uuid: 11458300-4a1b-4623-8ea1-db804daab3cf
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 6%

---


# PageView.zoomstep{#pageview-zoomstep}

` [PageView.|<containerId>_pageView.]zoomstep= *`斯`*[, *`特普利特`*]`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 步骤</span></span> </p> </td> 
   <td colname="col2"> <p> 配置将分辨率提高或降低两倍所需的放大和缩小操作数。 每个缩放操作的分辨率更改是每步2^1。 设置为<span class="codeph"> 0</span>可通过单个缩放操作缩放到完整分辨率。 </p> </td> 
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

`1,1`

## 示例 {#section-1e20672d42c845bd84f02f88cbc53efc}

`zoomstep=2,3`
