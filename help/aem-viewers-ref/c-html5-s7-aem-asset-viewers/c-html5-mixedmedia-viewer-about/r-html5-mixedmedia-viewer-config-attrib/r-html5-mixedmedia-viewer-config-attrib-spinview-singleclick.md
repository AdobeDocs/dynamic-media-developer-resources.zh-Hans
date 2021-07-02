---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: 18c5c21d-af31-4b1c-ab8b-c04d08650123
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 无|缩放|重置|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 配置单击/点按以缩放操作的映射。将设置为<span class="codeph">无</span>会禁用单击/点按缩放。 如果设置为<span class="codeph">缩放</span>，则单击图像会缩放一个缩放步骤；按住CTRL并单击可缩小一个缩放步骤。 将设置为<span class="codeph">重置</span>会导致单击图像以将缩放重置为初始旋转级别。 对于<span class="codeph"> zoomReset </span>，如果当前缩放因子达到或超过指定限制，则应用重置，否则应用缩放。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` 台式计算机上； `none` 在触控设备上。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
