---
description: 所有查看器通用的参数。
seo-description: 所有查看器通用的参数。
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
feature: Dynamic Media Classic，查看器，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---


# contentUrl{#contenturl}

所有查看器通用的参数。

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>指定自定义CSS文件、任何隐藏字幕内容或导航内容的基本路径。 </p> <p>如果路径没有前导<span class="filepath"> /</span>，则路径相对于查看器HTML页面的位置。 如果路径具有行距<span class="filepath"> /</span>，则它指定同一服务器上的绝对路径。 </p> <p> 不指定样式命令时，不影响默认CSS文件的加载。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-10ee45d637134e0fbcd943c62578cb78}

可选。

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

