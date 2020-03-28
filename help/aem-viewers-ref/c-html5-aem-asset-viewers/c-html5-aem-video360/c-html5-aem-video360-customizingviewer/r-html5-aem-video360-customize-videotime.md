---
description: 视频时间是显示当前播放的视频的当前时间和持续时间的数字显示。
seo-description: 视频时间是显示当前播放的视频的当前时间和持续时间的数字显示。
seo-title: 视频时间
solution: Experience Manager
title: 视频时间
topic: Dynamic media
uuid: f8ba615f-661a-4750-bdf7-559650d464af
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video time{#video-time}

视频时间是显示当前播放的视频的当前时间和持续时间的数字显示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

视频时间字体系列、字体大小和字体颜色是CSS可以控制的属性之一。 CSS还可以相对于包含该控件的控件栏定位它。

视频时间的外观由以下CSS类选择器控制：

```
.s7video360viewer .s7videotime
```

## 视频时间的CSS属性 {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从上边框开始的位置，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>从右边框开始的位置，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 视频时间控件的宽度。 Internet Explorer 8或更高版本需要此属性才能正常工作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小 </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>用于时间显示文本的字体颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** -将视频时间设置为浅灰色(十六进制 `#BBBBBB`)，大小为12像素，距控件栏顶部15像素，距控件栏顶部和右边缘80像素。

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```

