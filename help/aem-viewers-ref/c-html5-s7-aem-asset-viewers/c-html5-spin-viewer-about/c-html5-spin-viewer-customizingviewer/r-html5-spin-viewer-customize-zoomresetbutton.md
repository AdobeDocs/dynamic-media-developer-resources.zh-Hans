---
description: 单击或点按此按钮会重置主视图中的图像。 您可以使用CSS调整按钮的大小、外观和位置。
solution: Experience Manager
title: 缩放重置按钮
feature: Dynamic Media Classic，查看器，SDK/API，旋转集
role: Developer,User
exl-id: fce8ab8a-4db0-4902-8e82-26f201a88dbe
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 3%

---

# 缩放重置按钮{#zoom-reset-button}

单击或点按此按钮会重置主视图中的图像。 您可以使用CSS调整按钮的大小、外观和位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

通过以下CSS类选择器控制按钮的外观：

```
.s7spinviewer .s7zoomresetbutton
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从上边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从右边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>从左边框开始的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从下边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，该选择器可用于将不同的外观应用到不同的按钮状态。

按钮工具提示可进行本地化。 有关更多信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98) 。

示例 — 要设置一个32 x 32像素的缩放重置按钮，该按钮位于查看器的上边缘和右边缘的6个像素处，并针对四个不同按钮状态中的每个状态显示一个不同的图像。

```
.s7spinviewer .s7zoomresetbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7spinviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7spinviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7spinviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7spinviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```
