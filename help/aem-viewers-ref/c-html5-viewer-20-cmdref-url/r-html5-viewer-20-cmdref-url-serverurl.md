---
title: serverUrl
description: 所有檢視器通用的引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# serverUrl{#serverurl}

所有檢視器通用的引數。

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>相對或絕對的「影像伺服」根路徑。 </p> <p> 指定「影像伺服」的相對或絕對路徑，檢視器會從中擷取影像。 如果路徑沒有行距 <span class="filepath"> /</span>，此量度會與檢視器HTML頁面的位置相對應。 如果路徑有行距 <span class="filepath"> /</span>，會指定相同伺服器上的絕對路徑。 </p> <p> 在檢視器中啟用電子郵件共用模組時，僅使用絕對路徑。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选. 標準SaaS （軟體即服務）使用不需要。

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
