---
description: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 表示当SpinView空闲时，要在每个方向预载的最大帧数。 值<span class="codeph"> -1</span>预加载集中的所有帧。 预加载的帧始终以SpinView最初加载的原始分辨率显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 控制预加载帧的质量。 当设置为<span class="codeph"> 1</span>帧时，以高质量加载帧，与组件的大小匹配。 设置为<span class="codeph"> 0</span>时，仅加载低分辨率预览拼贴。 </p> <p>以高分辨率预加载可改善最终用户体验，尤其是在启用自动旋转时。 同时，这会导致开始时间更短，网络消耗更高，因此请谨慎使用。 使用高分辨率预载时，预加载的帧始终以组件最初加载时的原始分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选。

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
