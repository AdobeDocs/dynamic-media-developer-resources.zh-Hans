---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic media
uuid: 16a0ca99-1ed5-4f1d-b068-55adc46fde0b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持续`*[, *``*][, *`时间`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 时段</span></span> </p> </td> 
   <td colname="col2"> <p> 指定提示文本在隐藏前显示的秒数。 设置为-1 <span class="codeph"> 时</span>，即使用户激活弹出窗口，消息也始终显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定查看集合中的新图像时显示文本的次数。 值为 <span class="codeph"> -1表示</span> ，查看集合中的任何图像时，始终显示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 淡出</span></span> </p> </td> 
   <td colname="col2"> 指定文本出现或消失时出现的淡入淡出动画的持续时间。 值为0表示 <span class="codeph"></span> 没有淡入淡出过渡。 </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
