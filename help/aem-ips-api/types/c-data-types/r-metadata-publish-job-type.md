---
description: 将元数据发布到元数据服务器。
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic，SDK/API，元数据
role: Developer,Administrator
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
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
   <td colname="col3">设置为<span class="codeph"> True</span>可再次将<i>所有</i>数据发布到元数据服务器。 <p>注意： 根据数据量，这可能需要几分钟到几小时。 </p><p>如果只想发布新元数据或更改的元数据，请勿设置此参数。 </p></td> 
  </tr> 
 </tbody> 
</table>
