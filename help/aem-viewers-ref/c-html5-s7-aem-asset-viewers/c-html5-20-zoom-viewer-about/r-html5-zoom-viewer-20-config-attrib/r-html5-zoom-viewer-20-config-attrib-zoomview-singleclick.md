---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.singlick
solution: Experience Manager
title: ZoomView.singlick
topic: Dynamic media
uuid: 919dd48e-b621-4dbb-9cae-f2d0f91f45a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.singlick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置单击／点按缩放操作的映射。设置为“ <span class="codeph"> 无” </span> 将禁用单击／点按缩放功能。 如果设置为缩 <span class="codeph"> 放， </span> 单击图像将放大一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 设置为 <span class="codeph"> 重置 </span> 会导致单击图像将缩放重置为初始缩放级别。 对于 <span class="codeph"> 缩放重 </span>置，如果当前缩放因子达到或超过指定限制，则应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选。

## 默认 {#section-71fb773f814649b2885aefee68073641}

`zoomReset` 在台式计算机上；触 `none` 控设备。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
