---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置双击/点按到旋转操作的映射。 设置为<span class="codeph">无</span>可禁用双击/点按旋转。 如果设置为<span class="codeph">缩放</span>，则单击图像将旋转一个旋转步骤；按住CTRL键单击可旋转一个旋转步骤。 设置为<span class="codeph">重置</span>会导致单击图像以将旋转重置为初始旋转级别。 对于<span class="codeph"> zoomReset </span>，如果当前旋转因子达到或超过指定限制，则应用重置，否则应用旋转。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选.

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

桌面计算机上的`reset`；触控设备上的`zoomReset`。

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
