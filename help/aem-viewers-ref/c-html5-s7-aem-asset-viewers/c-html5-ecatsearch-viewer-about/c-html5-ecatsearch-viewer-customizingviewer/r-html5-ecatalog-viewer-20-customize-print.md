---
description: 打印工具由添加到控制栏的按钮和激活工具时显示的模态对话框组成。
seo-description: 打印工具由添加到控制栏的按钮和激活工具时显示的模态对话框组成。
seo-title: 打印
solution: Experience Manager
title: 打印
uuid: 7be047d8-d1be-4bda-90ca-6b55c749cc64
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 2%

---


# 打印{#print}

打印工具由添加到控制栏的按钮和激活工具时显示的模态对话框组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

使用以下CSS类选择器控制打印按钮的外观：

```
.s7ecatalogsearchviewer .s7print
```

**打印按钮的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上边距  </span> </p> </td> 
   <td colname="col2"> <p> 从控制栏顶部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距左  </span> </p> </td> 
   <td colname="col2"> <p> 到左边下一个按钮的距离；如果这是行中的第一个按钮，则指向控制栏的左侧。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置一个28 x 28像素的打印按钮，并针对四个不同按钮状态中的每个状态显示不同的图像。

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

使用以下CSS类选择器控制在对话框处于活动状态时覆盖网页的背景叠加：

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**背面叠加的CSS属性**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明  </span> </p> </td> 
   <td colname="col2"> <p> 背景叠加不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>背景叠加颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将背景叠加设置为灰色，不透明度为70%:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

默认情况下，模态对话框显示在桌面系统屏幕的中心位置。 该对话框的位置和大小由组件管理。该对话框由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**对话框的CSS属性**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> 对话框边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 对话框背景色； </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置具有灰色背景的对话框：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

对话框标题由图标、标题文本和关闭按钮组成。 标题容器通过以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
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

图标和标题文本将打包到其他容器中，并由以下各项控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**对话框行的CSS属性**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 标题图标和标题的内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题图标可通过以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**对话框标题图标的CSS属性**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高  </span> </p> </td> 
   <td colname="col2"> <p>图标高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>图标图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题通过以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
```

**对话框标题文本的CSS属性**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体权重  </span> </p> </td> 
   <td colname="col2"> <p>字体权重。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>字体高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内部文本填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用以下CSS类选择器控制“关闭”按钮：

```
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
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
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高  </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>按钮的内填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>每个状态的按钮图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同外观应用于不同的按钮状态。

可以本地化“关闭”按钮工具提示和对话框标题。 有关详细信息，请参阅[用户界面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置具有填充、22 x 22像素图标、粗体16点标题和28 x 28像素“关闭”按钮的对话框标题，该按钮位于距对话框容器顶部两个像素和距离对话框右侧两个像素的位置：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

对话框页脚由“取消”和“发送到打印”按钮组成。 页脚容器由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
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

页脚具有保留两个按钮的内容器。 它通过以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
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

使用以下CSS类选择器控制“取消”按钮：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
```

**对话框“取消”按钮的CSS属性**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同外观应用于不同的按钮状态。

“发送到打印”按钮由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**对话框操作按钮的CSS属性**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
   <td colname="col1"> <p> <span class="codeph"> 颜色  </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同外观应用于不同的按钮状态。

此外，两个按钮共享相同的通用CSS类，这些类可以包含对于其他对话框按钮相同的CSS设置：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
```

**按钮的CSS属性**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体权重  </span> </p> </td> 
   <td colname="col2"> <p>按钮字体权重。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>按钮字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>按钮字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行高  </span> </p> </td> 
   <td colname="col2"> <p> 按钮内的文本高度。 影响垂直对齐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 框 — 阴影  </span> </p> </td> 
   <td colname="col2"> <p>投影。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距右  </span> </p> </td> 
   <td colname="col2"> <p>右按钮边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化按钮工具提示。 有关详细信息，请参阅[用户界面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 要设置一个对话框的页脚，其中显示64 x 34 &quot;取消&quot;按钮和96 x 34 &quot;发送到打印&quot;按钮，并且每个按钮状态的文本颜色和背景颜色不同：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主对话框区域（在页眉和页脚之间）包含对话框内容。 在所有情况下，组件都管理此区域的宽度，无法在CSS中设置它。 主对话框区域由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**对话框查看区域的CSS属性**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高  </span> </p> </td> 
   <td colname="col2"> <p> 主对话框区域的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>主对话框区域的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>外边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置主对话框区域，使其具有自动计算的高度、十像素边距和白色背景：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

所有表单内容（如标签和输入字段）都驻留在由以下CSS类选择器控制的容器中：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

**对话框正文的CSS属性**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将表单内容设置为具有十个像素填充：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

对话框表单逐行填写，其中每行都包含表单内容的一部分（如标签和文本输入字段）。 使用以下CSS类选择器控制单个表单行：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**对话框行的CSS属性**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内线填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个对话框表单，使每行具有十个像素填充：

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

使用以下CSS类选择器控制对话框内容块的大小：

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**对话框输入宽度的CSS属性**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>块宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内线填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将内容块设置为430像素宽，并在底部填充10像素：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

对话框表单中的所有静态标签都通过以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

此类不适于控制标签大小或位置，因为您可以将它应用于表单用户界面中不同位置的文本。

**对话框标签的CSS属性。 **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体权重  </span> </p> </td> 
   <td colname="col2"> <p>标签字体权重。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>标签字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>标签字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 颜色  </span> </p> </td> 
   <td colname="col2"> <p>标签文本颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化对话框标签。 有关详细信息，请参阅[用户界面元素本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 将所有标签设置为灰色、粗体，字体为9像素：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

输入控件打包到容器中，并使用以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**对话框输入容器的CSS属性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左边距  </span> </p> </td> 
   <td colname="col2"> <p>内填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 从对话框的左边缘设置30像素填充。

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

单选按钮及其题注文本可通过以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**对话框选项的CSS属性**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p> 带题注的单选按钮的总宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 颜色  </span> </p> </td> 
   <td colname="col2"> <p>题注文本颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

单选按钮及其题注之间的间距由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**对话框选项输入的CSS属性**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距右  </span> </p> </td> 
   <td colname="col2"> <p> 单选按钮与其题注之间的间距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用以下CSS类选择器控制打印范围选择的数字选择器

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**对话框打印范围的CSS属性**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p> 数字选取器的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距  </span> </p> </td> 
   <td colname="col2"> <p> 数字选取器周围的间距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将所有单选按钮设置为150像素宽，带有黑色文本、10像素间距和42像素宽的数字拾取器：

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

使用以下CSS类选择器控制页面范围选择部分和打印布局部分之间的水平分隔线：

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**水平分隔线的CSS属性**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 分隔线周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>内填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>分隔线宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距  </span> </p> </td> 
   <td colname="col2"> <p>外边距 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置430像素宽的灰色分隔线，其两侧垂直边距为10像素，顶部边距为10像素：

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```

