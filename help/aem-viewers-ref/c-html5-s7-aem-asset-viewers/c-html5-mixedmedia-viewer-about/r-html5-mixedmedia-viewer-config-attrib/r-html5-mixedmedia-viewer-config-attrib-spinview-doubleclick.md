---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置双击/点按到旋转操作的映射。 设置为<span class="codeph">无</span>可禁用双击/点按旋转。 如果设置为<span class="codeph">缩放</span>，则单击图像将旋转一个旋转步骤；按住CTRL键单击可旋转一个旋转步骤。 设置为<span class="codeph">重置</span>会导致单击图像以将旋转重置为初始旋转级别。 对于<span class="codeph"> zoomReset </span>，如果当前旋转因子达到或超过指定限制，则应用重置，否则应用旋转。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset`在桌面计算机上；`zoomReset`在触控设备上。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
