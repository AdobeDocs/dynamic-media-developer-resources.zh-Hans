---
description: SearchPanel.iscommand
solution: Experience Manager
title: SearchPanel.iscommand
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,Business Practitioner
exl-id: 4e843866-75a5-4543-a275-e134b3aee75a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---

# SearchPanel.iscommand{#searchpanel-iscommand}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 应用于所有缩略图的图像提供命令字符串。 如果在URL中指定了<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有实例，则必须分别以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>的形式进行HTTP编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-df5a0604766b4ac2b9a6742b377e427c}

可选。

## 默认 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

无。

## 示例 {#section-813de2905d6c44c0991cfe0931581462}

在查看器URL中指定时。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

在配置数据中指定时。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
