---
description: 將中繼資料發佈至中繼資料伺服器。
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 10%

---

# [!DNL MetadataPublishJobType]{#metadatapublishjobtype}

將中繼資料發佈至中繼資料伺服器。

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
   <td colname="col3">設定為 <span class="codeph"> True</span> 以發佈 <i>全部</i> 再次將資料傳送到中繼資料伺服器。 <p>注意：視資料量而定，這可能需要幾分鐘到幾小時的時間。 </p><p>如果您只想發佈新或變更的中繼資料，請勿設定此引數。 </p></td> 
  </tr> 
 </tbody> 
</table>
