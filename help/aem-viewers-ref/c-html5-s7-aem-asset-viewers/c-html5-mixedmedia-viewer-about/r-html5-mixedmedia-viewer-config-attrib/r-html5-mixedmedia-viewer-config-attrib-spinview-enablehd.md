---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 6%

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`数字`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 总是|never|limit</span> </p> </td> 
   <td colname="col2"> <p> 对于<span class="codeph"> devicePixelRatio</span>大于<span class="codeph"> 1</span>的设备，即具有高密度显示屏（如iPhone4和类似设备）的设备，启用、限制或禁用优化。 如果处于活动状态，则组件会限制IS图像请求的大小，就像设备仅具有<span class="codeph"> 1</span>的像素比一样，从而减少带宽。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数字</span></span> </p> </td> 
   <td colname="col2"> <p> 如果使用<span class="codeph"> limit</span>设置，则组件仅启用高像素密度（高于指定限制）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
