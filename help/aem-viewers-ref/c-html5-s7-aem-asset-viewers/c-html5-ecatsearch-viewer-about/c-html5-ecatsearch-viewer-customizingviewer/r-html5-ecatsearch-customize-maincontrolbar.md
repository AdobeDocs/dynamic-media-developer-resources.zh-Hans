---
title: 主控制栏
description: 主控件栏是桌面系统和平板电脑上的矩形区域，其中包含所有可用于eCatalog搜索查看器的用户界面控件（大页面按钮除外）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# 主控制栏{#main-control-bar}

主控件栏是桌面系统和平板电脑上的矩形区域，其中包含所有可用于eCatalog搜索查看器的用户界面控件（大页面按钮除外）。

在手机上，它仍保留缩略图、目录、下载、打印、收藏夹、社交共享、全屏和关闭按钮。 但是，“第一页”、“最后一页”按钮和“页面指示器”从主控制栏中删除，并添加到辅助控制栏。 默认情况下，主控制栏显示在桌面系统和手机上的查看器区域顶部，并移动到平板电脑上的查看器区域底部。 它始终采用整个可用查看器宽度。 可以更改它在CSS中的颜色、高度和垂直位置（相对于查看器容器）。

使用以下CSS类选择器控制主控件栏的外观：

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>位于查看器顶部。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p>位于查看器底部。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>主控制栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>主控件栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** — 设置一个高度为36像素且位于查看器容器顶部的灰色主控件栏。

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

主控制栏支持可选滚动功能。 如果查看器宽度太小，并且没有足够的空间来容纳控制栏中的所有按钮预设，则会激活该查看器。 在这种情况下，控制栏右侧会显示一个双状态箭头按钮。 单击或点按此按钮可将所有控件栏元素向左或向右滚动，具体取决于滚动按钮的状态。 此功能的主要用例是带有纵向小屏幕的移动设备。

在主控制栏上启用滚动功能，在辅助控制栏上禁用滚动功能。 可使用以下CSS类选择器打开和关闭该功能：

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">位置</span> </p> </td> 
   <td colname="col2"> <p>当设置为<span class="codeph">静态</span>时，将禁用滚动功能。 </p> <p>将此属性设置为<span class="codeph">绝对</span>以启用滚动功能。 </p> </td> 
  </tr> 
 </tbody> 
</table>

将滚动按钮添加到特殊容器元素中，以正确放置按钮。 利用该面板，可在滚动按钮高度小于控制栏高度时，将按钮周围的区域样式与控制栏背景的其他区域样式不同。

此滚动按钮容器的外观由以下CSS类选择器控制：

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>通常应等于或大于滚动按钮本身的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>容器背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以通过CSS调整滚动按钮本身的大小和外观。

此按钮的外观可通过以下CSS类选择器来控制：

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
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
   <td colname="col2"> <p>如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`和`selected`属性选择器，它们可用于将不同的外观应用于不同的按钮状态。 特别是，`state="selected"`对应于初始滚动按钮状态（当可以将控件栏内容向左滚动时）。 `state="default"`对应于内容一直向左滚动时的状态，滚动按钮建议将其恢复到初始状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

**示例** — 在移动电话的主控件栏中启用滚动功能。 并且，设置一个64 x 64像素的滚动按钮，当选中或未选中时，该按钮会为4种不同的按钮状态中的每种状态显示不同的图像：

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
