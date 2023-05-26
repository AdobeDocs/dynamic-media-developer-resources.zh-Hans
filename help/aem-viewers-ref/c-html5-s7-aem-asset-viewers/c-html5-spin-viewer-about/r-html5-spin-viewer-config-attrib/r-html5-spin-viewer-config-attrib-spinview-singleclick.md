---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按以缩放操作的映射。 将设置为 <span class="codeph"> 无 </span> 禁用单击/点按缩放。 如果设置为 <span class="codeph"> 旋转 </span> 单击图像可放大一个缩放步长；按住CTRL键并单击可缩小一个缩放步长。 将设置为 <span class="codeph"> 重置 </span> 单击图像可将缩放重置为初始旋转级别。 对象 <span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则会应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` 在台式计算机上； `none` 在触控设备上。

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
