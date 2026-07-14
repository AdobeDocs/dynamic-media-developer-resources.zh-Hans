---
title: ThumbnailGridView.fmt
description: ThumbnailGridView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 916ee5d1-e398-4923-9107-96f649033298
TQID: 'https://experienceleague.adobe.com/Jp3-9jcSw3-AnFXY4TXdJrXdaKNQB-F5lPAYMcDl8uI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 67
ht-degree: 4%

---

# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

`[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>指定组件从图像服务器加载图像时使用的图像格式。 它可以是Image Server和客户端浏览器支持的任意值。 如果指定的格式以<span class="codeph"> -alpha</span>结尾，则组件会将图像渲染为透明内容。 对于所有其他图像格式，组件会将图像视为不透明。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

可选.

## 默认 {#section-502c098dbae1452180c7f575a1d9dc8b}

`jpeg`

## 示例 {#section-5cde7b856ba646c293cfd3d79e47c507}

`fmt-png-alpha`

