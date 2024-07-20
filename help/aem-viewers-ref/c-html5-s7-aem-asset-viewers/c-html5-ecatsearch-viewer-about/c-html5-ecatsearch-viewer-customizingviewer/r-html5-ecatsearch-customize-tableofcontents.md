---
title: 目录
description: 目录是主控件栏中的一个按钮。 激活后，将显示一个下拉面板，其中包含页面索引和标签列表。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: bc597c68-b86c-4577-9d24-6999eccada78
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# 目录{#table-of-contents}

目录是主控件栏中的一个按钮。 激活后，将显示一个下拉面板，其中包含页面索引和标签列表。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

根据配置，列表可以包含目录中存在的所有页面，也可以仅包含已定义显式标签的页面。 在桌面系统上，如果列表长于可用的屏幕区域，则右侧会显示滚动条。

查看器用户界面中目录按钮的位置和大小由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7tableofcontents
```

目录的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上边距</span> </p> </td> 
   <td colname="col2"> <p> 从控件栏顶部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左边距</span> </p> </td> 
   <td colname="col2"> <p> 与左侧的下一个按钮或控制栏左侧的距离（如果该按钮是行中的第一个按钮）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 目录按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p> 目录按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置一个目录按钮，该按钮位于主控件栏的底部4像素和左侧43像素的位置。 大小为28 x 28像素，并且对于四种不同的按钮状态中的每一种都显示不同的图像：

```
.s7ecatalogsearchviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

下拉面板的外观由以下CSS类选择器控制：

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel
```

下拉面板的&#x200B;**CSS属性**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 下拉面板的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p> 面板边界和内容之间的内部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">盒阴影</span> </p> </td> 
   <td colname="col2"> <p> 面板周围的投影。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>无法通过CSS控制下拉面板的大小或位置；组件以编程方式管理其布局。

示例 — 设置一个下拉面板，该面板具有半透明的黑色背景、围绕内容的5像素边距和投影：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

单个项目的外观可以通过以下CSS类选择器进行控制：

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item
```

项目的&#x200B;**CSS属性**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>项目的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内部填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>下拉列表项支持`state`属性选择器，该选择器可用于将不同的外观应用于悬停和选定项状态。

示例 — 设置具有Helvetica® 14像素字体和19像素高的下拉项目。 项目在悬停时具有深灰色背景，在选中时具有浅灰色背景：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

显示页面索引的元素受以下CSS类选择器的控制：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index
```

页面索引的&#x200B;**CSS属性**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">最小宽度</span> </p> </td> 
   <td colname="col2"> <p> 最小元素宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">最大宽度</span> </p> </td> 
   <td colname="col2"> <p> 最大元素宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充右侧</span> </p> </td> 
   <td colname="col2"> <p> 页面索引和页面标签之间的距离。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>通过为`s7index` CSS类设置`display:none`，可以完全隐藏页面索引。

示例1 — 设置一个页面索引，其中最小宽度为40像素，最大宽度为70像素，右侧具有5像素边距：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

示例2 — 隐藏页面索引：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

使用以下CSS类选择器控制页面标签：

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label
```

页面标签的&#x200B;**CSS属性**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">最小宽度</span> </p> </td> 
   <td colname="col2"> <p> 最小元素宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">最大宽度</span> </p> </td> 
   <td colname="col2"> <p> 最大元素宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置最小宽度为40像素和最大宽度为240像素的页面索引：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

如果下拉面板中的项目超出垂直容纳范围（且系统为桌面），则组件会在面板右侧呈现垂直滚动条。 滚动条区域的外观可通过以下CSS类选择器来控制：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar
```

滚动条的&#x200B;**CSS属性**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 滚动条宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p> 垂直滚动条从面板区域顶部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p> 垂直滚动条从面板区域的底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> 水平滚动条从面板区域的右边缘偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个宽度为28像素的滚动条，该滚动条在面板的顶部、右侧或底部区域没有边距：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

滚动条轨道是上下滚动按钮之间的区域。 组件会自动设置轨道的位置和高度。 使用以下CSS类选择器控制跟踪：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

滚动轨道的&#x200B;**CSS属性**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>轨道宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>轨道背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个宽度为28像素并具有半透明灰色背景的滚动条轨道：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

滚动条缩略图在滚动轨道区域内垂直移动。 其垂直位置由组件逻辑控制。 但是，缩略图高度不会因内容量而动态变化。 您可以使用以下CSS类选择器配置缩略图高度和其他方面：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

滚动条缩略图的&#x200B;**CSS属性**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>缩略图宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>缩略图高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充顶端</span> </p> </td> 
   <td colname="col2"> <p> 轨道顶部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充底部</span> </p> </td> 
   <td colname="col2"> <p>轨道底部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 为给定缩略图状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持`state`属性选择器，该选择器可用于将不同的外观应用于`up`、`down`、`over`和`disabled`缩略图状态。

示例 — 设置一个大小为28 x 45像素的滚动条缩略图，其顶部和底部有10像素边距，并且每种状态具有不同的图稿：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

顶部和底部滚动按钮的外观可通过以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

无法使用CSS `top`、`left`、`bottom`和`right`属性来定位滚动按钮；相反，查看器逻辑会自动定位它们。

向上和向下滚动按钮的&#x200B;**CSS属性**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>按钮支持`state`属性选择器，该选择器可用于将不同的外观应用于`up`、`down`、`over`和`disabled`按钮状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置滚动按钮，这些按钮的像素为28 x 32，并且每种状态的图稿各不相同：

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
