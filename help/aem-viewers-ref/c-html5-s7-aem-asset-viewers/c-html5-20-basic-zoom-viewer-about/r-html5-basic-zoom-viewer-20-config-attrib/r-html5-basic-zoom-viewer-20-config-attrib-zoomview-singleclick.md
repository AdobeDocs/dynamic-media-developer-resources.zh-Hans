---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: Developer,User
exl-id: c2292b5b-5b4e-4368-9495-9108042ec2f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按以缩放操作的映射。将设置为<span class="codeph">无</span>会禁用单击/点按缩放。 如果设置为<span class="codeph">缩放</span>，则单击图像会缩放一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为<span class="codeph">重置</span>会导致单击图像，将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-50bcd15223174bb79ce08b31ea03d682}

可选。

## 默认 {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` 台式计算机上； `none` 在触控设备上。

## 示例 {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom`
