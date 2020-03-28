---
description: 嵌入共享工具由添加到“社交共享”面板的按钮和激活工具时显示的模态对话框组成。 按钮的位置完全由社交共享工具管理。
seo-description: 嵌入共享工具由添加到“社交共享”面板的按钮和激活工具时显示的模态对话框组成。 按钮的位置完全由社交共享工具管理。
seo-title: 嵌入共享
solution: Experience Manager
title: 嵌入共享
topic: Dynamic media
uuid: 73d259fe-0978-4f47-95f6-bbfcd3b7bad1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 嵌入共享{#embed-share}

嵌入共享工具由添加到“社交共享”面板的按钮和激活工具时显示的模态对话框组成。 按钮的位置完全由社交共享工具管理。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

嵌入共享按钮的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embedshare
```

**嵌入共享工具的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
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

可以通过在“社交共享”面板的CSS类上设置 `display:none` CSS属性，从中删除该按钮。

按钮工具提示可以本地化。 有关 [详细信息，请参阅用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例——设置一个28 x 28像素的嵌入共享按钮，并为四个不同按钮状态中的每个状态显示一个不同的图像：

```
.s7ecatalogsearchviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

使用以下CSS类选择器控制在对话框处于活动状态时覆盖网页的背景叠加：

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay
```

**背景叠加的CSS属性**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>背景叠加不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>背景叠加颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将背景叠加设置为灰色且不透明度为70%:

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

默认情况下，模态对话框显示在桌面系统屏幕的中心位置，并在触控设备上占据整个网页区域。 在所有情况下，对话框的定位和大小调整都由组件管理。 使用以下CSS类选择器控制该对话框：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialog
```

**对话框的CSS属性**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 对话框边框radius，以防对话框不占用整个浏览器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>对话框背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>应取消设置，或设置为100%，在这种情况下，对话框将占据整个浏览器窗口（触控设备首选此模式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>应取消设置，或设置为100%，在这种情况下，对话框将占据整个浏览器窗口（触控设备首选此模式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置对话框以使用整个浏览器窗口并在触控设备上具有白色背景：

```
.s7ecatalogsearchviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

对话框标题由图标、标题文本和关闭按钮组成。 标题容器由

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader
```

**对话框标题的CSS属性**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 标题内容的内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

图标和标题文本将打包到由

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**对话框行的CSS属性**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 标题图标和标题的内填充 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题图标由以下CSS类选择器控制

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon
```

**对话框标题图标的CSS属性**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>图标高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p>图标图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中定位（如果使用CSS Sprite）。 </p> <p>另请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题标题由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext
```

**对话框标题文本的CSS属性**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体权重 </span> </p> </td> 
   <td colname="col2"> <p>字体权重。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小 </span> </p> </td> 
   <td colname="col2"> <p>字体高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内部文本填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用以下CSS类选择器控制关闭按钮：

```
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton
```

**关闭按钮的CSS属性**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 相对于标题容器的垂直按钮位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 相对于标题容器的水平按钮位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>按钮的内填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p>每个状态的按钮图像。 </p> </td> 
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

示例——设置具有填充、24 x 14像素图标、粗体16点标题和28 x 28像素关闭按钮的对话框标题，从顶部放置两个像素，从对话框容器的右侧放置两个像素：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

对话框页脚由“取消”按钮组成。 使用以下CSS类选择器控制页脚容器:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter
```

**对话框页脚的CSS属性**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 用于以可视方式将页脚与对话框其余部分分开的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

页脚具有保留按钮的内部容器。 它由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer
```

**对话框按钮容器的CSS属性**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 页脚和按钮之间的内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用以下CSS类选择器控制“全选”按钮：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton
```

该按钮仅在桌面系统上可用。

**“全选”按钮的CSS属性**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>“全选”按钮支持属 `state` 性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

使用以下CSS类选择器控制“取消”按钮：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton
```

**对话框取消按钮的CSS属性**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持属 `state` 性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

此外，两个按钮共享相同的公用CSS类，该类可包含其他对话框按钮相同的CSS设置：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button
```

**按钮的CSS属性**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体权重 </span> </p> </td> 
   <td colname="col2"> <p>按钮字体权重。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小 </span> </p> </td> 
   <td colname="col2"> <p>按钮字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>按钮字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> 按钮内的文本高度。 影响垂直对齐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>投影。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>右按钮边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

按钮工具提示可以本地化。 有关 [详细信息，请参阅用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例——要设置一个对话框页脚，其中显示64 x 34“取消”按钮、82 x 34“全选”按钮，并且文本颜色和背景颜色与每个按钮状态不同：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主对话框区域（在页眉和页脚之间）包含可滚动对话框内容和右侧的滚动面板。 在所有情况下，组件都管理此区域的宽度，无法在CSS中设置它。 使用以下CSS类选择器控制主对话框区域：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea
```

**对话框查看区域的CSS属性**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 主对话框区域的高度。 仅当对话框在桌面模式下工作时才应指定它。 当该对话框的大小调整为占用整个浏览器窗口时，它不适用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>主对话框区域的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要将主对话框区域设置为300像素高、有10像素边距并使用白色背景：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

所有表单内容（如标签和输入字段）都驻留在使用以下CSS类选择器控制的容器中：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody
```

如果此容器的高度似乎大于主对话框区域，则组件将自动启用垂直滚动。

**对话框正文的CSS属性**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将表单内容设置为具有十个像素填充：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

对话框表单中的所有静态标签都由

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel
```

此类不适合控制标签大小或位置，因为您可以将它应用于表单用户界面中不同位置的文本。

**对话框标签的CSS属性。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体权重 </span> </p> </td> 
   <td colname="col2"> <p>标签字体权重。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小 </span> </p> </td> 
   <td colname="col2"> <p>标签字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>标签字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>标签文本颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

对话框标签可以本地化。 有关 [详细信息，请参阅用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例——将所有标签设置为灰色，粗体，字体为9像素：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

嵌入代码顶部显示的文本副本的大小由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide
```

**对话框输入宽字段的CSS属性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>输入字段宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将文本副本设置为430像素宽，并在底部具有十个像素填充：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

嵌入代码封装在容器中，并使用以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**对话框输入容器的CSS属性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>嵌入代码容器的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>嵌入代码容器周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——要在嵌入代码文本周围设置一个像素灰色边框，请使其宽度为430像素，并且填充10像素：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

实际嵌入代码文本由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**对话框输入容器的CSS属性**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自动换行 </span> </p> </td> 
   <td colname="col2"> <p>自动换行样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置嵌入代码以使用 `break-word` 自动换行：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

嵌入大小标签和下拉框位于对话框底部，并放入使用以下CSS类选择器控制的容器:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**对话框嵌入大小面板的CSS属性**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置嵌入大小面板，使其具有十个填充像素：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

嵌入大小标签的大小和对齐方式由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**对话框嵌入大小面板的CSS属性**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 垂直对齐 </span> </p> </td> 
   <td colname="col2"> <p>垂直标签对齐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>标签宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将嵌入大小标签设置为顶对齐，80像素宽：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

嵌入大小组合框的宽度由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox
```

**组合框的CSS属性**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>组合框宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>组合框支持具有 `expanded` 可能值为和的属性选择 `true` 器 `false`。 `true` 当组合框显示预定义的嵌入大小之一时使用，因此应使用所有可用宽度。 `false` 在组合框中选择自定义大小选项时使用，因此应缩小以为自定义宽度和高度输入字段留出空间。

示例——将嵌入大小组合框设置为在显示预定义项目时为300像素宽，在显示自定义大小时为110像素宽：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

组合框文本的高度由特殊的内部元素定义，并由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**组合框文本的CSS属性**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>组合框文本高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将嵌入大小组合框文本高度设置为40像素：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

组合框右侧有一个“下拉”按钮，它由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**组合框按钮的CSS属性**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>组合框内的垂直按钮位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>组合框内的水平按钮位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p>每个状态的按钮图像。 </p> </td> 
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

示例——将下拉按钮设置为28 x 28像素，并为每个状态提供一个单独的图像：

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

使用以下CSS类选择器控制打开组合框时显示嵌入大小列表的面板：

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown
```

面板的大小和位置由组件控制。 无法通过CSS更改它。

**组合框下拉框的CSS属性**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>面板边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将组合框面板设置为具有一个像素灰色边框：

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

下拉面板中的单个项目，它由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor
```

**下拉项锚点的CSS属性**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>项目背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将组合框面板项设置为白色背景：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

使用以下CSS类选择器控制的组合框面板中选定项目左侧显示的复选标记：

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark
```

**复选标记框的CSS属性**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>图标高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p>项目图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中定位（如果使用CSS Sprite）。 </p> <p>另请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将复选标记图标设置为25 x 25像素：

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

在嵌入大小组合框中选择“自定义大小”选项后，对话框右侧将显示两个额外的输入字段，以允许用户输入自定义嵌入大小。 这些字段包含在由以下CSS类选择器控制的容器中：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel
```

**对话框自定义大小面板的CSS属性**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p> 嵌入大小组合框的距离。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将自定义大小输入字段面板设置为组合框右侧的20像素：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

每个自定义大小输入字段都封装在一个容器中，该域渲染边框并设置字段之间的边距。 它由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize
```

**对话框自定义大小的CSS属性**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>输入字段周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 输入字段宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 输入字段边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 输入字段填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将自定义大小输入字段设置为具有一个像素灰色边框、边距、填充且宽度为70像素：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

如果需要垂直滚动，滚动条将呈现在对话框右边缘附近的面板中，该对话框由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel
```

**对话框滚动面板的CSS属性**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>滚动面板宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将滚动面板设置为44像素宽

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

滚动条区域的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar
```

**滚动条的CSS属性**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>滚动条宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 垂直滚动条从滚动面板顶部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直滚动条与滚动面板底部的偏移量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 水平滚动条与滚动面板的右边缘偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置宽28像素、距滚动面板顶部、右侧和底部有8像素边距的滚动条：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

滚动条轨道是顶部和底部滚动按钮之间的区域。 组件会自动设置轨道的位置和高度。 使用以下CSS类选择器控制音轨

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**滚动条轨道的CSS属性**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>轨道宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 跟踪背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置宽28像素且背景为灰色的滚动条轨道：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

滚动条缩略图在滚动轨道区域内垂直移动。 其垂直位置完全由组件逻辑控制。 但是，缩略图高度不会根据内容的数量而动态更改。 可通过以下CSS类选择器配置缩略图高度和其他方面：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**滚动条缩略图的CSS属性**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>缩略图宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>缩略图高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>轨道顶部之间的垂直填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> 轨道底部之间的垂直填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p> 为给定的缩略图状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中定位（如果使用CSS Sprite）。 </p> <p>另请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持 `state` 属性选择器，该选择器可用于将不同的外观应用到不同的缩略图状态： `up`、 `down`、 `over`和 `disabled`。

示例——设置一个滚动条缩略图，该缩略图为28 x 45像素，顶部和底部有10个像素边距，并且每个状态的图稿各不相同：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

顶部和底部滚动按钮的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

无法使用CSS、、和属性定位 `top`滚动 `left`按 `bottom`钮 `right` 。 相反，查看器逻辑会自动定位它们。

**顶部和底部滚动按钮的CSS属性**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中定位（如果使用CSS Sprite）。 </p> <p>另请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>这些按钮支持属 `state` 性选择器，该选择器可用于将不同的外观应用于不同的按钮状态： `up`、 `down`、 `over`和 `disabled`。

按钮工具提示可以本地化。 有关 [详细信息，请参阅用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例——设置28 x 32像素的滚动按钮，并且每个状态的图稿不同：

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

