---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: e375f3ec-82f3-441d-9e01-d0ea5605bd25
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 应用于所有样本的图像服务命令字符串。 如果在URL中指定，请确保对<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有匹配项进行HTTP编码，分别表示<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> <p> <p>注意：不支持图像大小调整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

在查看器URL中指定时。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
