---
description: 目录是位于主控制栏中的按钮。 激活后，将显示一个下拉面板，其中包含页面索引和标签的列表。
solution: Experience Manager
title: 目录
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog
role: Developer,Business Practitioner
exl-id: 9b61e269-201d-4083-9c47-0b73d55aa6ed
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 2%

---

# 目录{#table-of-contents}

目录是位于主控制栏中的按钮。 激活后，将显示一个下拉面板，其中包含页面索引和标签的列表。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

根据配置，列表可以包含目录中存在的所有页面，也可以仅包含那些定义了明确标签的页面。 在桌面系统上，如果列表的长度大于可用屏幕的面积，则右侧会显示一个滚动条。

使用以下CSS类选择器控制查看器用户界面中目录按钮的位置和大小：

```
.s7ecatalogviewer .s7tableofcontents
```

**目录的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 顶部  </span> </p> </td> 
   <td colname="col2"> <p> 与控制栏顶部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 左  </span> </p> </td> 
   <td colname="col2"> <p> 左侧的到下一个按钮的距离；或者如果这是一行中的第一个按钮，则位于控制栏的左侧。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 目录按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 目录按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，该选择器可用于将不同的外观应用到不同的按钮状态。

按钮工具提示可进行本地化。 有关更多信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例 — 设置目录按钮，其位置为从底部4像素和从主控制栏左侧43像素；大小为28 x 28像素，并且四个不同按钮状态中的每一个状态都会显示一个不同的图像：

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

下拉面板的外观由以下CSS类选择器控制：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**下拉面板的CSS属性**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> 下拉面板的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 面板边界和内容之间的内部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 框阴影  </span> </p> </td> 
   <td colname="col2"> <p> 在面板周围投影。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>无法从CSS控制下拉面板的大小或位置；组件以编程方式管理其布局。

示例 — 设置一个下拉面板，其中具有半透明的黑色背景、内容周围的5像素边距和投影：

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

单个项目的外观通过以下CSS类选择器进行控制：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**项目的CSS属性**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>项目的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内部内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>下拉列表项支持`state`属性选择器，该选择器可用于应用不同的外观来悬停和选择的项目状态。

示例 — 设置一个下拉项，其字体为Helvetica 14像素，高19像素。 选择项目时，悬停时具有深灰色背景和浅灰色背景：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

使用以下CSS类选择器控制显示页面索引的元素：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**页面索引的CSS属性**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最小宽度  </span> </p> </td> 
   <td colname="col2"> <p> 最小元素宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最大宽度  </span> </p> </td> 
   <td colname="col2"> <p> 元素最大宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内边距 — 右边距  </span> </p> </td> 
   <td colname="col2"> <p> 页面索引和页面标签之间的距离。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>可以通过为`s7index` CSS类设置`display:none`来完全隐藏页面索引。

示例1 — 在右侧设置最小宽度为40像素、最大宽度为70像素和5像素边距的页面索引：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

示例2 — 隐藏页面索引：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

使用以下CSS类选择器控制页面标签：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**页面标签的CSS属性**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最小宽度  </span> </p> </td> 
   <td colname="col2"> <p> 最小元素宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 最大宽度  </span> </p> </td> 
   <td colname="col2"> <p> 元素最大宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置最小宽度为40像素、最大宽度为240像素的页面索引：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

如果下拉面板中的项目数量多于垂直容纳的项目，并且系统是桌面，则组件会在面板的右侧呈现垂直滚动条。 通过以下CSS类选择器控制滚动条区域的外观：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**滚动条的CSS属性**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p> 滚动条宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 垂直滚动条从面板区域的顶部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直滚动条从面板区域的底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 水平滚动条与面板区域的右边缘偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置宽度为28像素的滚动条，该滚动条在面板的顶部、右侧或底部区域没有边距：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

滚动条轨道是顶部和底部滚动按钮之间的区域。 该组件会自动设置轨道的位置和高度。 通过以下CSS类选择器控制跟踪：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**滚动跟踪的CSS属性**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>轨道宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>跟踪背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置宽28像素且具有半透明灰色背景的滚动条轨道：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

滚动条拇指在滚动轨道区域内垂直移动。 其垂直位置由组件逻辑控制。 但是，缩览图高度不会根据内容的数量动态更改。 您可以使用以下CSS类选择器配置缩览图高度和其他方面：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**滚动条缩览图的CSS属性**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>拇指宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>拇指高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top  </span> </p> </td> 
   <td colname="col2"> <p> 轨道顶部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom  </span> </p> </td> 
   <td colname="col2"> <p>轨道底部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为给定的拇指状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩览图支持`state`属性选择器，该选择器可用于对`up`、`down`、`over`和`disabled`缩览图状态应用不同的外观。

示例 — 设置一个滚动条缩览图，其28 x 45像素，上下边距为10像素，每种状态的图稿都不同：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

通过以下CSS类选择器控制顶部和底部滚动按钮的外观：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

无法使用CSS `top`、`left`、`bottom`和`right`属性定位滚动按钮；相反，查看器逻辑会自动定位它们。

**向上滚动和向下滚动按钮的CSS属性**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>按钮支持`state`属性选择器，该选择器可用于对`up`、`down`、`over`和`disabled`按钮状态应用不同的外观。

按钮工具提示可进行本地化。 有关更多信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例 — 设置28 x 32像素的滚动按钮，每个状态具有不同的图稿：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
