---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durationcountfade`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 指定提示文本在隐藏之前显示的秒数。 如果设置为<span class="codeph"> -1</span>，则始终会显示消息，即使用户激活弹出窗口也是如此。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定在查看集合中的新图像时显示文本的次数。 值<span class="codeph"> -1</span>表示在查看集合中的任何图像时始终显示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡淡</span></span> </p> </td> 
   <td colname="col2"> 指定文本出现或消失时出现的渐隐动画的持续时间。 值<span class="codeph"> 0</span>表示没有渐隐过渡。 </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
