---
title: InitialFrame
description: InitialFrame
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 28b6b981-94f6-4136-b322-992e18d154db
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 10%

---

# InitialFrame{#initialframe}

` initialFrame= *`frame`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> frame</span></span> </p> </td> 
   <td colname="col2"> <p> 指定要在查看器加载时显示的零基跨页索引。 索引与横向模式下跨页的索引匹配。 如果将查看器旋转为纵向，则查看器将显示跨页最左侧的页面，跨页指向 <span class="codeph"> frameIdx</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-fc7c012c91d1419b8a5bb60d28e17327}

可选。

## 默认 {#section-bbc6ebad3af54fd79837515c270e6ddf}

`0`

## 示例 {#section-cbc6684eb22e4d0883edc4b3d5742336}

在查看器URL中指定时。

```
initialFrame=2
```
