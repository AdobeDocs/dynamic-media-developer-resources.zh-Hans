---
description: 表示当SpinView空闲时，要在每个方向预载的最大帧数。
seo-description: 表示当SpinView空闲时，要在每个方向预载的最大帧数。
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

表示当SpinView空闲时，要在每个方向预载的最大帧数。

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valuehighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 值<span class="codeph"> -1</span>预加载集中的所有帧。 预加载的帧始终以SpinView最初加载的原始分辨率显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 控制预加载帧的质量。 </p> <p>设置为<span class="codeph"> 1</span>时，帧将以高质量加载，与组件的大小匹配。 </p> <p>设置为<span class="codeph"> 0</span>时，仅加载低分辨率预览拼贴。 </p> <p>以高分辨率预加载可改善最终用户体验，尤其是在启用自动旋转时。 同时，开始时间较慢，网络消耗较高，应谨慎使用。 使用高分辨率预载时，预加载的帧始终以最初加载组件时的原始分辨率显示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
