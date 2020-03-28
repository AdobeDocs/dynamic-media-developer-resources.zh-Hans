---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
topic: Dynamic media
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|fade </span></span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏弹出视图时应用的效果的类型。 如果 <span class="codeph"> 没有 </span>弹出图像，则激活后弹出图像会立即显示；滑 <span class="codeph"> 动 </span> 使幻灯片动画按从左到右的方向播放；淡 <span class="codeph"> 入淡 </span> 出将alpha过渡应用于弹出图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 观看时 </span> 间 </span> </p> </td> 
   <td colname="col2"> <p> 完成显示动画所需的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 显示延迟 </span></span> </p> </td> 
   <td colname="col2"> <p> 启动显示动画的用户操作与显示动画本身的开始之间的延迟时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidetime </span></span> </p> </td> 
   <td colname="col2"> <p> 隐藏动画完成所需的秒数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> hidedelay </span></span> </p> </td> 
   <td colname="col2"> <p> 启动隐藏动画的用户操作与隐藏动画本身的开始之间的延迟时间（以秒为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
