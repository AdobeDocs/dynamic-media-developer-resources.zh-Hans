---
title: SpinView.maxloadradius
description: 表示当SpinView空闲时在每个方向预载的最大帧数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

表示当SpinView空闲时在每个方向预载的最大帧数。

` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">值</span></span> </p> </td> 
   <td colname="col2"> <p> 值为<span class="codeph"> -1</span>将预加载集中的所有帧。 预加载的帧始终以初始加载“旋转视图”的原始分辨率显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">高分辨率</span></span> </p> </td> 
   <td colname="col2"> <p> 控制预加载帧的质量。 </p> <p>当设置为<span class="codeph"> 1</span>时，帧以高质量加载，与组件的大小匹配。 </p> <p>当设置为<span class="codeph"> 0</span>时，将只加载低分辨率预览拼贴。</p> <p>以高分辨率预载可改善用户体验，尤其是在启用了自动旋转的情况下。 同时，由于它的启动时间较慢，网络消耗较大，所以使用时应该小心。 当使用高分辨率预加载时，预加载的帧始终为最初加载组件时的原始分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
