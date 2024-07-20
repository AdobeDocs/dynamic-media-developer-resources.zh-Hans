---
title: 嵌入共享
description: 嵌入共享工具由添加到“社交”共享面板的按钮以及激活该工具时显示的模式对话框组成。 按钮的位置完全由社交共享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d5f8db82-f1f9-45be-990d-ebfef97507b6
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '2621'
ht-degree: 0%

---

# 嵌入共享{#embed-share}

嵌入共享工具由添加到“社交”共享面板的按钮以及激活该工具时显示的模式对话框组成。 按钮的位置完全由社交共享工具管理。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

嵌入共享按钮的外观可通过以下CSS类选择器来控制：

```
.s7smartcropvideoviewer .s7embedshare
```

嵌入共享工具的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

可以通过在社交共享面板的CSS类中设置`display:none` CSS属性来删除该按钮。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

示例 — 要设置一个28 x 28像素的嵌入共享按钮，并为四种不同的按钮状态分别显示不同的图像：

```
.s7smartcropvideoviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

使用以下CSS类选择器可控制对话框处于活动状态时覆盖网页的背景叠加：

```
.s7smartcropvideoviewer .s7embeddialog .s7backoverlay
```

背景叠加的&#x200B;**CSS属性**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p>背景叠加不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>背景叠加颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将背景叠加设置为具有70%不透明度的灰色，请执行以下操作：

```
.s7smartcropvideoviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

默认情况下，模式对话框会以桌面系统屏幕的中心位置显示，并在触控设备上显示整个网页区域。 在所有情况下，对话框的位置和大小都由组件管理。 使用以下CSS类选择器控制该对话框：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialog
```

**对话框的CSS属性**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框半径</span> </p> </td> 
   <td colname="col2"> <p> 对话框边框半径（如果对话框不占用整个浏览器）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>对话框背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>应取消设置或设置为100%，在这种情况下，对话框会占用整个浏览器窗口（触控设备首选此模式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>应取消设置或设置为100%，在这种情况下，对话框会占用整个浏览器窗口（触控设备首选此模式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置对话框以使用整个浏览器窗口并在触控设备上使用白色背景：

```
.s7smartcropvideoviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

对话框标题由图标、标题文本和关闭按钮组成。 标题容器的控制方式

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader
```

对话框标头的&#x200B;**CSS属性**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p> 标题内容的内部边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

图标和标题文本将封装在一个额外的容器中，由控制

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**对话框行的CSS属性**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p> 标题图标和标题的内边距 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题图标由以下CSS类选择器控制

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadericon
```

**对话框标题图标的CSS属性**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>图标高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>图标图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题标题由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadertext
```

**对话框标题文本的CSS属性**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内部文本边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用以下CSS类选择器控制“关闭”按钮：

```
.s7smartcropvideoviewer .s7embeddialog .s7closebutton
```

关闭按钮的**CSS属性**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p> 相对于标题容器的垂直按钮位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> 相对于标题容器的水平按钮位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>按钮的内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>每个状态的按钮图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

可以本地化“关闭”按钮工具提示和对话框标题。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

示例 — 要设置带有内边距的对话框标题，请设置24 x 14像素图标、粗体16点标题和28 x 28像素关闭按钮。 最后，将其从顶部放置两个像素，从对话框容器右侧放置两个像素：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

对话框页脚包含“取消”按钮。 使用以下CSS类选择器控制页脚容器：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter
```

**对话框页脚的CSS属性**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框</span> </p> </td> 
   <td colname="col2"> <p> 可用于在视觉上分隔页脚和对话框其余部分的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

页脚具有用于保存按钮的内部容器。 可使用以下CSS类选择器来控制分类：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogbuttoncontainer
```

**对话框按钮容器的CSS属性**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p> 页脚和按钮之间的内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

全选按钮由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton
```

该按钮仅在桌面系统上可用。

“全选”按钮的&#x200B;**CSS属性**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>全选按钮支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

使用以下CSS类选择器可控制“取消”按钮：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton
```

对话框取消按钮的&#x200B;**CSS属性**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
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
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>取消按钮支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

此外，这两个按钮共享公用的CSS类，该类可以包含与其他对话框按钮相同的CSS设置：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter .s7button
```

按钮的&#x200B;**CSS属性**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>按钮字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>按钮字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>按钮字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行高</span> </p> </td> 
   <td colname="col2"> <p> 按钮内的文本高度。 影响垂直对齐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">盒阴影</span> </p> </td> 
   <td colname="col2"> <p>投影。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右边距</span> </p> </td> 
   <td colname="col2"> <p>右按钮边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化按钮工具提示。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

示例 — 使用64 x 34 Cancel按钮设置对话框页脚，每种按钮状态的文本颜色和背景颜色不同：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主对话框区域位于页眉和页脚之间，右侧包含可滚动的对话框内容和滚动面板。 在所有情况下，此区域的宽度均由组件管理，因此无法在CSS中设置此区域。 主对话框区域由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogviewarea
```

对话框查看区域的**CSS属性**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p> 主对话框区域的高度。 仅当对话框在桌面模式下工作时，才应指定它。 当调整对话框的大小以占据整个浏览器窗口时，此选项不适用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>主对话框区域的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p>外边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将主对话框区域设置为300像素高度，具有十像素边距，并使用白色背景：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

所有表单内容（如标签和输入字段）都驻留在由控制的容器中

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogbody
```

如果此容器的高度看起来比主对话框区域大，则组件会自动启用垂直滚动。

对话框正文的**CSS属性**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将表单内容设置为具有十个像素的填充：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

对话框表单中的所有静态标签都由控制

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoglabel
```

此类不适合控制标签大小或位置，因为您可以将其应用于表单用户界面各个位置的文本。

对话框标签的**CSS属性。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>标签字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>标签字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>标签字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>标签文本颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化对话框标签工具提示。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

示例 — 将所有标签设置为灰色，粗体带九像素字体：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

显示在嵌入代码顶部的文本副本的大小由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputwide
```

对话框输入范围字段的&#x200B;**CSS属性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>输入字段宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将文本副本的宽度设置为430像素，并在底部填充10像素：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

嵌入代码将封装在容器中，并使用以下CSS类选择器进行控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer
```

对话框输入容器的&#x200B;**CSS属性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>嵌入代码容器的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框</span> </p> </td> 
   <td colname="col2"> <p>嵌入代码容器周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要在嵌入代码文本周围设置1像素灰色边框，请使其宽度为430像素，并具有10像素填充：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

使用以下CSS类选择器控制实际的嵌入代码文本：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer
```

对话框输入容器的&#x200B;**CSS属性**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自动换行</span> </p> </td> 
   <td colname="col2"> <p>文字环绕样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置嵌入代码以使用`break-word`单词换行：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

嵌入大小标签和下拉列表位于对话框底部，并放入由以下CSS类选择器控制的容器中：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel
```

对话框嵌入大小面板的&#x200B;**CSS属性**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将嵌入大小面板设置为具有十个填充像素：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

嵌入大小标签的大小和对齐方式由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel
```

对话框嵌入大小面板的&#x200B;**CSS属性**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">垂直对齐</span> </p> </td> 
   <td colname="col2"> <p>垂直标签对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>标签宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将嵌入大小标签设置为顶部对齐和80像素宽：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

嵌入大小组合框的宽度由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox
```

组合框的&#x200B;**CSS属性**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>组合框宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>组合框支持可能值为`true`和`false`的`expanded`属性选择器。 当组合框显示预定义的嵌入大小之一时使用`true`值，因此应采用所有可用宽度。 在组合框中选择了自定义大小选项时使用`false`值，因此它应该收缩以便为自定义宽度和高度输入字段留出空间。

示例 — 将嵌入大小组合框设置为在显示预定义项目时为300像素宽，在显示自定义大小时为110像素宽：

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

组合框文本的高度由特殊内部元素定义，并使用以下CSS类选择器进行控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxtext
```

组合框文本的&#x200B;**CSS属性**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>组合框文本高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将嵌入大小组合框文本高度设置为40像素，请执行以下操作：

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

组合框的右侧有一个“下拉”按钮，它通过以下CSS类选择器进行控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

组合框按钮的&#x200B;**CSS属性**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>组合框内的垂直按钮位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>水平按钮在组合框中的位置。 </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>每个状态的按钮图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

示例 — 将“下拉”按钮设置为28 x 28像素，并为每种状态提供单独的图像：

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

使用以下CSS类选择器来控制在打开组合框时显示嵌入大小列表的面板：

```
.s7smartcropvideoviewer .s7embeddialog .s7comboboxdropdown
```

面板的大小和位置由组件控制。 无法通过CSS更改此设置。

组合框下拉列表的&#x200B;**CSS属性**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框</span> </p> </td> 
   <td colname="col2"> <p>面板边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将组合框面板设置为具有一个像素灰色边框：

```
.s7smartcropvideoviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

下拉面板中由以下CSS类选择器控制的单个项目：

```
.s7smartcropvideoviewer .s7embeddialog .s7dropdownitemanchor
```

下拉项锚点的&#x200B;**CSS属性**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>项目背景。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将组合框面板项目设置为具有白色背景：

```
.s7smartcropvideoviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

组合框面板中选定项目的左侧显示的复选标记，它受以下CSS类选择器的控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7checkmark
```

复选标记框的&#x200B;**CSS属性**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>图标高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>项目图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将复选标记图标设置为25 x 25像素：

```
.s7smartcropvideoviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

在嵌入大小组合框中选择“自定义大小”选项后，对话框在右侧显示两个额外的输入字段，以允许用户输入自定义嵌入大小。 这些字段将封装在容器中，该容器由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsizepanel
```

对话框自定义大小面板的&#x200B;**CSS属性**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">已离开</span> </p> </td> 
   <td colname="col2"> <p> 距嵌入大小组合框的距离。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将自定义大小输入字段面板设置为组合框右侧20像素：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

每个自定义大小输入字段都包装在一个容器中，该容器可呈现边框并设置字段之间的边距。 可使用以下CSS类选择器来控制分类：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsize
```

对话框自定义大小的&#x200B;**CSS属性**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框</span> </p> </td> 
   <td colname="col2"> <p>输入字段周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 输入字段宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p> 输入字段边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p> 输入字段边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将自定义大小输入字段设置为具有一个像素灰色边框、边距、内边距和70像素宽：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

如果需要垂直滚动，则滚动条将在对话框右边缘附近的面板中呈现，该面板由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogscrollpanel
```

对话框滚动面板的&#x200B;**CSS属性**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>滚动面板宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将滚动面板的宽度设置为44像素

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

使用以下CSS类选择器控制滚动条区域的外观：

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar
```

滚动条的&#x200B;**CSS属性**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>滚动条宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p> 垂直滚动条从滚动面板顶部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p> 垂直滚动条从滚动面板底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> 水平滚动条从滚动面板的右边缘偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个宽度为28像素的滚动条，该滚动条在滚动面板的顶部、右侧和底部具有8像素边距：

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

滚动条轨道是上下滚动按钮之间的区域。 组件会自动设置轨道的位置和高度。 使用以下CSS类选择器控制跟踪

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

滚动条轨道的&#x200B;**CSS属性**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>轨道宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 跟踪背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置宽度为28像素且背景为灰色的滚动条轨道：

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

滚动条缩略图在滚动轨道区域内垂直移动。 其垂直位置完全由组件逻辑控制。 但是，缩略图高度不会因内容量而动态变化。 可以使用以下CSS类选择器配置缩略图高度和其他方面：

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

滚动条缩略图的&#x200B;**CSS属性**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
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
   <td colname="col2"> <p>轨道顶部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充底部</span> </p> </td> 
   <td colname="col2"> <p> 轨道底部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 为给定的缩略图状态显示的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态： `up`、`down`、`over`和`disabled`。

示例 — 设置一个滚动条缩览图，其大小为28 x 45像素，顶部和底部有10像素边距，并且每种状态具有不同的图稿：

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

顶部和底部滚动按钮的外观可通过以下CSS类选择器进行控制：

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton 
```

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

无法使用CSS top、left、bottom和right属性定位滚动按钮。 相反，查看器逻辑会自动定位它们。

顶部和底部滚动按钮的&#x200B;**CSS属性**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>这些按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态： `up`、`down`、`over`和`disabled`。

可以本地化按钮工具提示。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

示例 — 设置具有28 x 32像素且每种状态有不同图稿的滚动按钮：

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
