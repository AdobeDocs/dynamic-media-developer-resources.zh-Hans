---
title: videoServerUrl
description: 所有查看者通用的参数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# videoServerUrl{#videoserverurl}

所有查看者通用的参数。

>[!NOTE]
>
>此命令不适用于视频图像查看器。

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 视频服务器根路径。 如果没有指定域，则应用为页面提供服务的域。 标准URI路径解析在此处适用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选. 标准软件即服务使用不需要。

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
