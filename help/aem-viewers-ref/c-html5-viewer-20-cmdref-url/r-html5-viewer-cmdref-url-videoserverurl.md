---
description: 所有查看器通用的参数。
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---

# videoServerUrl{#videoserverurl}

所有查看器通用的参数。

>[!NOTE]
>
>此命令不适用于视频图像查看器。

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 视频服务器根路径。 如果未指定域，则将应用提供页面的域。 应用标准URI路径解析。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选。标准软件不需要作为服务使用。

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
