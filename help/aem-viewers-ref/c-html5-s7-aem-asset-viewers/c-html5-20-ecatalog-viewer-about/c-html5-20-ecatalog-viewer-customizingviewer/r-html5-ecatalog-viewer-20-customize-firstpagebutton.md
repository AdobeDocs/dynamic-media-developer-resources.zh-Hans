---
description: 单击或点按此按钮可使用户转到目录中的第一页。 此按钮显示在台式机系统和平板电脑的主控制栏中；在手机上，它会添加到辅助控制栏。 您可以使用CSS调整此按钮的大小、外观和位置。
seo-description: 单击或点按此按钮可使用户转到目录中的第一页。 此按钮显示在台式机系统和平板电脑的主控制栏中；在手机上，它会添加到辅助控制栏。 您可以使用CSS调整此按钮的大小、外观和位置。
seo-title: 首页按钮
solution: Experience Manager
title: 首页按钮
uuid: fd164899-505c-448b-8dba-7581d97d87b6
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 1%

---


# 首页按钮{#first-page-button}

单击或点按此按钮可使用户转到目录中的第一页。 此按钮显示在台式机系统和平板电脑的主控制栏中；在手机上，它会添加到辅助控制栏。 您可以使用CSS调整此按钮的大小、外观和位置。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**主查看器区域的CSS属性**

按钮的外观由以下CSS类选择器控制：

`.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton`

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
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的上边框进行定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的右边框中定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的左边框中的位置，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从主控制栏（在台式机系统和平板电脑上）或辅助控制栏（在手机上）的底边框中的位置，包括边距。 </p> </td> 
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
   <td colname="col2"> <p> 如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置第一个页面按钮（28 x 28像素），从底部放置4个像素，从主控件条的左边缘放置220像素，并针对四个不同的按钮状态中的每个状态显示不同的图像。

```
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton { 
bottom:4px; 
left:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/FirstPageButton_dark_up.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/FirstPageButton_dark_over.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/FirstPageButton_dark_down.png); 
} 
.s7ecatalogviewer .s7firstpagebutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/FirstPageButton_dark_disabled.png); 
}
```

