---
title: Video360Player.iconeffect
description: Video360 Viewer的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 7%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Video360 Viewer的配置属性。

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`count`*][, *`渐隐`*][, *`自动隐藏`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 当视频处于暂停状态时，在视频的顶部显示IconEffect。 在某些设备上，使用本机控件。 在这种情况下， <span class="codeph">iconeffect</span> 修饰符将被忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出现和重新出现的最大次数。 值 <span class="codeph"> -1</span> 表示图标会无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 渐隐</span></span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 自动隐藏</span></span> </p> </td> 
   <td colname="col2"> <p> 设置IconEffect在自动隐藏之前保持完全可见的秒数。 即，淡入动画完成之后和淡出动画开始之前的时间。 设置为 <span class="codeph"> 0</span> 禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
