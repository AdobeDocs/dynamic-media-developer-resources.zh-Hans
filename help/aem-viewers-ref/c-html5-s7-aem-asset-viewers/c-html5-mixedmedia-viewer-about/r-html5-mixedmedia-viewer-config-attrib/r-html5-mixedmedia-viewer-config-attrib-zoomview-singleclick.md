---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0fcc1f5c-a735-430d-be0c-c00ed08830df
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按以缩放操作的映射。将设置为 <span class="codeph"> 无 </span> 禁用单击/点按缩放。 如果设置为 <span class="codeph"> 缩放 </span> 单击图像会缩放一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为 <span class="codeph"> 重置 </span> 会导致单击图像将缩放重置为初始缩放级别。 对于 <span class="codeph"> zoomReset </span>，则当前缩放因子达到或超过指定限制时，会应用重置，否则会应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` 台式计算机上； `none` 在触控设备上。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
