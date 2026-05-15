---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
TQID: 'https://experienceleague.adobe.com/fceYX6xApL3EyDRk3FQFnzew7C4-Ax3acpPJH-HVrKw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# PageView.zoomstep{#pageview-zoomstep}

[!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`步骤`*[, *`限制`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">步骤</span></span> </p> </td> 
   <td colname="col2"> <p> 配置要将分辨率增大或减小2倍所需的放大和缩小操作的次数。 每步缩放操作的分辨率变更为2^1。 设置为<span class="codeph"> 0</span>可通过单个缩放操作缩放到完全分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">限制</span></span> </p> </td> 
   <td colname="col2"> <p> 指定相对于全分辨率图像的最大缩放分辨率。 默认值为<span class="codeph"> 1.0</span>，不允许缩放超过完全分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-636d35a4791447039f1902973f568320}

可选.

## 默认 {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## 示例 {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
