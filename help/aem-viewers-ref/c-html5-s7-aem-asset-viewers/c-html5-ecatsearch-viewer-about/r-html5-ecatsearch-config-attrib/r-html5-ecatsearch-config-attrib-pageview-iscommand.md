---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
uuid: 32bfd041-e44c-4a78-a923-896a85d8f75f
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 应用于页面图像的图像服务命令字符串。 如果在URL中指定了<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有匹配项，则必须分别以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>的形式进行HTTP编码。 </p> <p> <p>注意： 不支持图像大小调整操作命令。 </p> </p> </td> 
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
