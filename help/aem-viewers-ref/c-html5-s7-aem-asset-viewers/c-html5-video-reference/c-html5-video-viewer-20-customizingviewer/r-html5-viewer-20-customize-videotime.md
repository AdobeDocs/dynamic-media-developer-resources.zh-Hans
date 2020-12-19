---
description: 视频时间是显示当前播放的视频的当前时间和持续时间的数字显示。
seo-description: 视频时间是显示当前播放的视频的当前时间和持续时间的数字显示。
seo-title: 视频时间
solution: Experience Manager
title: 视频时间
topic: Dynamic media
uuid: a15b069a-18c8-428f-ac6f-ab5aeda65f4d
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 2%

---


# 视频时间{#video-time}

视频时间是显示当前播放的视频的当前时间和持续时间的数字显示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

视频时间字体系列、字体大小和字体颜色是CSS可以控制的属性之一。 它还可以由CSS相对于包含它的控件栏进行定位。

视频时间的外观由以下CSS类选择器控制：

```
.s7videoviewer .s7videotime
```

## 视频时间{#css-properties-of-video-time}的CSS属性

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从上边框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从右边框定位，包括边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 视频时间控件的宽度。 Internet Explorer 8或更高版本需要此属性才能正常工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

将视频时间设置为浅灰色（十六进制`#BBBBBB`），大小为12像素，距控制栏顶部15像素，距控制栏右边缘80像素。

```
.s7videoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

