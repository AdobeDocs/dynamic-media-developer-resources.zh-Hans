---
description: 为您的视频生成缩略图图像。
solution: Experience Manager
title: 媒体选项
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f37d935d-fe74-4878-8477-d2144d58d982
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# [!DNL MediaOptions]{#mediaoptions}

为您的视频生成缩略图图像。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：HandleArray</span> </td> 
   <td colname="col3">一个数组 <span class="codeph"> 属性集</span> 处理引用视频编码预设以转码视频。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 如果为true，则提取视频的第一帧，并将其用作缩略图。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailoptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：缩略图选项</span> </td> 
   <td colname="col3">可选. 允许您选择特定的视频帧作为缩略图图像。 <p>要指定缩略图图像，请为要使用的帧传递时间（从视频开始起算的毫秒数）。 值范围从0到视频的结尾。 <p>注意：如果指定的时间不正确， <span class="codeph"> generateThumbnail</span> 默认为true。 </p></p><p>参见 <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> 缩略图选项</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## 使用者 {#section-87cb83407198432c95eaa2db9f12f9db}

此 `mediaOptions` 类型由以下人员使用：

* [上载目录作业](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPost作业](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
