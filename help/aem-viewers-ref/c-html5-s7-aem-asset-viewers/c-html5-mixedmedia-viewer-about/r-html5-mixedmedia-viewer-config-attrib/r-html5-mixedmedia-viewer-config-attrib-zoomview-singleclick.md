---
description: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic Media
uuid: 3e57e235-7888-4ba2-9c8e-4f568a6caa52
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|缩放重置  </span> </p> </td> 
   <td colname="col2"> <p> 配置单击／点按缩放操作的映射。设置为<span class="codeph">无</span>将禁用单击／点按缩放。 如果设置为<span class="codeph">缩放</span>单击图像，则会放大一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为<span class="codeph"> reset </span>会导致单击图像将缩放重置为初始缩放级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用reset，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` 在台式计算机上； `none` 触控设备。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
