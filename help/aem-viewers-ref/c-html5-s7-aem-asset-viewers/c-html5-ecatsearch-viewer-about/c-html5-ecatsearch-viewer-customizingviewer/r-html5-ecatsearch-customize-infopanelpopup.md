---
title: “信息”面板弹出窗口
description: 当用户激活的图像映射具有在Dynamic Media Classic中定义的rollover_key属性，并且已为查看器正确配置了信息面板功能时，“信息面板弹出窗口”会显示在查看器区域的中间。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 907b7bd5-3f87-4918-ad62-8a28249ea023
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 3%

---

# “信息”面板弹出窗口{#info-panel-popup}

当用户激活的图像映射具有在Dynamic Media Classic中定义的rollover_key属性，并且已为查看器正确配置了信息面板功能时，“信息面板弹出窗口”会显示在查看器区域的中间。

“信息”面板背景涵盖整个查看器区域，并可通过以下CSS类选择器进行控制：

`.s7ecatalogsearchviewer .s7infopanelpopup .s7backoverlay`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p>信息面板背景填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。</p> <p>另请参阅 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置信息面板弹出窗口以使用半透明黑色背景。

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7backoverlay { 
 background-color : rgba(0,0,0,0.75); 
}
```

默认情况下，“信息”面板对话框显示在查看器区域的中间。 但是，可以使用CSS类选择器控制其大小、对齐方式、背景和边框。

`.s7ecatalogsearchviewer .s7infopanelpopup .s7overlay`

<table id="table_4E666A03A3D44CEEA72225113553AB3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>“信息面板”对话框在查看器区域面板背景填充中的水平位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>“信息面板”对话框在查看器区域中的垂直位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>对话框宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>对话框高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 左 </span> </p> </td> 
   <td colname="col2"> <p>信息面板对话框的左边距可用于居中显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 顶部 </span> </p> </td> 
   <td colname="col2"> <p>信息面板对话框的上边距可用于居中显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内部对话框内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>对话框背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边框半径 </span> </p> </td> 
   <td colname="col2"> <p>对话框边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 框阴影 </span> </p> </td> 
   <td colname="col2"> <p>对话阴影。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置位于查看器区域中心的300 x 200像素信息面板对话框；顶部有40个像素的内边距，其他所有侧边有10个像素的内边距，背景为浅灰色，边框半径和投影为10个像素。

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7overlay { 
 left: 50%; 
 top: 50%; 
 margin-left: -150px; 
 margin-top: -100px; 
 width: 300px; 
 height: 200px; 
 padding-top: 40px; 
 padding-right: 10px; 
 padding-bottom: 10px; 
 padding-left: 10px; 
 background-color:rgb(221,221,221); 
 border-radius: 10px 10px 10px 10px; 
box-shadow: 0 0 5px rgba(0,0,0,0.25);  
}
```

“信息面板”对话框具有一个关闭按钮，单击或点按该按钮可关闭该对话框。

通过以下CSS类选择器控制此按钮的外观：

`.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从对话框的上边框的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从对话框的右边框定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>从对话框的左边框开始的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从对话框的下边框定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p>为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>另请参阅 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 属性选择器，您可以使用该选择器将不同的外观应用到不同的按钮状态。

按钮工具提示可进行本地化。 请参阅 [用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以了解更多信息。

示例 — 要设置一个28 x 28像素的对话框关闭按钮，该按钮位于信息面板对话框的上边缘和右边缘5个像素处，并针对四个不同按钮状态中的每个状态显示一个不同的图像。

```
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton { 
 width: 28px; 
 height: 28px; 
 top: 5px; 
 right: 5px; 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="up"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="over"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="down"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7infopanelpopup .s7closebutton[state="disabled"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
}
```
