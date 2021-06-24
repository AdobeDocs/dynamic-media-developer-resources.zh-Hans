---
description: 交互式视频查看器的URL命令。
solution: Experience Manager
title: 导航
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,Business Practitioner
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 12%

---

# 导航{#navigation}

交互式视频查看器的URL命令。

` navigation= *`文件`*`

查看器支持通过托管的WebVTT文件进行视频章节导航。 不支持提示定位运算符。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 文件</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT导航内容的URL或路径。 图像服务应托管WebVTT文件。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```
