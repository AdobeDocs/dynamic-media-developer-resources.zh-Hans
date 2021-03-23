---
description: 允许您选择特定视频帧作为缩略图图像的可选类型。
seo-description: 允许您选择特定视频帧作为缩略图图像的可选类型。
seo-title: ThumbnailOptions
solution: Experience Manager
title: ThumbnailOptions
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 5%

---


# ThumbnailOptions{#thumbnailoptions}

允许您选择特定视频帧作为缩略图图像的可选类型。

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
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>设置要用于视频缩略图的帧的时间(以视频开始的毫秒为单位)。 值范围从0到视频末尾。 <p>注意：如果您指定的时间不正确，系统会将视频的第一帧用作缩略图。 请参阅<a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>。 </p></p> </td> 
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

