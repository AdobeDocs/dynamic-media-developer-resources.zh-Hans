---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic media
uuid: 42bbef39-36b6-4f1d-a228-0aaf107600a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持续`*[, *``*][, *`时间`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 持 <span class="varname"> 续时间</span></span> </p> </td> 
   <td colname="col2"> <p>指定提示文本在隐藏前显示的秒数。 设置为-1 <span class="codeph"> 时</span>，即使用户激活弹出窗口，消息也始终显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p>指定查看集合中的新图像时显示文本的次数。 值为 <span class="codeph"> -1表示</span> ，查看集合中的任何图像时，始终显示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡入淡出</span></span> </p> </td> 
   <td colname="col2"> <p>指定文本出现或消失时出现的淡入淡出动画的持续时间。 值为 <span class="codeph"> 0表示</span> ，无淡入淡出过渡。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
