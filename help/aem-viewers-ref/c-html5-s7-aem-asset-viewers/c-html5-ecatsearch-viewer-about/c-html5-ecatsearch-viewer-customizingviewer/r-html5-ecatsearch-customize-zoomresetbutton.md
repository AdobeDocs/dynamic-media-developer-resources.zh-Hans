---
description: 单击或点按此按钮可重置主视图中的图像。 此按钮显示在桌面系统和平板电脑上的主控制栏中。 在手机上，此按钮显示在图像的中下方。 但是，当图像处于重置状态时，不会显示它。 您可以使用CSS调整此按钮的大小、外观和位置。
seo-description: 单击或点按此按钮可重置主视图中的图像。 此按钮显示在桌面系统和平板电脑上的主控制栏中。 在手机上，此按钮显示在图像的中下方。 但是，当图像处于重置状态时，不会显示它。 您可以使用CSS调整此按钮的大小、外观和位置。
seo-title: 缩放重置按钮
solution: Experience Manager
title: 缩放重置按钮
topic: Dynamic media
uuid: 19ef5c77-8352-4021-a022-adec6ecbf078
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 缩放重置按钮{#zoom-reset-button}

单击或点按此按钮可重置主视图中的图像。 此按钮显示在桌面系统和平板电脑上的主控制栏中。 在手机上，此按钮显示在图像的中下方。 但是，当图像处于重置状态时，不会显示它。 您可以使用CSS调整此按钮的大小、外观和位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

按钮的外观由以下CSS类选择器控制：

`.s7ecatalogsearchviewer .s7zoomresetbutton`

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
   <td colname="col2"> <p>从主控制栏（在台式机和平板电脑上）或查看器（在手机上）的上边框定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机和平板电脑上）或查看器（在手机上）的右边框定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机和平板电脑上）或查看器（在手机上）的左边框中的位置，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机和平板电脑上）或查看器（在手机上）的下边框中的位置，包括边距。 </p> </td> 
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
   <td colname="col2"> <p> 在图稿Sprite中定位（如果使用CSS Sprite）。 </p> <p>另请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持属 `state` 性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关 [详细信息，请参阅用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例——设置一个28 x 28像素的缩放重置按钮，该按钮位于（桌面）距主控件栏底部4像素，距右边47像素，并针对四个不同按钮状态中的每个状态显示不同的图像。

```
.s7ecatalogsearchviewer .s7zoomresetbutton { 
bottom:4px; 
right:47px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```

