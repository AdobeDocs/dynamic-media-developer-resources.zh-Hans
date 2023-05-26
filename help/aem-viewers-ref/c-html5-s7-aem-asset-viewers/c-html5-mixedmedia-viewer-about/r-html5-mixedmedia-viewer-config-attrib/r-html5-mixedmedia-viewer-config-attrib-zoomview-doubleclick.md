---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置双击/点按以缩放操作的映射。 将设置为 <span class="codeph"> 无 </span> 禁用双击/点按缩放。 如果设置为 <span class="codeph"> 缩放 </span> 单击图像可放大一个缩放步长；按住CTRL键并单击可缩小一个缩放步长。 将设置为 <span class="codeph"> 重置 </span> 单击图像可将缩放重置为初始缩放级别。 对象 <span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则会应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` 在台式计算机上； `zoomReset` 在触控设备上。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
