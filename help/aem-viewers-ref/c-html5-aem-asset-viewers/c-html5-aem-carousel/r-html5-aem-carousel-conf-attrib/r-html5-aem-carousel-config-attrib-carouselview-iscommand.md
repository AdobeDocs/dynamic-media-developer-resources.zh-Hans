---
title: CarouselView.iscommand
description: CarouselView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 848eaed7-c150-4537-96a4-f2614162d58f
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 8%

---

# CarouselView.iscommand{#carouselview-iscommand}

` [CarouselView.|<containerId>_carouselView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand </span></span> </p> </td> 
   <td colname="col2"> <p> 应用于横幅图像的图像服务命令字符串。 如果在URL中指定，则所有匹配项 <span class="codeph"> 和</span> 和 <span class="codeph"> =</span> 必须为HTTP编码 <span class="codeph"> %26</span> 和 <span class="codeph"> %3D</span>，则不会显示任何内容。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

无。

## 示例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

在查看器URL中指定时：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
