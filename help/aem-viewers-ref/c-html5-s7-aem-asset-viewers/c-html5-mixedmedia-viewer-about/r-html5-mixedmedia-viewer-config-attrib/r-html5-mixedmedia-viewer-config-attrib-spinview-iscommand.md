---
description: SpinView.iscommand
solution: Experience Manager
title: SpinView.iscommand
topic: Dynamic Media
uuid: e2c86ec3-0f8a-42eb-98a1-689f083fa20c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---


# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> 应用于旋转图像的图像服务命令字符串。 如果在URL中指定，则所有<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的匹配项必须分别以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>的形式进行HTTP编码。 </p> <p> <p>注意： 不支持图像大小调整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

无。

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

当在查看器URL中指定时：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
