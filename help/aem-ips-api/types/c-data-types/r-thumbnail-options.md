---
description: 一种可选类型，允许您选择特定的视频帧作为缩略图像。
solution: Experience Manager
title: 缩略图选项
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---

# [!DNL ThumbnailOptions]{#thumbnailoptions}

一种可选类型，允许您选择特定的视频帧作为缩略图像。

语法

## 参数 {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：long</span> </td> 
   <td colname="col3"> <p>为要用于视频缩略图的帧设置时间（以自视频开始后的毫秒为单位）。 值的范围从0到视频的结尾。 <p>注意：如果您指定的时间不正确，系统将使用视频的第一帧作为缩略图。 请参阅<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```
