---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按缩放操作的映射。设置为<span class="codeph">无</span>将禁用单击/点按缩放。 如果设置为<span class="codeph">旋转</span>，则单击图像将放大一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 设置为<span class="codeph"> reset </span>会导致单击图像将缩放重置为初始旋转级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用reset，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-924163cb2f6542499f49894becef7fb5}

可选。

## 默认 {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` 在台式计算机上； `none` 触控设备。

## 示例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
