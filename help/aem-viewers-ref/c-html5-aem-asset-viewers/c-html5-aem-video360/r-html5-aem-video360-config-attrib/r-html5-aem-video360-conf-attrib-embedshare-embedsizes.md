---
title: EmbedShare.embedsizes
description: Video360 Viewer的設定屬性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 3a6c23dd-5e2c-4149-aa24-37d445128125
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Video360 Viewer的設定屬性。

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`寬度`*, *`高度`*[,0|1][; *`寬度`*, *`高度`*[,0|1]]`

指定內嵌共用模式對話方塊中大小下拉式方塊的內嵌大小清單。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> 內嵌寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>內嵌高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定是否一開始應在下拉式方塊中預先選取此清單專案。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
