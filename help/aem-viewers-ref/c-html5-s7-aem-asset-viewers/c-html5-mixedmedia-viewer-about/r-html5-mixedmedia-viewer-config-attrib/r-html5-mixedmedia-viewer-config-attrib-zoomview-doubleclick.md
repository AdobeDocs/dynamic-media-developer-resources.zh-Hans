---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
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

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 在台式计算机上； `zoomReset` 触控设备。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
