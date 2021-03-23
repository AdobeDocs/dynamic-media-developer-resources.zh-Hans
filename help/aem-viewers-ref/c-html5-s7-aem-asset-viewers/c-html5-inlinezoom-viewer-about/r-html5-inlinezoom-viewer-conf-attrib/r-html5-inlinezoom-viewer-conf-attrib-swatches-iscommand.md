---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
uuid: a7d3b93b-daa2-4d08-8e2f-52e3ea11efbd
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> 应用于所有色板的图像服务命令字符串。 如果在URL中指定，请确保将<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有匹配项HTTP编码为<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> <p> <p>注意： 不支持图像大小调整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-e6310c8c4e8547689a5b48ceddb3671d}

可选。

## 默认 {#section-fcb06fd8e7e945e590094efcf9a1d510}

无。

## 示例 {#section-3a188ab955c445bcb2efa3c49722c10d}

在查看器URL中指定时。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
