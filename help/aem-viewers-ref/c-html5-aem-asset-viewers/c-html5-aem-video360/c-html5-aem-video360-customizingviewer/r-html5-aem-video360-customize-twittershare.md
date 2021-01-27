---
description: Twitter共享工具由添加到“社交共享”面板的按钮组成。 单击按钮时，用户将被重定向到由社交服务提供的共享对话框。 按钮的位置完全由社交共享工具管理。
seo-description: Twitter共享工具由添加到“社交共享”面板的按钮组成。 单击按钮时，用户将被重定向到由社交服务提供的共享对话框。 按钮的位置完全由社交共享工具管理。
seo-title: Twitter共享
solution: Experience Manager
title: Twitter共享
topic: Dynamic Media
uuid: c16ce881-e5d5-4864-bfad-69b4c9b51a21
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Twitter共享{#twitter-share}

Twitter共享工具由添加到“社交共享”面板的按钮组成。 单击按钮时，用户将被重定向到由社交服务提供的共享对话框。 按钮的位置完全由社交共享工具管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Twitter共享按钮的外观由以下CSS类选择器控制：

```
.s7video360viewer .s7twittershare
```

**Twitter共享工具的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置位置（如果使用CSS Sprite）。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

通过设置其CSS类的`display:none` CSS属性，可以从“社交共享”面板中删除该按钮。

按钮工具提示可以本地化。 请参阅[用户界面元素本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

**示例** -设置一个28 x 28像素的Twitter共享按钮，并为四个不同按钮状态中的每个状态显示一个不同的图像：

```
.s7video360viewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7video360viewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7video360viewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7video360viewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```

