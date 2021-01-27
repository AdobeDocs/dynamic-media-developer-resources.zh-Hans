---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic Media
uuid: 0b94956d-9ee6-409e-9b52-29c888932a0e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 无|幻灯片|淡入淡出  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏弹出视图时应用的效果的类型。 当<span class="codeph">没有</span>时，弹出图像在激活并准备就绪后立即显示；<span class="codeph">幻灯片</span>使幻灯片动画以从左到右的方向播放；<span class="codeph"> fade </span>对弹出图像应用alpha过渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> 完成显示动画所需的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 显示延迟  </span> </span> </p> </td> 
   <td colname="col2"> <p> 启动显示动画的用户操作与显示动画本身的开始之间的延迟时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 藏时  </span> </span> </p> </td> 
   <td colname="col2"> <p> 隐藏动画完成所需的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 隐藏延迟  </span> </span> </p> </td> 
   <td colname="col2"> <p> 启动隐藏动画的用户操作与隐藏动画本身开始之间的延迟时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
