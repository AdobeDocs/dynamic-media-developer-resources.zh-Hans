---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 011ef772-6760-4794-819e-2a822fbae1b5
TQID: 'https://experienceleague.adobe.com/R-8C-obmM18dPSWcLrekSvAzSRRTrthSDePpybEcCOc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> 启用或禁用用户通过鼠标或使用触控手势滚动样本的功能 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 0-1 </span>范围内的函数。 当移动的实际速度方向错误时，它是一个<span class="codeph"> % </span>值。 如果设置为<span class="codeph"> 1 </span>，则它会随鼠标移动。 如果设置为<span class="codeph"> 0 </span>，则根本不允许您向错误的方向移动。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-831c23dea82449bfa50fd155bea365b7}

可选.

## 默认 {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## 示例 {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]

