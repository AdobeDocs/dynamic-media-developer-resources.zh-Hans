---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`持续时间`*[, *`间距`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|渐隐|幻灯片 </span> </p> </td> 
   <td colname="col2"> <p>指定对帧更改应用的效果的类型。 属性 <span class="codeph"> 无 </span> 表示无过渡；帧更改会立即发生。 属性 <span class="codeph"> 渐隐 </span> 表示旧帧和新帧之间的交叉淡入淡出过渡。 属性 <span class="codeph"> 幻灯片 </span> 激活旧框架滑出视图和新框架滑入的过渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 持续时间 </span> </span> </p> </td> 
   <td colname="col2"> <p>指定以下内容的持续时间（以秒为单位）： <span class="codeph"> 渐隐 </span> 或 <span class="codeph"> 幻灯片 </span> 过渡效果。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 间距 </span> </span> </p> </td> 
   <td colname="col2"> <p>中相邻帧之间的间距 <span class="codeph"> 幻灯片 </span> 过渡，范围为 <span class="codeph"> 0 </span> 到 <span class="codeph"> 1 </span> 和相对于组件的宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
