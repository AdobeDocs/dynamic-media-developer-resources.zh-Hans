---
description: 初始框架
solution: Experience Manager
title: 初始框架
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 15241738-a1b6-4723-b6fc-ebc8f7dedb03
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 8%

---

# 初始框架{#initialframe}

[!DNL ` initialFrame= *`frame`*`]

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> frame</span></span> </p> </td> 
   <td colname="col2"> <p> 指定要在檢視器載入時顯示的從零開始的展開索引。 索引符合橫向模式下的跨頁索引。 如果檢視器旋轉為縱向，檢視器會顯示跨頁所指向的最左側頁面 <span class="codeph"> frameIdx</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-fc7c012c91d1419b8a5bb60d28e17327}

可选.

## 默认 {#section-bbc6ebad3af54fd79837515c270e6ddf}

[!DNL `0`]

## 示例 {#section-cbc6684eb22e4d0883edc4b3d5742336}

在檢視器URL中指定時。

```
[!DNL initialFrame=2
```
