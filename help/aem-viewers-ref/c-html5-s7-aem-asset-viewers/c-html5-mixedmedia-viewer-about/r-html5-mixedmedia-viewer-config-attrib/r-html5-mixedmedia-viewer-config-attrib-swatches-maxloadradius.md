---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 06f493d7-18c9-4bb1-add6-a0dfd1a689bd
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 7%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>指定组件预加载行为。 当设置为 <span class="codeph"> -1</span> 初始化组件或更改资产时，会同时加载所有色板。 </p> <p>当设置为 <span class="codeph"> 0</span> 只加载可见的色板。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> 定义预加载可见区域周围的多少行/列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-65be9301796240e38f31818229da7acc}

可选。

## 默认 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 示例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
