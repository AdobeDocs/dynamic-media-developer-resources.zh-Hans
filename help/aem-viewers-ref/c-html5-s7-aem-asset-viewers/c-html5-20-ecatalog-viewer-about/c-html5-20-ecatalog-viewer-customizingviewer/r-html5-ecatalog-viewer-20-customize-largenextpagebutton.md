---
title: 大下一页按钮
description: 单击或点按此按钮会将用户引导至目录中的下一页。 此按钮显示在主控制栏中。 为了节省屏幕空间，此按钮不会显示在手机上。 您可以使用CSS调整此按钮的大小、外观和位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 8147cdf8-298c-4713-a5a5-b34674f6b2c8
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 大下一页按钮{#large-next-page-button}

选择或点击此按钮会将用户引导至目录中的下一页。 此按钮显示在主控制栏中。 为了节省屏幕空间，此按钮不会显示在手机上。 您可以使用CSS调整此按钮的大小、外观和位置。

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

主查看器区域的&#x200B;**CSS属性**

使用以下CSS类选择器控制按钮的外观：

`.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>从主控件栏的顶部边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>从主控制栏的右边框定位，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">已离开</span> </p> </td> 
   <td colname="col2"> <p>从主控制栏的左边框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p>从主控制栏的底部边框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置一个大小为56 x 56像素、垂直居中和固定到右侧查看器边框的下一页按钮，并为四种不同的按钮状态分别显示不同的图像。

```
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton { 
bottom:50%; 
margin-bottom:-28px; 
right:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/RightButton_dark_up.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/RightButton_dark_over.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/RightButton_dark_down.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/RightButton_dark_disabled.png); 
}
```
