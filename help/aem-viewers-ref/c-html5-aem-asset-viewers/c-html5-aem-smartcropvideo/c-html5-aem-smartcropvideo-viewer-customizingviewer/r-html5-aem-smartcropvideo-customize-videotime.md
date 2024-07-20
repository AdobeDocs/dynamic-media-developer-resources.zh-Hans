---
title: 视频时间
description: 视频时间是显示当前播放视频的当前时间和持续时间的数字显示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0ef09f06-c2d5-4c84-8ff9-4e94e9e54d40
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# 视频时间{#video-time}

视频时间是显示当前播放视频的当前时间和持续时间的数字显示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

视频时间字体系列、字体大小和字体颜色是CSS可以控制的属性。 还可以通过CSS将其相对于包含它的控制栏进行定位。

视频时间的外观可通过以下CSS类选择器进行控制：

```
.s7smartcropvideoviewer .s7videotime
```

## 视频时间的CSS属性 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>上边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>从右边框定位，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 视频时间控件的宽度。 Internet Explorer 8或更高版本需要此属性才能正常运行。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

将视频时间设置为浅灰色（十六进制`#BBBBBB`），大小为12像素，位置从控制栏顶部起15像素，从控制栏右边缘起80像素。

```
.s7smartcropvideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
