---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic Media
uuid: a9928350-d9a9-49b0-8990-1f8b67d82f10
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 应用于所有色板的图像服务命令字符串。 如果在URL中指定了该属性，请确保对<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有匹配项进行HTTP编码，分别作为<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> <p> <p>注意： 不支持图像大小调整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

无。

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

当在查看器URL中指定时：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
