---
title: UnCompressOptions
description: 上载设置，用于将ZIP和TAR文件作为主资产进行处理（无）或者提取并上载其内容（解压缩）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 89222959-3701-4ea6-bcae-98ceec93764f
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# [!DNL UnCompressOptions]{#uncompressoptions}

上载设置，用于将ZIP和TAR文件作为主资产进行处理（无）或者提取并上载其内容（解压缩）。

>[!NOTE]
>
>设置`None`为默认设置。

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
   <td colname="col1"> <span class="codeph"> <span class="varname">进程</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>控制ZIP和TAR存档文件的处理。 它提供了两个选项： 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph">无：</span>作为主资产处理。 </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph">解压缩：</span>提取并处理内容。 </li>
     </ul><p>注意：字符串常量区分大小写。 使用<span class="codeph"> UnCompress</span>，而不是<span class="codeph"> uncompress</span>或<span class="codeph"> unCompress</span>。 </p></p> </td> 
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

## 使用者 {#section-b2a829cf5511412e968bb2000f85cc31}

`unCompressionOptions`类型由以下用户使用：

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
