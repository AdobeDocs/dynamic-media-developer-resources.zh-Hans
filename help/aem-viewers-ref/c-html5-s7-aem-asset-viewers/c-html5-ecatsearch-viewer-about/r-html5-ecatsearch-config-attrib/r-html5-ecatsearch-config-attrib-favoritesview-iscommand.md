---
description: 应用于所有缩略图的图像服务命令字符串。
solution: Experience Manager
title: 收藏夹视图命令
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 114cc5b7-32b9-4d16-ab93-a66f3ec666e0
TQID: 'https://experienceleague.adobe.com/FZZjN7PhDctqlyEfwrp-25xrCJ5tYeklalzZtMyeIns'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 6%

---

# 收藏夹视图命令{#favoritesview-iscommand}

应用于所有缩略图的图像服务命令字符串。

[!DNL `[FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> 如果在URL中指定，则<span class="codeph"> &amp;</span>和<span class="codeph"> =</span>的所有匹配项必须通过HTTP编码分别表示为<span class="codeph"> %26</span>和<span class="codeph"> %3D</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

在查看器URL中指定时。

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

在配置数据中指定时。

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
