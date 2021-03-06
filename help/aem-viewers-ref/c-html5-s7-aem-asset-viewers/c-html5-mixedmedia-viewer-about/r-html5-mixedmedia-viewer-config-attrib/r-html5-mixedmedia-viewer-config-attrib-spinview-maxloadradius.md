---
title: SpinView.maxloadradius
description: 表示在SpinView空闲时，要在每个方向上预载的帧数上限。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e64fcd95-9660-4c1f-91b2-3ffc5a7493ce
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---

# SpinView.maxloadradius{#spinview-maxloadradius}

表示在SpinView空闲时，要在每个方向上预载的帧数上限。

` [SpinView.|<containerId>_spinView.]maxloadradius= *`值`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 值</span></span> </p> </td> 
   <td colname="col2"> <p> 值 <span class="codeph"> -1</span> 预加载集中的所有帧。 预加载的帧始终以最初加载SpinView的原始分辨率显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> 控制预加载帧的质量。 </p> <p>当设置为 <span class="codeph"> 1</span> 帧以高质量加载，与组件的大小匹配。 </p> <p>当设置为 <span class="codeph"> 0</span> 仅加载低分辨率预览拼贴。</p> <p>以高分辨率预加载可改善用户的体验，尤其是在启用了自动旋转的情况下。 同时，启动时间较慢，网络消耗较高，因此应谨慎使用。 使用高分辨率预加载时，预加载的帧始终处于最初加载组件的原始分辨率。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
