---
description: 所有查看器通用的参数。
seo-description: 所有查看器通用的参数。
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
topic: Dynamic Media
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# serverUrl{#serverurl}

所有查看器通用的参数。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>相对或绝对图像服务根路径。 </p> <p> 指定图像服务的相对或绝对路径，查看器从中检索图像。 如果路径没有前导<span class="filepath"> /</span>，则它相对于查看器HTML页面的位置。 如果路径具有前导<span class="filepath"> /</span> ，则它指定同一服务器上的绝对路径。 </p> <p> 在查看器中启用电子邮件共享模块时，请仅使用绝对路径。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选。标准SaaS（软件即服务）使用不需要。

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

