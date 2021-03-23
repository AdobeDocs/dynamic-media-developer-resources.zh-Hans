---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
uuid: 676a13b5-4634-4233-8059-6effed6e2b5d
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置多次单击/点按以缩放操作的映射。 设置为<span class="codeph">无</span>将禁用多次单击/点按缩放。 如果设置为<span class="codeph">缩放</span>，则单击图像将放大一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 设置为<span class="codeph"> reset </span>会导致单击图像将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用reset，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-50bcd15223174bb79ce08b31ea03d682}

可选。

## 默认 {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` 在台式计算机上； `zoomReset` 触控设备。

## 示例 {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom`
