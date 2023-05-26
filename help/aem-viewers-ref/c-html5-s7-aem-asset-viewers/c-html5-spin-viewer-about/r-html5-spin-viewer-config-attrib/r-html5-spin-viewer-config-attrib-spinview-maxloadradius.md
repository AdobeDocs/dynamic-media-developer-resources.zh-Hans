---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *`值`*[, *`高分辨率`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 表示当SpinView空闲时，在每个方向预载的最大帧数。 值 <span class="codeph"> -1</span> 预载集中的所有帧。 预加载的帧始终以初始加载“旋转视图”的原始分辨率显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 高分辨率</span></span> </p> </td> 
   <td colname="col2"> <p> 控制预加载帧的质量。 当设置为 <span class="codeph"> 1</span> 帧以高品质加载，与组件的大小相匹配。 当设置为 <span class="codeph"> 0</span> 仅加载低分辨率预览拼贴。 </p> <p>以高分辨率预载可改善最终用户体验，尤其是在启用自动旋转的情况下。 同时，它会导致启动时间变慢和网络消耗增加，因此请谨慎使用。 当使用高分辨率预加载时，预加载的帧始终为组件最初加载时的原始分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
