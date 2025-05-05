---
title: 电子邮件共享
description: 电子邮件共享工具由添加到“社交”共享面板的按钮以及激活工具时显示的模式对话框组成。 按钮的位置完全由社交共享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4c72500b-9750-4fae-9447-96cf600b31c7
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '3081'
ht-degree: 0%

---

# 电子邮件共享{#email-share}

电子邮件共享工具由添加到“社交”共享面板的按钮以及激活工具时显示的模式对话框组成。 按钮的位置完全由社交共享工具管理。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

电子邮件共享按钮的外观可通过以下CSS类选择器来控制：

```
.s7ecatalogviewer .s7emailshare
```

电子邮件共享工具的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col2"> <p> 针对给定按钮状态显示的图像。 </p> </td> 
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

可以通过在社交共享面板的CSS类中设置`display:none` CSS属性来删除该按钮。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置一个28 x 28像素的电子邮件共享按钮，并针对四种不同的按钮状态分别显示不同的图像。

```
.s7ecatalogviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

使用以下CSS类选择器来控制对话框处于活动状态时覆盖网页的背景叠加：

```
.s7ecatalogviewer .s7emaildialog .s7backoverlay
```

背面叠加的&#x200B;**CSS属性**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p> 背景叠加不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>背景叠加颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将背景叠加设置为具有70%不透明度的灰色，请执行以下操作：

```
.s7ecatalogviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

默认情况下，模式对话框会以桌面系统屏幕的中心位置显示，并在触控设备上显示整个网页区域。 在所有情况下，对话框的位置和大小都由组件管理。 该对话框可通过以下CSS类选择器进行控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialog
```

**对话框的CSS属性**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框半径</span> </p> </td> 
   <td colname="col2"> <p> 对话框边框半径（如果对话框未占用整个浏览器窗口）； </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 对话框背景颜色； </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 应取消设置或设置为100%，在这种情况下，对话框会占用整个浏览器窗口（在触控设备上首选此模式）； </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p> 应取消设置或设置为100%，在这种情况下，对话框会占用整个浏览器窗口（触摸设备首选此模式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置对话框以使用整个浏览器窗口并在触控设备上使用白色背景：

```
.s7ecatalogviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

对话框标题由图标、标题文本和关闭按钮组成。 标头容器由以下CSS类选择器控制

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader
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
.s7ecatalogviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**对话框行的CSS属性**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p> 标题图标和标题的内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题图标由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialogheadericon
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
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题标题由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialogheadertext
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
.s7ecatalogviewer .s7emaildialog .s7closebutton
```

关闭按钮的&#x200B;**CSS属性**

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
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

可以本地化“关闭”按钮工具提示和对话框标题。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 要设置带内边距的对话框标题，请设置24 x 17像素图标和粗体16点标题。 最后，一个28 x 28像素的“关闭”按钮，它位于对话框容器顶部两个像素和右侧两个像素的位置：

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

对话框页脚包含取消和发送电子邮件按钮。 使用以下CSS类选择器控制页脚容器：

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter
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

页脚有一个内部容器，用于保存两个按钮。 可使用以下CSS类选择器来控制分类：

```
.s7ecatalogviewer .s7emaildialog .s7dialogbuttoncontainer
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

使用以下CSS类选择器可控制“取消”按钮：

```
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton
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
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

使用以下CSS类选择器控制发送电子邮件按钮：

```
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton
```

对话框操作按钮的&#x200B;**CSS属性**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

此外，这两个按钮共享公用的CSS类，该类可以包含与其他对话框按钮相同的CSS设置：

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter .s7button
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

可以本地化此按钮的工具提示。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 使用64 x 34取消按钮和82 x 34发送电子邮件按钮设置对话框页脚。 每个按钮状态的文本颜色和背景颜色均不同：

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主对话框区域位于页眉和页脚之间，右侧包含可滚动的对话框内容和滚动面板。 在所有情况下，此区域的宽度均由组件管理，因此无法在CSS中设置此区域。 主对话框区域由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea
```

对话框查看区域的&#x200B;**CSS属性**

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

>[!NOTE]
>
>主对话框区域支持可选的`state`属性选择器。 在提交电子邮件表单且对话框显示确认消息时，它被设置为`sendsuccess`。 只要确认消息较小，就可以使用此属性选择器来减小显示此类确认消息时的对话框高度。

示例 — 要将主对话框区域最初设置为高度300像素，在显示确认消息时设置为高度100像素，具有十像素边距，并使用白色背景：

```
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

所有表单内容（如标签和输入字段）都驻留在由以下CSS类选择器控制的容器中：

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody
```

如果此容器的高度看起来比主对话框区域大，则组件会自动启用垂直滚动。

对话框正文的&#x200B;**CSS属性**

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
.s7ecatalogviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

对话框表单是逐行填充的，其中每一行都带有表单内容的一部分（如标签和文本输入字段）。 使用以下CSS类选择器控制单个表单行：

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogline
```

对话框行&#x200B;**的** CSS属性

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置对话框表单，使每行有十个像素填充：

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

对话框表单中的所有静态标签均由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialoglabel
```

此类不适合控制标签大小或位置，因为您可以将其应用于表单用户界面各个位置的文本。

对话框标签的&#x200B;**CSS属性。 &#x200B;**

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

可以本地化对话框标签。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 要将所有标签设置为灰色、粗体、九像素字体：

```
.s7ecatalogviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

所有显示在表单输入字段左侧的静态标签都受以下控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputlabel
```

对话框输入标签的&#x200B;**CSS属性**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>静态标签的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">文本对齐</span> </p> </td> 
   <td colname="col2"> <p>水平文本对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p>静态标签边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>静态标签填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将输入字段标签设置为宽度为50像素，请右对齐，在右侧有10个像素的边距，并有10个像素的边距：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

每个表单输入字段都包装在容器中，以便您在输入字段周围应用自定义边框。 可使用以下CSS类选择器来控制分类：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer
```

对话框输入容器的&#x200B;**CSS属性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框</span> </p> </td> 
   <td colname="col2"> <p>输入字段容器周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>输入字段容器支持可选的`state`属性选择器。 当用户输入数据格式错误且内联验证失败时，它设置为`verifyerror`。 此属性选择器可用于突出显示表单中错误的用户输入。

从对话框主体的左边缘到右边缘的标签展开的大多数输入字段（包括“发件人”字段和“消息”字段）均由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputwide
```

对话框输入范围字段的&#x200B;**CSS属性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>输入字段宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

“收件人”字段比较窄，因为它为右侧的删除电子邮件按钮分配了空间。 可使用以下CSS类选择器来控制分类：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputshort
```

对话框输入短字段的&#x200B;**CSS属性**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>输入字段宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将表单设置为在所有输入字段周围使用1像素灰色边框和9像素填充。 对于验证失败的字段，使用相同的红色边框。 到字段宽250像素。 最后，其余输入字段宽度为300像素：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

电子邮件输入字段也可通过以下进行控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialogmessage
```

此类允许您为基础`TEXTAREA`元素设置特定属性。

**对话框消息的CSS属性**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>消息高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自动换行</span> </p> </td> 
   <td colname="col2"> <p>文字环绕样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将电子邮件设置为50像素高并使用`break-word`单词换行：

```
.s7ecatalogviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

“添加其他电子邮件地址”按钮允许用户在电子邮件表单中添加多个收件人。 可使用以下CSS类选择器来控制分类：

```
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton
```

**对话框的CSS属性添加电子邮件地址按钮**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>每个状态的按钮图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p>按钮图像在按钮区域中的位置。 </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>按钮内的文本高度。 影响垂直对齐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">文本对齐</span> </p> </td> 
   <td colname="col2"> <p>水平文本对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 要将“Add Another Email Address”按钮设置为25像素高，请使用具有右对齐方式的12点粗体字体，并为每种状态使用不同的文本颜色和图像：

```
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

删除按钮允许用户从电子邮件表单中删除额外的地址。 可使用以下CSS类选择器来控制分类：

```
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton
```

**对话框的CSS属性删除电子邮件按钮**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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
   <td colname="col2"> <p>每个状态的按钮图像。 </p> </td> 
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

示例 — 要将“删除”按钮设置为25 x 25像素，并为每种状态使用不同的图像：

```
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

要共享的内容显示在对话框主体的底部，并包括缩略图、标题、源URL和描述。 它将被包装到一个容器中，该容器由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

对话框内容的&#x200B;**CSS属性**

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框</span> </p> </td> 
   <td colname="col2"> <p>容器边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置底部容器具有一个像素点状边框并且没有边距：

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

使用以下CSS类选择器控制缩略图图像：

```
.s7ecatalogviewer .s7emaildialog .s7dialogthumbnail
```

`background-image`属性由组件逻辑设置。

对话框缩略图图像的&#x200B;**CSS属性**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
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
   <td colname="col1"> <p> <span class="codeph">垂直对齐</span> </p> </td> 
   <td colname="col2"> <p>垂直对齐缩略图。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将缩略图设置为90 x 60像素，并使用10个像素进行顶部对齐：

```
.s7ecatalogviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

内容标题、源和描述进一步分组到内容缩略图右侧的面板中。 可使用以下CSS类选择器来控制分类：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginfopanel
```

对话框信息面板的&#x200B;**CSS属性**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>面板宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将内容信息面板的宽度设置为300像素：

```
.s7ecatalogviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

使用以下CSS类选择器控制内容标题：

```
.s7ecatalogviewer .s7emaildialog .s7dialogtitle
```

对话框标题的&#x200B;**CSS属性**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p>外边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将内容标题设置为使用粗体字体并具有十像素边距，请执行以下操作：

```
.s7ecatalogviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

使用以下CSS类选择器控制内容来源：

```
.s7ecatalogviewer .s7emaildialog .s7dialogorigin
```

对话框内容源&#x200B;**的**&#x200B;CSS属性

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p>外边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将内容原点设置为具有十像素边距，请执行以下操作：

```
.s7ecatalogviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

使用以下CSS类选择器控制内容描述：

```
.s7ecatalogviewer .s7emaildialog .s7dialogdescription
```

**对话框内容描述的CSS属性**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p>外边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将内容描述设置为具有十像素边距并使用九点字体：

```
.s7ecatalogviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

当用户输入不正确的输入数据时，内联验证失败。 或者，如果对话框在提交表单时必须显示错误或确认消息，则对话框正文的顶部会显示消息。 可使用以下CSS类选择器来控制分类：

```
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage
```

**对话框的CSS属性错误消息**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 错误图标。 缺省值为感叹号。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 错误图标在消息区域中的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>消息文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行高</span> </p> </td> 
   <td colname="col2"> <p> 消息中的文本高度。 影响垂直对齐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此消息支持具有以下可能值的`state`属性选择器： `verifyerror`、`senderror`和`sendsuccess`。 由于内联输入验证失败而显示消息时设置值`verifyerror`。 当后端电子邮件服务报告错误时设置值`senderror`。 成功发送电子邮件时设置值`sendsuccess`。 这样，就可以根据对话框状态对消息设置不同的样式。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 要设置消息以使用10点粗体字体，行高为25像素，左侧填充为20像素，并使用感叹号图标。 最后，如果出现错误，则显示红色文本；如果成功，则显示无图标和绿色文本：

```
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

如果需要垂直滚动，则滚动条将在对话框右边缘附近的面板中呈现，该面板可通过以下CSS类选择器进行控制：

```
.s7ecatalogviewer .s7emaildialog .s7dialogscrollpanel
```

对话框滚动面板的&#x200B;**CSS属性**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>滚动面板宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将滚动面板的宽度设置为44像素：

```
.s7ecatalogviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

滚动条区域的外观可通过以下CSS类选择器来控制：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar
```

滚动条的&#x200B;**CSS属性**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 滚动条宽度。 </p> </td> 
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

示例 — 设置一个宽度为28像素的滚动条，该滚动条在滚动面板的顶部、右侧和底部各有8个像素的边距：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

滚动条轨道是上下滚动按钮之间的区域。 组件会自动设置轨道的位置和高度。 使用以下CSS类选择器控制跟踪：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

滚动轨道的&#x200B;**CSS属性**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
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

示例 — 设置宽度为28像素且背景为灰色的滚动条轨道：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

滚动条缩略图在滚动轨道区域内垂直移动。 其垂直位置完全由组件逻辑控制，但缩略图高度不会根据内容量动态变化。 您可以使用以下CSS类选择器配置缩略图高度和其他方面：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

滚动条缩略图的&#x200B;**CSS属性**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
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
   <td colname="col2"> <p> 轨道底部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>为给定缩略图状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态： `up`、`down`、`over`和`disabled`。

示例 — 设置滚动条缩览图，其大小为28 x 45像素，顶部和底部有10像素边距，并且每种状态具有不同的图稿：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

顶部和底部滚动按钮的外观可通过以下CSS类选择器进行控制：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

无法使用CSS `top`、`left`、`bottom`和`right`属性定位滚动按钮。 相反，查看器逻辑会自动定位它们。

顶部和底部滚动按钮的&#x200B;**CSS属性**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
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
>这些按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态： `up`、`down`、`over`和`disabled`。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置具有28 x 32像素且每种状态有不同图稿的滚动按钮：

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
