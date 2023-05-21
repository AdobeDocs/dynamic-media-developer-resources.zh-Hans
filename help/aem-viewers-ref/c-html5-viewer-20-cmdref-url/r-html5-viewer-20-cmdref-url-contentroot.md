---
title: contentUrl
description: 所有檢視器通用的引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# contentUrl{#contenturl}

所有檢視器通用的引數。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>指定自訂CSS檔案、任何隱藏式字幕內容或導覽內容的基本路徑。 </p> <p>如果路徑沒有行距 <span class="filepath"> /</span>，此量度會與檢視器HTML頁面的位置相對應。 如果路徑有行距 <span class="filepath"> /</span>，會指定相同伺服器上的絕對路徑。 </p> <p> 若您未指定樣式指令，不會影響預設CSS檔案的載入。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选.

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```
