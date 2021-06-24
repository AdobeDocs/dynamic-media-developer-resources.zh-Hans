---
description: Twitter共享工具由添加到Social共享面板的按钮组成。 单击按钮后，用户将被重定向到由社交服务提供的共享对话框。 按钮的位置完全由Social共享工具管理。
solution: Experience Manager
title: Twitter份额
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,Business Practitioner
exl-id: a90a4c82-b51a-4fb0-9196-44ae4ba8e0cd
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# Twitter份额{#twitter-share}

Twitter共享工具由添加到Social共享面板的按钮组成。 单击按钮后，用户将被重定向到由社交服务提供的共享对话框。 按钮的位置完全由Social共享工具管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

通过以下CSS类选择器控制Twitter共享按钮的外观：

```
.s7video360viewer .s7twittershare
```

**twitter共享工具的CSS属性**

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
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，该选择器可用于将不同的外观应用到不同的按钮状态。

可以通过在Social共享面板的CSS类中设置`display:none` CSS属性，从该面板中删除该按钮。

按钮工具提示可进行本地化。 请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

**示例**  — 要设置一个28 x 28像素的Twitter共享按钮，并针对四个不同按钮状态中的每个状态显示一个不同的图像，请执行以下操作：

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
