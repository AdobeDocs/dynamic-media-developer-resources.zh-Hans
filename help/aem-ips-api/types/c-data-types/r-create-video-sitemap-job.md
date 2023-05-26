---
description: 创建视频站点地图。
solution: Experience Manager
title: CreateVideoSitemapJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2af7c949-46cf-4570-9043-1b6296a2e467
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 14%

---

# [!DNL CreateVideoSitemapJob]{#createvideositemapjob}

创建视频站点地图。

语法

## 参数 {#section-21fbc2712d6d499b8249f4ef256016a9}

<table id="table_7B459A9D55CE49A38D8A77CBD229033A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forceUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">设置为时生成网站地图 <span class="codeph"> true</span>. <p><p>注意：如果Sitemap生成配置设置为手动，并且 <span class="codeph"> forceUpdate</span> 未设置，将不会生成站点地图。 </p></p></td> 
  </tr> 
 </tbody> 
</table>
