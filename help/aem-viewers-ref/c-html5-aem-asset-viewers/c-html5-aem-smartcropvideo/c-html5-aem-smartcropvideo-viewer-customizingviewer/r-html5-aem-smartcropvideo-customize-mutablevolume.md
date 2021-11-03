---
title: 可变卷
description: 可变音量控件最初显示为一个按钮，允许用户将智能裁剪视频播放器的声音静音或取消静音。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: bd86af60-a9a0-4f2e-9d36-f7ee22bd8c8e
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 2%

---

# 可变卷{#mutable-volume}

可变音量控件最初显示为一个按钮，允许用户将智能裁剪视频播放器的声音静音或取消静音。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

当用户滚动按钮时，会显示一个滑块，允许用户设置音量。 可变音量控件可以通过CSS相对于包含它的控制栏进行大小调整、外观设置和定位。

可变卷区域的外观由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7mutablevolume
```

**可变卷的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 从上边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 从右边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 可变音量控件的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>可变音量控制的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 可变音量控件的颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

通过以下CSS类选择器控制静音/取消静音按钮的外观：

```
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton
```

您可以控制每个按钮状态的背景图像。 按钮的大小继承自卷控件的大小。

**按钮图像的CSS属性**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>请参阅 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 和 `selected` 属性选择器，可用于将不同的外观应用于不同的按钮状态。 特别是， `selected='true'` 对应于“静音”状态和 `selected='false'` 对应于“未静音”状态。

使用以下CSS类选择器控制垂直音量条区域：

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume
```

**垂直卷条区域的CSS属性**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 垂直音量的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p> 垂直体积块的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p> 垂直体积的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

垂直卷控件内的跟踪通过以下CSS类选择器进行控制：

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**垂直卷控件的CSS属性**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> 垂直音量控件的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

通过以下CSS类选择器控制垂直音量旋钮：

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**垂直音量控制旋钮的CSS属性**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p> 垂直音量控制旋钮图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>请参阅 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度 </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>垂直音量控制旋钮的水平位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

按钮工具提示可进行本地化。 请参阅 [用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以了解更多信息。

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置一个静音按钮，该按钮为32 x 32像素，距顶部6像素，距控制栏右边缘38像素。 选择或未选择时，针对四个不同按钮状态中的每个状态显示不同的图像。

```
.s7smartcropvideoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

以下示例说明了如何在可变音量控件中设置音量滑块的样式。

```
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7smartcropvideoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

以下示例说明了如何自定义视频播放器，以便在播放过程中禁用声音。 将以下代码添加到查看器的嵌入代码中：

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

在上述代码示例中，卷级别设置为 `0` 在 `mutableVolume` 组件。 然后，同一组件将被停用，因此最终用户无法使用该组件。
