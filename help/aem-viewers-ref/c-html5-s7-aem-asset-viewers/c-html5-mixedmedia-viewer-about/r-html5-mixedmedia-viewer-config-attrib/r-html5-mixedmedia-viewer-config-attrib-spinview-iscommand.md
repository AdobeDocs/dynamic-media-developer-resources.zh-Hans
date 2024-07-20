---
title: SpinView.iscommand
description: SpinView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: d616c8cf-6717-48f9-9926-1b37afe0e444
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> 应用于旋转图像的图像服务命令字符串。 如果在URL中指定，则<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有匹配项必须通过HTTP编码分别表示为<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> <p> <p>注意：不支持图像大小调整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选.

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

无。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

在查看器URL中指定时：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
