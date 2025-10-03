---
title: contentUrl
description: 所有查看者通用的参数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# contentUrl{#contenturl}

所有查看者通用的参数。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>指定自定义CSS文件、任何隐藏式字幕内容或导航内容的基本路径。 </p> <p>如果路径没有前导<span class="filepath"> /</span>，则它是相对于查看器HTML页面的位置的。 如果路径前置<span class="filepath"> /</span>，则它指定同一服务器上的绝对路径。 </p> <p> 在不指定样式命令时，不会影响默认CSS文件的加载。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

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

<!--

```
contentUrl=https://demos-pub.assetsadobe.com/
```

-->
