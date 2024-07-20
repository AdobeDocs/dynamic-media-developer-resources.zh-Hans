---
title: FlyoutZoomView.flyouttransition
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 3199d4a3-4799-40a2-b0a5-0e1ee4744fbe
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *`显示时间`*[, *`显示延迟`*[, *`隐藏时间`*[, *`隐藏延迟`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">无|幻灯片|渐隐</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏弹出视图时应用的效果的类型。 使用<span class="codeph">无</span>，弹出图像在激活并准备就绪时立即显示；<span class="codeph">幻灯片</span>使幻灯片动画以从左到右的方向播放；<span class="codeph">渐隐</span>对弹出图像应用Alpha过渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">显示时间</span> </span> </p> </td> 
   <td colname="col2"> <p> 显示动画完成需要的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">显示延迟</span> </span> </p> </td> 
   <td colname="col2"> <p> 启动显示动画的用户操作和显示动画本身开始之间的延迟（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">隐藏时间</span> </span> </p> </td> 
   <td colname="col2"> <p> 隐藏动画完成需要的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">隐藏延迟</span> </span> </p> </td> 
   <td colname="col2"> <p> 启动隐藏动画的用户操作和隐藏动画本身开始之间的延迟（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选.

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
