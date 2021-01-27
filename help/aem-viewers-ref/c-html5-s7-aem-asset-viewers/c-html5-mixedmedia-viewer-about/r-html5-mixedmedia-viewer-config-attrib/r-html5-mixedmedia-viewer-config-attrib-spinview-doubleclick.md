---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic Media
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|缩放重置  </span> </p> </td> 
   <td colname="col2"> <p> 配置多次单击／点按旋转操作的映射。 设置为<span class="codeph">无</span>将禁用多次单击／点按旋转。 如果设置为<span class="codeph">缩放</span>，则单击图像在一个旋转步骤中旋转；按住CTRL并单击可旋转一个旋转步骤。 将设置为<span class="codeph"> reset </span>将导致单击图像将旋转重置为初始旋转级别。 对于<span class="codeph"> zoomReset </span>，如果当前旋转系数达到或超过指定的限制，则应用reset，否则应用旋转。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 在台式计算机上； `zoomReset` 触控设备。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
