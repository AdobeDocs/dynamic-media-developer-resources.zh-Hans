---
title: 交互数据
description: 交互式视频查看器的URL命令。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
TQID: 'https://experienceleague.adobe.com/xIjjnZZX0Y7wce2TJwN2R228elxxysj0qXB2WELq9xc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 4%

---

# 交互数据{#interactivedata}

交互式视频查看器的URL命令。

`interactivedata= *`文件`*`

交互式数据将视频内容中的特定时间区域与产品数据关联，产品数据稍后显示在视频旁边的交互式样本中。 它还与视频播放结束时显示的call-to-action面板相关联。 它还为call-to-action面板中显示的交互式视频提供标题。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">文件</span> </span> </p> </td> 
   <td colname="col2"> <p> 指定WebVTT交互式数据内容的URL或路径。 WebVTT文件必须由图像服务提供服务。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选.

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

无。

## 示例： {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
