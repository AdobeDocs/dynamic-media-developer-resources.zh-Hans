---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
TQID: 'https://experienceleague.adobe.com/h7jV66-f8J9UoMxsROgQrDLSN-ONyXSZ71gj75-Z7v8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">值</span></span> </p> </td> 
   <td colname="col2"> <p> 表示当SpinView空闲时在每个方向预载的最大帧数。 值为<span class="codeph"> -1</span>将预加载集中的所有帧。 预加载的帧始终以初始加载“旋转视图”的原始分辨率显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">高分辨率</span></span> </p> </td> 
   <td colname="col2"> <p> 控制预加载帧的质量。 当设置为<span class="codeph">时，1</span>帧以高质量加载，与组件的大小匹配。 当设置为<span class="codeph"> 0</span>时，将只加载低分辨率预览拼贴。 </p> <p>以高分辨率预载可改善最终用户体验，尤其是在启用自动旋转的情况下。 同时，它也会导致启动时间变慢，网络消耗量增加，因此请谨慎使用。 当使用高分辨率预加载时，预加载的帧始终为组件最初加载时的原始分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
