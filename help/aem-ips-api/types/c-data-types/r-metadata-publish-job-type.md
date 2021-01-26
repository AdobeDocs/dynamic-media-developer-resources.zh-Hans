---
description: 将元数据发布到元数据服务器。
seo-description: 将元数据发布到元数据服务器。
seo-title: MetadataPublishJobType
solution: Experience Manager
title: MetadataPublishJobType
topic: Dynamic Media Image Production System API
uuid: 14cbb67e-56dc-4a25-b871-740be7ea7858
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 9%

---


# MetadataPublishJobType{#metadatapublishjobtype}

将元数据发布到元数据服务器。

语法

## 参数 {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">设置为<span class="codeph"> True</span>可再次将<i>所有</i>数据发布到元数据服务器。 <p>注意： 根据数据量，这可能需要几分钟到几小时。 </p><p>如果仅要发布新的或更改的元数据，请不要设置此参数。 </p></td> 
  </tr> 
 </tbody> 
</table>

