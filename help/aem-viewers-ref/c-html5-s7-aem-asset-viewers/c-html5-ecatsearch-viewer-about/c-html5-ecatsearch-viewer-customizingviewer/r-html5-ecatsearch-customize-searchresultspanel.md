---
description: 搜索结果面板由顶部的搜索输入框和显示信息性消息或搜索结果的主区域组成。
seo-description: 搜索结果面板由顶部的搜索输入框和显示信息性消息或搜索结果的主区域组成。
seo-title: 搜索结果面板
solution: Experience Manager
title: 搜索结果面板
topic: Dynamic Media
uuid: 43d8e003-79f7-4e41-98d7-b362ab7180ea
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '952'
ht-degree: 2%

---


# 搜索结果面板{#search-results-panel}

搜索结果面板由顶部的搜索输入框和显示信息性消息或搜索结果的主区域组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

当面板处于活动状态时，查看器用户界面将覆盖半透明填充。 此填充的颜色和不透明度由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>叠加的颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p>颜色的不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

搜索结果面板始终占据所有可用的查看器高度。 但是，您可以配置宽度。 可以将宽度设置为绝对像素值，这是大中型断点的默认设置。 或者，可将宽度设置为100%，以使搜索结果面板占用整个查看器区域。 面板宽度由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**搜索结果空间的CSS属性**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 搜索结果空间的宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——在大中型断点上设置一个250像素宽的搜索结果面板，在小型断点上使用一个全尺寸面板：

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

搜索结果面板的顶部专用于搜索输入框。 输入框两侧的边距由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**搜索输入容器的CSS属性**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 在输入框周围填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

搜索输入字段由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**搜索输入字段的CSS属性**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>搜索输入字段的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充左  </span> </p> </td> 
   <td colname="col2"> <p> 输入字段边界与输入文本之间的内填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>搜索输入字段的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>搜索输入字段的边距 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>文本字体的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置具有0像素高和14像素文本字体的搜索输入字段：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

默认情况下，以“外观玻璃”形式显示的搜索输入字段左侧的搜索按钮由以下CSS类选择器控制：

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**搜索输入按钮的CSS属性**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>搜索输入按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>搜索输入按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>“外观玻璃”图标图像的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景大小  </span> </p> </td> 
   <td colname="col2"> <p>“外观玻璃”图标的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>搜索输入按钮的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距  </span> </p> </td> 
   <td colname="col2"> <p>搜索输入按钮的边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置一个26 x 26像素的“镜头”图标的搜索按钮；大小为30像素，边框为1像素：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

当首次调用该特征时，搜索结果面板可显示文本提示。 当用户的搜索未返回任何结果时，也会显示一条消息。 在所有情况下，文本都显示在搜索结果面板的主要部分，并由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**搜索信息的CSS属性**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 文本的颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>文本字体的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>水平文本对齐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>字体文本的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此文本面板支持`state`属性选择器，该选择器可用于将不同的样式应用于不同的文本消息。 特别是，`state='prompt'`对应于首次调用面板时显示的文本提示；`state='results'`与含有搜索点击信息的文本相对应；`state='no_results'`与搜索查询未返回任何结果时显示的文本相对应。

消息文本可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例——设置使用灰色18像素字体的文本面板：

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

对于具有搜索点击量的页面，搜索结果将呈现为单列或单行缩略图。 搜索结果缩览图之间的间距由以下CSS类选择器控制：

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**缩略图单元格的CSS属性**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距  </span> </p> </td> 
   <td colname="col2"> <p> 每个缩略图周围垂直边距的大小。 实际缩略图间距等于为<span class="codeph"> .s7thumbcell </span>设置的上边距和下边距之和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置10像素间距：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

通过以下CSS类选择器控制各个缩略图的外观：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**缩略图的CSS属性**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>缩略图的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>缩略图的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>缩略图的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要设置215 x 129像素的缩略图，请使用浅灰色默认边框和深灰色选定边框：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

缩略图标签的外观由以下CSS类选择器控制：

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**标签的CSS属性**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 颜色  </span> </p> </td> 
   <td colname="col2"> <p> 文本颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>文本字体的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>文本字体的大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置使用12像素、灰色、Helvetica字体的标签：

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

在使用鼠标输入的系统上，用户在搜索结果面板底部滚动两个滚动按钮，以浏览搜索结果。 上下滚动按钮的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

无法使用CSS顶部、左侧、底部和右侧属性定位滚动按钮。 相反，查看器逻辑会自动定位它们。

**上下滚动按钮的CSS属性**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>滚动按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>滚动按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置位置（如果使用CSS Sprite）。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，该选择器可用于将不同的外观应用于`"up"`、`"down"`、`"over"`和`"disabled"`按钮状态。

可以本地化按钮工具提示。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例——设置一个125 x 35像素的向上滚动按钮，每个状态的图稿不同：

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```

