---
title: 题注
description: 视频查看器的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 5%

---

# 题注{#caption}

视频查看器的URL命令。

` caption= *`文件`*[,0|1]`

查看器支持通过托管的WebVTT文件使用隐藏式字幕。 不支持重叠提示和区域。 支持的提示定位运算符包括：

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>鍵 </p> </th> 
   <th colname="col2" class="entry"> <p>名称 </p> </th> 
   <th colname="col3" class="entry"> <p>值 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>文本对齐 </p> </td> 
   <td colname="col3"> <p><span class="codeph">左|右|中|开始|结束</span> </p> </td> 
   <td colname="col4"> <p> 控制文本对齐方式。 </p> <p>默认值为<span class="codeph">中间</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>文本位置 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 注解文本开头插入VideoPlayer组件中的百分比。 </p> <p>默认值为0%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>行大小 </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> 用于字幕的视频宽度的百分比。 </p> <p>默认值为100%。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>行位置 </p> </td> 
   <td colname="col3"> <p> 0%-100%|整数 </p> </td> 
   <td colname="col4"> <p> 确定页面上的行位置。 </p> <p>如果以整数形式表示（无百分比符号），则它是文本显示位置上方的行数。 </p> <p>如果它是一个百分比（百分比符号是最后一个字符），则说明文本在显示区域以百分比向下显示。 </p> <p>默认值为100%。 </p> </td> 
  </tr> 
 </tbody> 
</table>

不支持WebVTT文件中存在的其他WebVTT功能，但不应中断字幕。

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">文件</span></span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT描述内容的URL或路径。 通过ImageServing提供WebVTT文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 指定默认字幕状态（启用为<span class="codeph"> 1</span>）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
