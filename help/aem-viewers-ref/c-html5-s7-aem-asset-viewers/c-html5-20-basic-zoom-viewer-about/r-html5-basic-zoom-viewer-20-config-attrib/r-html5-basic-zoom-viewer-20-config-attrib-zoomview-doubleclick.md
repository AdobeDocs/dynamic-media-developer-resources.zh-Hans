---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 38c90d7f-ddbc-4123-b90d-02f9cabd785c
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置双击/点按以缩放操作的映射。 将设置为 <span class="codeph"> 无 </span> 禁用双击/点按缩放。 如果设置为 <span class="codeph"> 缩放 </span> 单击图像可放大一个缩放步长；按住CTRL键并单击可缩小一个缩放步长。 将设置为 <span class="codeph"> 重置 </span> 单击图像可将缩放重置为初始缩放级别。 对象 <span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则会应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-50bcd15223174bb79ce08b31ea03d682}

可选.

## 默认 {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` 在台式计算机上； `zoomReset` 在触控设备上。

## 示例 {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
