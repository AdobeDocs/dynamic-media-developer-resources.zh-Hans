---
description: 'null'
seo-description: 'null'
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置多次单击／点按旋转操作的映射。 设置为“ <span class="codeph"> 无” </span> 将禁用多次单击／点按旋转。 如果设置为缩 <span class="codeph"> 放， </span> 单击图像将在一个旋转步骤中旋转；CTRL+单击可旋转一个旋转步骤。 设置为 <span class="codeph"> 重置 </span> 会导致单击图像将旋转重置为初始旋转级别。 对于 <span class="codeph"> zoomReset </span>，如果当前旋转因子达到或超过指定的限制，则应用reset，否则应用旋转。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选。

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`reset` 在台式计算机上；触 `zoomReset` 控设备。

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
