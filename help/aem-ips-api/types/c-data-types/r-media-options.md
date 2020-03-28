---
description: 为视频生成缩略图。
seo-description: 为视频生成缩略图。
seo-title: 媒体选项
solution: Experience Manager
title: 媒体选项
topic: Scene7 Image Production System API
uuid: 4de59678-1bef-484c-9a43-ded531537aeb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 媒体选项{#mediaoptions}

为视频生成缩略图。

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
   <td colname="col1"> <span class="codeph"> videoEncodingPresetsArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">引用视频编码预 <span class="codeph"></span> 设以转码视频的一组PropertySet句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 如果为true，则提取视频的第一帧并用作缩略图图像。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 缩 <span class="varname"> 略图选项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:ThumbnailOptions</span> </td> 
   <td colname="col3">可选。允许您选择要用作缩略图的特定视频帧。 <p>要指定缩略图图像，请传递要使用的帧的时间(以视频开始的毫秒为单位)。 值的范围从0到视频结尾。 <p>注意：如果指定时间不正确，则 <span class="codeph"> 生成Thumbnail</span> 默认值为true。 </p></p><p>请参阅 <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> 缩略图选项</a>。 </p></td> 
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

类 `mediaOptions` 型由以下用户使用：

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

