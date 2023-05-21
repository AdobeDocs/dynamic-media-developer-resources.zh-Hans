---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c2bbcb99-eeef-4793-a132-d0bd1fefb534
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 5%

---

# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>指定元件預先載入行為。 </p> <p>當設定為 <span class="codeph"> -1</span> 初始化元件或變更資產時，所有縮圖會同時載入。 </p> <p> 當設定為 <span class="codeph"> 0</span> 僅載入可見的縮圖。 </p> <p>設定 <span class="codeph"><span class="varname"> preloadnbr</span></span> 定義可見區域周圍預先載入的隱藏列數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-4b7952997f9240e581d21bcdb173f9af}

可选.

## 默认 {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## 示例 {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
