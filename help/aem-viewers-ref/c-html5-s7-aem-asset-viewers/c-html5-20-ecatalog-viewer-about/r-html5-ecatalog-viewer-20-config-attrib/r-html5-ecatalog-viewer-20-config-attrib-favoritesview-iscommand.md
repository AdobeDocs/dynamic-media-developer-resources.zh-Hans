---
description: 应用于所有缩略图的图像提供命令字符串。
solution: Experience Manager
title: FavoritesView.iscommand
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog
role: Developer,User
exl-id: 1b6198f4-367d-437a-b8b1-206519567af0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 7%

---

# FavoritesView.iscommand{#favoritesview-iscommand}

应用于所有缩略图的图像提供命令字符串。

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 如果在URL中指定，则所有出现的<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>都必须分别以<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>的形式进行HTTP编码。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

在查看器URL中指定时。

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时。

`iscommand=op_sharpen=1&op_colorize=0xff0000`
