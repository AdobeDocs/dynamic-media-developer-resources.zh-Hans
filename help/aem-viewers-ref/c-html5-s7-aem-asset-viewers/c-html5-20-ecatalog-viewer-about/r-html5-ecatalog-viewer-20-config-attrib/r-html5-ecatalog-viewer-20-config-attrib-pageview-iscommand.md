---
description: 'null'
seo-description: 'null'
seo-title: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
topic: Dynamic media
uuid: 6c853c6a-a57d-4cab-ad71-74baf9e870d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.iscommand{#pageview-iscommand}

` [PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 应用于页面图像的图像服务命令字符串。 如果在URL中指定，则&amp;和 <span class="codeph"> =的所有出现都必须以HTTP编码，分别为</span> %26 <span class="codeph"> 和</span><span class="codeph"></span><span class="codeph"></span>%3D Exconded。 </p> <p> <p>注意： 不支持图像大小调整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-df5a0604766b4ac2b9a6742b377e427c}

可选。

## 默认 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

无。

## 示例 {#section-813de2905d6c44c0991cfe0931581462}

在查看器URL中指定时。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
