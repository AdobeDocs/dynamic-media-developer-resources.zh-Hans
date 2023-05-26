---
title: “向左旋转”按钮
description: 单击或点按此按钮可将图像在主视图的左侧旋转。 为了节省屏幕空间，此按钮不显示在手机上。 此外，当使用多维旋转集时，按钮是隐藏的。 您可以使用CSS调整按钮的大小、外观和位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0c7ca422-f4ac-4ad1-ab51-8521b4d4b20e
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 4%

---

# “向左旋转”按钮{#spin-left-button}

选择此按钮可将图像在主视图的左侧旋转。 为了节省屏幕空间，此按钮不显示在手机上。 此外，当使用多维旋转集时，按钮是隐藏的。 您可以使用CSS调整按钮的大小、外观和位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**旋转按钮的CSS属性**

按钮将添加到由CSS类选择器进行DIV控制的内部容器中：

```
.s7mixedmediaviewer .s7spinbuttons
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
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>上边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从右边框定位，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>左边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从下边框定位，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此按钮在容器中的外观由CSS类选择器控制：

```
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton
```

<table id="table_3EC45539877A479DB83E8FC69142450B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>上边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从右边框定位，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>左边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从下边框定位，包括内边距。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite内。 </p> <p>参见 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS脚本 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 属性选择器，可用于将不同的外观应用于不同的按钮状态。

可对按钮工具提示进行本地化。 参见 [用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 了解更多信息。

示例 — 设置一个28 x 28像素的左旋转按钮，该按钮位于内部容器的左边缘。 最后，为四种不同的按钮状态分别显示不同的图像：

```
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton { 
 position:absolute; 
 left: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='up'] { 
background-image:url(images/v2/SpinLeftButton_light_up.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='over'] { 
background-image:url(images/v2/SpinLeftButton_light_over.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='down'] { 
background-image:url(images/v2/SpinLeftButton_light_down.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='disabled'] { 
background-image:url(images/v2/SpinLeftButton_light_disabled.png); 
}
```
