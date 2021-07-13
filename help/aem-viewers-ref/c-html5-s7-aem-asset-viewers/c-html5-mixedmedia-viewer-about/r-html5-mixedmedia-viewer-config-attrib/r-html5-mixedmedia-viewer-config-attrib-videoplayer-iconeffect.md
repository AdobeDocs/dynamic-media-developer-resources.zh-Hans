---
description: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,User
exl-id: 8371cb69-4cd9-457b-bd8c-e4167fc67600
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> 在视频暂停时，使IconEffect能够显示在视频顶部。 在某些设备上，使用本机控件。 在这种情况下，将忽略<span class="codeph"> iconeffect</span>修饰符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 计数</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定IconEffect出现和重新出现的最大次数。 值<span class="codeph"> -1</span>表示该图标无限期地重新显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 淡淡</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定显示或隐藏动画的持续时间（以秒为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> 设置IconEffect在自动隐藏之前保持可见的秒数。 即，淡入动画完成后和淡出动画开始前的时间。 设置<span class="codeph"> 0</span>会禁用自动隐藏行为。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
