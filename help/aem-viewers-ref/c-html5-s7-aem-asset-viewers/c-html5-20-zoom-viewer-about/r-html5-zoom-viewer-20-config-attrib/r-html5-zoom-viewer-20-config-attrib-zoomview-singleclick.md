---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3fd5b907-faf6-4d36-8ee1-79f3ace781d4
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按以缩放操作的映射。 将设置为 <span class="codeph"> 无 </span> 禁用单击/点按缩放。 如果设置为 <span class="codeph"> 缩放 </span> 单击图像可放大一个缩放步长；按住CTRL键并单击可缩小一个缩放步长。 将设置为 <span class="codeph"> 重置 </span> 单击图像可将缩放重置为初始缩放级别。 对象 <span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则会应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`zoomReset`  — 台式计算机； `none` 在触控设备上。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
