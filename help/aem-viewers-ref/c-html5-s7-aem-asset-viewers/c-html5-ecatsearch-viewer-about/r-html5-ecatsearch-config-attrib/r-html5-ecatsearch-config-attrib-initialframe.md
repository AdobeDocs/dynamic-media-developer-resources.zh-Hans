---
description: InitialFrame
solution: Experience Manager
title: InitialFrame
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,Business Practitioner
exl-id: 15241738-a1b6-4723-b6fc-ebc8f7dedb03
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 9%

---

# InitialFrame{#initialframe}

[!DNL ` initialFrame= *`frame`*`]

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> frame</span></span> </p> </td> 
   <td colname="col2"> <p> 指定要在查看器加载时显示的零基跨页索引。 索引与横向模式下跨页的索引匹配。 如果将查看器旋转为纵向，则查看器将显示跨页中最左侧的页面，该跨页由<span class="codeph"> frameIdx</span>指向。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-fc7c012c91d1419b8a5bb60d28e17327}

可选。

## 默认 {#section-bbc6ebad3af54fd79837515c270e6ddf}

[!DNL `0`]

## 示例 {#section-cbc6684eb22e4d0883edc4b3d5742336}

在查看器URL中指定时。

```
[!DNL initialFrame=2
```
