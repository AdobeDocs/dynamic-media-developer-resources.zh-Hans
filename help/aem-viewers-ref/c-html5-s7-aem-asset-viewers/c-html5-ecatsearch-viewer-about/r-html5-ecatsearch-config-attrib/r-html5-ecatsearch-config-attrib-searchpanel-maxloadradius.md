---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,User
exl-id: c2bbcb99-eeef-4793-a132-d0bd1fefb534
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定组件预加载行为。 </p> <p>当设置为<span class="codeph"> -1</span>时，在初始化组件或资产更改时，将同时加载所有缩略图。 </p> <p> 设置为<span class="codeph"> 0</span>时，只加载可见的缩略图。 </p> <p>设置<span class="codeph"><span class="varname"> preloadnbr</span></span>以定义预加载可见区域周围的不可见行数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-4b7952997f9240e581d21bcdb173f9af}

可选。

## 默认 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 示例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
