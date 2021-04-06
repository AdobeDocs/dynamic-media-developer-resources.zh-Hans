---
description: 用于交互式视频查看器的URL命令。
solution: Experience Manager
title: interactivedata
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，商业从业者
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 5%

---

# interactivedata{#interactivedata}

用于交互式视频查看器的URL命令。

`interactivedata= *`文件`*`

交互式数据将视频内容中的某些时间区域与产品数据相关联，产品数据稍后显示在视频旁边的交互式色板中。 它还关联在视频播放结束时显示的行动动员面板中。 它还为在行动动员面板中显示的交互式视频提供标题。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 文件</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT交互式数据内容的URL或路径。 WebVTT文件必须由图像服务提供。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
