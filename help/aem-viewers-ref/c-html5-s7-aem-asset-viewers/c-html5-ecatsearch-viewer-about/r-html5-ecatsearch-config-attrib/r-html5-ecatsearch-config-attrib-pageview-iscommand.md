---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fd1fa0f2-d666-4470-8b5b-673f3c4327e0
TQID: 'https://experienceleague.adobe.com/km9mFC3Fv0PTD04iE-CF2mhfPmYvqoPaFZOO4j7Ml98'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 59
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

