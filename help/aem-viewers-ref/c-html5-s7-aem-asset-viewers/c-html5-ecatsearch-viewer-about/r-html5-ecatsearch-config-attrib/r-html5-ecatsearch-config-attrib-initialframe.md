---
description: 初始帧
solution: Experience Manager
title: 初始帧
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 15241738-a1b6-4723-b6fc-ebc8f7dedb03
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# 初始帧{#initialframe}

[!DNL ` initialFrame= *`帧`*`]

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">帧</span></span> </p> </td> 
   <td colname="col2"> <p> 指定在查看器加载时显示的从零开始的扩展索引。 索引与横向模式下的跨页的索引匹配。 如果将查看器旋转为纵向，查看器将显示跨页最左边的<span class="codeph"> frameIdx</span>指向的页面。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-fc7c012c91d1419b8a5bb60d28e17327}

可选.

## 默认 {#section-bbc6ebad3af54fd79837515c270e6ddf}

[!DNL `0`]

## 示例 {#section-cbc6684eb22e4d0883edc4b3d5742336}

在查看器URL中指定时。

```
[!DNL initialFrame=2
```
