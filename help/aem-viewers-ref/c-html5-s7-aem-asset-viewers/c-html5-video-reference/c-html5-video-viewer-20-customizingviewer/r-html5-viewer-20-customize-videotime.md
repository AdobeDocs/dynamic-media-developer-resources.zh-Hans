---
title: 视频时间
description: 视频时间是显示当前播放视频的当前时间和持续时间的数字显示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83491281-aff4-411a-a5a2-42e2454fd375
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# 视频时间{#video-time}

视频时间是显示当前播放视频的当前时间和持续时间的数字显示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

CSS可以控制的属性包括视频时间字体系列、字体大小和字体颜色。 还可以通过CSS将其相对于包含它的控制栏进行定位。

视频时间的外观由以下CSS类选择器控制：

```
.s7videoviewer .s7videotime
```

## 视频时间的CSS属性 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 视频时间控制的宽度。 Internet Explorer 8或更高版本需要此属性才能正常运行。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

将视频时间设置为浅灰色（十六进制） `#BBBBBB`)，大小为12像素，位于距离控制栏顶部15像素的位置，距离控制栏右边缘80像素的位置。

```
.s7videoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
