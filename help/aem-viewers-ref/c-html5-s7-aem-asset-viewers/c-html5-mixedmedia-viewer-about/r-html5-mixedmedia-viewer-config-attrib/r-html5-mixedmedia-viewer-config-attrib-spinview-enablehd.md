---
title: SpinView.enableHD
description: SpinView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '83'
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
