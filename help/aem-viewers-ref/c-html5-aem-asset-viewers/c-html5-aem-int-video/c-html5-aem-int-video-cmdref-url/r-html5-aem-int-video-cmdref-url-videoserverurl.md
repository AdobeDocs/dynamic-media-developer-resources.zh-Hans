---
title: videoServerUrl
description: Video Viewer的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2bcbe117-14a3-42c8-bdd3-790b32bb757c
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 6%

---

# videoServerUrl{#videoserverurl}

Video Viewer的URL命令。

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

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna
```
