---
title: 链接共享
description: 链接共享工具由添加到“社交”共享面板的按钮以及激活该工具时显示的模式对话框组成。 按钮的位置完全由社交共享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 638ca6c2-375c-4162-b640-68aed6a8a9c6
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# 链接共享{#link-share}

链接共享工具由添加到“社交”共享面板的按钮以及激活该工具时显示的模式对话框组成。 按钮的位置完全由社交共享工具管理。

<!--RICK - Edit to distinguish from previous -->

链接共享按钮的外观由以下CSS类选择器控制：

```css{.line-numbers}
.s7video360viewer .s7linkshare
```

**链接共享工具的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS脚本 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 属性选择器，可用于将不同的外观应用于不同的按钮状态。

可以通过设置从Social共享面板中删除按钮 `display:none` CSS属性的CSS类。

按钮工具提示可以本地化。 请参阅 [用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

示例 — 设置一个28 x 28像素的链接共享按钮，并针对四种不同的按钮状态分别显示不同的图像：

```css {.line-numbers}
.s7video360viewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7video360viewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7video360viewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7video360viewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

使用以下CSS类选择器控制活动对话框时覆盖网页的背景叠加：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7backoverlay
```

**背景叠加的CSS属性**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>背景叠加不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>背景叠加颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**  — 要将背景叠加设置为具有70%不透明度的灰色，请执行以下操作：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

默认情况下，模式对话框会以桌面系统屏幕的中心位置显示，并在触控设备上显示整个网页区域。 在所有情况下，对话框的位置和大小都由组件管理。 使用以下CSS类选择器控制该对话框：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialog
```

**对话框的CSS属性**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> 对话框边框半径（如果对话框不占用整个浏览器）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>对话框背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>应取消设置或设置为100%，在这种情况下，对话框会占用整个浏览器窗口（触控设备首选此模式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>应取消设置或设置为100%，在这种情况下，对话框会占用整个浏览器窗口（触控设备首选此模式）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**  — 设置对话框以使用整个浏览器窗口并在触控设备上使用白色背景：

```css {.line-numbers}
.s7video360viewer.s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

对话框标题由图标、标题文本和关闭按钮组成。 标头容器由以下CSS类选择器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader
```

**对话框标题的CSS属性**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p> 标题内容的内部边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

图标和标题文本将封装到由以下CSS类选择器控制的额外容器中：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline
```

**对话框行的CSS属性**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p> 标题图标和标题的内边距 </p> </td> 
  </tr> 
 </tbody> 
</table>

标题图标由以下CSS类选择器控制

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheadericon
```

**对话框标题图标的CSS属性**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>图标高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>图标图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS脚本 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

标题标题由以下CSS类选择器控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheadertext
```

**对话框标题文本的CSS属性**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p>内部文本边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用以下CSS类选择器控制“关闭”按钮：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7closebutton
```

**关闭按钮的CSS属性**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> 相对于标题容器的垂直按钮位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 相对于标题容器的水平按钮位置。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p>按钮的内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>每个状态的按钮图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS脚本 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 属性选择器，可用于将不同的外观应用于不同的按钮状态。

可以本地化“关闭”按钮工具提示和对话框标题。 请参阅 [用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**示例**  — 要设置带内边距的对话框标题，请用22 x 12像素图标（粗体的16点标题）来设置。 最后，一个28 x 28像素的“关闭”按钮，它位于对话框容器顶部两个像素和右侧两个像素的位置：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7video360viewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

对话框页脚包含一个“取消”按钮。 使用以下CSS类选择器控制页脚容器：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter
```

**对话框页脚的CSS属性**

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边框 </span> </p> </td> 
   <td colname="col2"> <p> 可用于在视觉上分隔页脚和对话框其余部分的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

页脚有一个内部容器，用于保存按钮。 可使用以下CSS类选择器来控制分类：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer
```

**对话框按钮容器的CSS属性**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p> 页脚和按钮之间的内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

使用以下CSS类选择器可控制全选按钮：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogactionbutton
```

该按钮仅在桌面系统上可用。

**全选按钮的CSS属性**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 颜色 </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>全选按钮支持 `state` 属性选择器，可用于将不同的外观应用于不同的按钮状态。

使用以下CSS类选择器可控制“取消”按钮：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogcancelbutton
```

**对话框取消按钮的CSS属性**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 颜色 </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 每个状态的按钮背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 属性选择器，可用于将不同的外观应用于不同的按钮状态。

此外，这两个按钮共享一个通用的CSS类，该类可以包含与其他对话框按钮相同的CSS设置：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button
```

**按钮的CSS属性**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>按钮字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 盒阴影 </span> </p> </td> 
   <td colname="col2"> <p>投影。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右边距 </span> </p> </td> 
   <td colname="col2"> <p>右按钮边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化按钮工具提示。 请参阅 [用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**示例**  — 使用64 x 34“取消”按钮设置对话框页脚，该按钮具有每种按钮状态不同的文本颜色和背景颜色：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

主对话框区域位于页眉和页脚之间，包含对话框内容。 在任何情况下，组件都管理此区域的宽度 — 无法在CSS中设置此区域。 主对话框区域由以下CSS类选择器控制：

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogviewarea
```

**对话框查看区域的CSS属性**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p> 主对话框区域的高度。 仅当对话框在桌面模式下工作时，才应指定它。 当调整对话框的大小以占据整个浏览器窗口时，此选项不适用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>主对话框区域的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p>外边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**  — 要将主对话框区域设置为300像素高度，具有10像素边距，并使用白色背景：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

所有表单内容（如标签和输入字段）都驻留在由以下CSS类选择器控制的容器中：

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialogbody
```

**对话框正文的CSS属性**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**  — 要将表单内容设置为具有十像素填充，请执行以下操作：

```css {.line-numbers}
.s7interactivevideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

对话框表单中的所有静态标签都由控制

```
.s7video360viewer .s7linkdialog .s7dialoglabel
```

此类不适合控制标签大小或位置，因为您可以将其应用于表单用户界面各个位置的文本。

**对话框标签的CSS属性**

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>标签字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>标签字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>标签字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 颜色 </span> </p> </td> 
   <td colname="col2"> <p>标签文本颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化对话框标签。 请参阅 [用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**示例**  — 将所有标签设置为灰色，粗体带九像素字体：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

显示在链接顶部的文本副本的大小可通过以下CSS类选择器进行控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputwide
```

**对话框输入范围字段的CSS属性**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>文本宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**  — 将文本副本的宽度设置为430像素，并在底部填充10像素：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

共享链接将封装在容器中，并使用以下CSS类选择器进行控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputcontainer
```

**对话框输入容器的CSS属性**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边框 </span> </p> </td> 
   <td colname="col2"> <p>共享链接容器周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 </span> </p> </td> 
   <td colname="col2"> <p>内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**  — 要在嵌入代码文本周围设置一个像素灰色边框，并且边框间距为9像素，请执行以下操作：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

共享链接本身可通过以下CSS类选择器进行控制：

```css {.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglink
```

**对话框共享链接的CSS属性**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>共享链接宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**  — 将共享链接设置为450像素宽：

```css{.line-numbers}
.s7video360viewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
