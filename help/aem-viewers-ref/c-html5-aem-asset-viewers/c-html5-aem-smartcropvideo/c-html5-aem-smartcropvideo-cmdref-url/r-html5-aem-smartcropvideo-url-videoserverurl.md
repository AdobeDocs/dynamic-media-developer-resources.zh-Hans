---
title: videoServerUrl
description: 智慧型裁切視訊檢視器的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9bd37d2c-c7ec-4f58-8328-45c0a156f330
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 5%

---

# videoServerUrl{#videoserverurl}

智慧型裁切視訊檢視器的URL命令。

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 視訊伺服器根路徑。 若未指定網域，則改為套用伺服頁面的網域。 適用標準URI路徑解析。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选. 標準SaaS使用不需要。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
