---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置双击/点按旋转操作的映射。 将设置为<span class="codeph">无</span>会禁用双击/点按旋转。 如果设置为<span class="codeph">缩放</span> ，则单击图像会在一个旋转步骤中旋转；CTRL+单击可旋转一个旋转步骤。 将设置为<span class="codeph">重置</span>会导致单击图像以将旋转重置为初始旋转级别。 对于<span class="codeph"> zoomReset </span>，如果当前旋转因子达到或超出指定限制，则应用重置，否则应用旋转。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 台式计算机上； `zoomReset` 在触控设备上。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
