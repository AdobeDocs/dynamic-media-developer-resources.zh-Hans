---
description: 主控件栏是桌面系统和平板电脑上的矩形区域，其中包含eCatalog查看器可用的所有用户界面控件（“大页”按钮除外）。
seo-description: 主控件栏是桌面系统和平板电脑上的矩形区域，其中包含eCatalog查看器可用的所有用户界面控件（“大页”按钮除外）。
seo-title: 主控制栏
solution: Experience Manager
title: 主控制栏
uuid: 0900f678-d7ec-4653-bc8a-21b8da7d5044
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 1%

---


# 主控件栏{#main-control-bar}

主控件栏是桌面系统和平板电脑上的矩形区域，其中包含eCatalog查看器可用的所有用户界面控件（“大页”按钮除外）。

在手机上，它仍保留“缩览图”、“目录”、“下载”、“打印”、“收藏夹”、“社交共享”、“全屏”和“关闭”按钮。 但是，“首页”和“末页”按钮以及“页面指示器”将从主控件栏中删除，并添加到辅助控件栏。 默认情况下，主控制栏显示在桌面系统和手机上的查看器区域的顶部，并移到平板电脑上的查看器区域的底部。 它始终采用整个可用查看器宽度。 可以相对于查看器容器更改其CSS中的颜色、高度和垂直位置。

主控件条的外观由以下CSS类选择器控制：

`.s7ecatalogviewer .s7controlbar`

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
   <td colname="col2"> <p>从查看器顶部定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从查看器底部定位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>主控件条的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**  — 设置一个高度为36像素且位于查看器容器顶部的灰色主控件条。

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

主控件条支持可选的滚动功能。 如果查看器宽度太小，并且没有足够的空间来容纳控制栏中所有预设的按钮，则会激活该按钮。 在这种情况下，控件条的右侧将显示一个两状态箭头按钮。 单击或点按此按钮可将所有控制栏元素向左或向右滚动，具体取决于滚动按钮状态。 此功能的主要用例是纵向小屏幕的移动设备。

主控制栏启用滚动功能，辅助控制栏禁用滚动功能。 使用以下CSS类选择器打开和关闭该功能：

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>设置为<span class="codeph">静态</span>时，将禁用滚动功能。 </p> <p>将此属性设置为<span class="codeph">绝对</span>以启用滚动功能。 </p> </td> 
  </tr> 
 </tbody> 
</table>

滚动按钮将添加到特殊容器元素，该元素可正确放置按钮，并允许您在滚动按钮的高度小于控制栏高度时，以不同于控制栏背景的方式设置按钮周围区域的样式。

此滚动按钮容器的外观由以下CSS类选择器控制：

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>通常应等于或大于滚动按钮本身的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>容器背景色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以通过CSS调整滚动按钮本身的大小和外观。

此按钮的外观由以下CSS类选择器控制：

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高  </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`和`selected`属性选择器，这两个选择器可用于将不同的外观应用于不同的按钮状态。 尤其是，当可将控件条内容滚动到左侧时，`state="selected"`对应于初始滚动按钮状态；`state="default"`对应于内容向左滚动且滚动按钮建议将其返回到初始状态时的状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

**示例**  — 在手机的主控件栏中启用滚动功能，并设置一个64 x 64像素的滚动按钮，在选中或未选中时，该按钮会为4个不同按钮状态中的每个状态显示不同的图像：

```
.s7ecatalogviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```

