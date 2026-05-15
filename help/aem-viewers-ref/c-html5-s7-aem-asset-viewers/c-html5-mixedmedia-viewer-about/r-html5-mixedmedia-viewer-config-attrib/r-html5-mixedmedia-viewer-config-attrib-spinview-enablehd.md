---
title: SpinView.enableHD
description: SpinView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
TQID: 'https://experienceleague.adobe.com/sVDq51PMMpTHbeBjGsIM3WS2p-Ap1ifJOBLiMylzrek'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 84
ht-degree: 3%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">始终|从不|限制</span> </p> </td> 
   <td colname="col2"> <p> 允许、限制或禁止对<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备进行优化，这些设备是指具有高密度显示屏的设备，如iPhone4和类似设备。 如果处于活动状态，则组件会限制IS图像请求的大小，就像设备只有<span class="codeph"> 1</span>的像素比一样，因此会减少带宽。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用<span class="codeph">限制</span>设置，则组件将启用高像素密度，但最多只能启用指定的限制。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
