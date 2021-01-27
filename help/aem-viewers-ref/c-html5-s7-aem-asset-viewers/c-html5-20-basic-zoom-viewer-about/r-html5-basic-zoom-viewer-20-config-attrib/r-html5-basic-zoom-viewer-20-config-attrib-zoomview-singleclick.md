---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic Media
uuid: 42327f03-269b-4d4e-a35d-2537ca3ba071
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|缩放重置  </span> </p> </td> 
   <td colname="col2"> <p> 配置单击／点按缩放操作的映射。设置为<span class="codeph">无</span>将禁用单击／点按缩放。 如果设置为<span class="codeph">缩放</span>单击图像，则会放大一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为<span class="codeph"> reset </span>会导致单击图像将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用reset，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-50bcd15223174bb79ce08b31ea03d682}

可选。

## 默认 {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` 在台式计算机上； `none` 触控设备。

## 示例 {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
