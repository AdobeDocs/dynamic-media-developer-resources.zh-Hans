---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9f52542e-398c-45a2-89ea-95c9aefbde3e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置双击/点按以缩放操作的映射。 将设置为 <span class="codeph"> 无 </span> 禁用双击/点按缩放。 如果设置为 <span class="codeph"> 缩放 </span> 单击图像会缩放一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为 <span class="codeph"> 重置 </span> 会导致单击图像将缩放重置为初始缩放级别。 对于 <span class="codeph"> zoomReset </span>，则当前缩放因子达到或超过指定限制时，会应用重置，否则会应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`reset`  — 在台式计算机上； `zoomReset` 在触控设备上。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`doubleclick=zoom`
