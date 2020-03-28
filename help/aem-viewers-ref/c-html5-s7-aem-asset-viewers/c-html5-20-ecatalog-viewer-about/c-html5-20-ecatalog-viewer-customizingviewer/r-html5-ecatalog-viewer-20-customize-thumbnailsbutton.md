---
description: 单击或点按此按钮重置可在主视图和缩略图之间切换查看器。 此按钮显示在主控件栏中。 您可以使用CSS调整此按钮的大小、外观和位置。
seo-description: 单击或点按此按钮重置可在主视图和缩略图之间切换查看器。 此按钮显示在主控件栏中。 您可以使用CSS调整此按钮的大小、外观和位置。
seo-title: 缩览图按钮
solution: Experience Manager
title: 缩览图按钮
topic: Dynamic media
uuid: a1a7f4b0-672e-4b83-9b21-0b8c6fc3f24a
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 缩览图按钮{#thumbnails-button}

单击或点按此按钮重置可在主视图和缩略图之间切换查看器。 此按钮显示在主控件栏中。 您可以使用CSS调整此按钮的大小、外观和位置。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**主查看器区域的CSS属性**

按钮的外观由以下CSS类选择器控制：

`.s7ecatalogviewer .s7thumbnailpagebutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> 与控制栏顶部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 到左侧下一个按钮的距离；如果这是一行中的第一个按钮，则距控件栏左侧的距离。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p>为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中定位（如果使用CSS Sprite）。 </p> <p>另请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮同时支持 `state` 和属 `selected` 性选择器，这两个选择器可用于将不同的外观应用于不同的按钮状态。 特别是，当缩 `selected='true'` 略图模式为活动状态时，与查看器状态对应， `selected='false'` 与具有主视图的默认状态对应。

按钮工具提示可以本地化。 有关 [详细信息，请参阅用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例——设置28 x 28像素的缩览图按钮，从主控件栏的底部放置4个像素，从左边缘放置5个像素，在选择或不选择时，为四个不同的按钮状态中的每一个状态显示不同的图像。

```
.s7ecatalogviewer .s7thumbnailpagebutton{ 
margin-top: 4px; 
margin-left: 5px; width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='false'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='up'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='over'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='down'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailpagebutton [selected='true'][state='disabled'] { 
background-image:url(images/v2/ThumbnailPageButton_dark_disabled.png); 
}
```

