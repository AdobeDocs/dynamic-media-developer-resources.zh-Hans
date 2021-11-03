---
title: videoServerUrl
description: 智能裁剪视频查看器的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 945c32e0-a67b-4c27-b661-26510615d757
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# videoServerUrl{#videoserverurl}

智能裁剪视频查看器的URL命令。

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 视频服务器根路径。 如果未指定域，则会应用提供页面的域。 标准URI路径解析适用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。标准SaaS使用不需要。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
