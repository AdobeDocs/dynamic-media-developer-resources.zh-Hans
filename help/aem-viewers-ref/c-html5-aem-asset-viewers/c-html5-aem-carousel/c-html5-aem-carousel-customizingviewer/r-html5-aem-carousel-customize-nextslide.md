---
description: 单击或点按“下一张”幻灯片按钮可将用户移动到旋转集中的下一张幻灯片。
seo-description: 单击或点按“下一张”幻灯片按钮可将用户移动到旋转集中的下一张幻灯片。
seo-title: 下一张幻灯片
solution: Experience Manager
title: 下一张幻灯片
topic: Dynamic Media
uuid: 6cf7a16c-42bf-4576-bcb1-d504589b2748
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---


# 下一张幻灯片{#next-slide}

单击或点按“下一张”幻灯片按钮可将用户移动到旋转集中的下一张幻灯片。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

此按钮不显示在触控设备上。 您可以使用CSS调整此按钮的大小、外观和位置。

**主查看器区域的CSS属性**

按钮的外观由以下CSS类选择器控制：

`.s7carouselviewer .s7panrightbutton`

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
   <td colname="col2"> <p>从查看器边框顶部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从查看器边框的右侧定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>从查看器左侧的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从查看器边框底部定位。 </p> </td> 
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
   <td colname="col2"> <p> 在图稿Sprite中放置位置（如果使用CSS Sprite）。 </p> <p>另请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 光标  </span> </p> </td> 
   <td colname="col2"> <p>光标类型。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md)。

示例——设置上一个60 x 60像素的幻灯片按钮，该按钮距右侧查看器边框和垂直居中放置10像素，并针对四个不同按钮状态中的每个状态显示不同的图像。

```
.s7carouselviewer .s7panrightbutton{ 
 bottom: 50%; 
 right: 10px; 
 background-size:60px; 
 cursor: pointer; 
 } 
.s7carouselviewer.s7mouseinput .s7panrightbutton { 
 width:60px; 
 height:60px; 
 margin-bottom: -20px; 
} 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state]  { 
    background-image: url(../../viewers/s7viewers/html5/images/v2/CarouselDotsRightButton_dark_sprite.png); 
} 
 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='up'] { background-position: -0px -60px;  } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='over'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='down'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='disabled'] { background-position: -0px -60px; }
```

