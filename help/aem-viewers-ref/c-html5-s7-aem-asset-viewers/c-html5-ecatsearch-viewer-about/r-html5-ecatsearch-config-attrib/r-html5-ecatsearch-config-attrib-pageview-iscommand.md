---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fd1fa0f2-d666-4470-8b5b-673f3c4327e0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 6%

---

# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 应用于页面图像的图像服务命令字符串。 如果在URL中指定，则<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有匹配项必须通过HTTP编码分别表示为<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> <p> <p>注意：不支持图像大小调整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-df5a0604766b4ac2b9a6742b377e427c}

可选.

## 默认 {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

无。

## 示例 {#section-813de2905d6c44c0991cfe0931581462}

在查看器URL中指定时。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

在配置数据中指定时。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
