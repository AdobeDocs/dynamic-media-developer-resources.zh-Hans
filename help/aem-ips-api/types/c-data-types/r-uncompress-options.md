---
description: 上传设置可将ZIP和TAR文件作为主资源进行处理（无），或提取并上传其内容（解压缩）。
solution: Experience Manager
title: UnCompressOptions
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---


# UnCompressOptions{#uncompressoptions}

上传设置可将ZIP和TAR文件作为主资源进行处理（无），或提取并上传其内容（解压缩）。

>[!NOTE]
>
>`None` 。

## 参数 {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 过程</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>控制ZIP和TAR存档文件处理。 提供2个选项： 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> 无：处</span> 理为主资产。 </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> UnCompress：提</span> 取和处理内容。 </li>
     </ul><p>注意：字符串常量区分大小写。 使用<span class="codeph"> UnCompress</span>，而不是<span class="codeph">解压缩</span>或<span class="codeph"> unCompress</span>。 </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## 由{#section-b2a829cf5511412e968bb2000f85cc31}使用

`unCompressionOptions`类型由：

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

