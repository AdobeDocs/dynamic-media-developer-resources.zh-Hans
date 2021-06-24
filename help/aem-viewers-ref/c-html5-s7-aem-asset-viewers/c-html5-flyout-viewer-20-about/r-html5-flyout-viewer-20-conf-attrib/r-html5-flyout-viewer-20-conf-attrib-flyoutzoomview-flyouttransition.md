---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: Developer,Business Practitioner
exl-id: a15723fe-a8be-49c5-bad3-1a1360eeb232
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 无|幻灯片|渐隐  </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏弹出视图时应用的效果类型。 当<span class="codeph">无</span>时，弹出图像在激活并准备就绪后即时显示；<span class="codeph">幻灯片</span>使幻灯片动画以从左到右的方向播放；<span class="codeph">渐隐</span>对弹出图像应用Alpha过渡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> 节目动画完成所用的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay  </span> </span> </p> </td> 
   <td colname="col2"> <p> 启动节目动画的用户操作与节目动画本身的开始之间的延迟（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime  </span> </span> </p> </td> 
   <td colname="col2"> <p> 隐藏动画完成所用的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 隐藏延迟  </span> </span> </p> </td> 
   <td colname="col2"> <p> 启动隐藏动画的用户操作与隐藏动画本身的开始之间的延迟（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
