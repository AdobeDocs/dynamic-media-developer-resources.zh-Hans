---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 03a04bba-85ae-4c30-91fa-dfc6b732a9ac
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`持续时间`*[, *`计数`*][, *`渐隐`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">持续时间</span></span> </p> </td> 
   <td colname="col2"> <p> 指定提示文本在隐藏之前显示的秒数。 当设置为<span class="codeph"> -1</span>时，即使用户激活弹出窗口，也会始终显示消息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">计数</span></span> </p> </td> 
   <td colname="col2"> <p> 指定查看集中的新图像时文本显示的次数。 值为<span class="codeph"> -1</span>表示在查看集中的任何图像时始终显示文本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">淡化</span></span> </p> </td> 
   <td colname="col2"> 指定文本出现或消失时出现的渐隐动画的持续时间。 值为<span class="codeph"> 0</span>表示无渐隐过渡。 </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`3,1,0.3`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`tip=1,-1,0`
