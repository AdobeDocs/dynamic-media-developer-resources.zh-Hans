---
description: Video360查看器的配置属性。
seo-description: Video360查看器的配置属性。
seo-title: EmbedShare.embedsizes
solution: Experience Manager
title: EmbedShare.embedsizes
uuid: d3eea508-fb1e-4147-b853-a16f51725dd7
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 9%

---


# EmbedShare.embedsizes{#embedshare-embedsizes}

Video360查看器的配置属性。

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`宽`*, *``*[,0|1][; *``*, *`高双高`*[,0|1]]`

在“嵌入共享模式”对话框中，为“大小”组合框指定嵌入大小列表。

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> 嵌入宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>嵌入高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> 指定是否应在组合框中预先选择此列表项。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-f42369774e2740dcb399626a0e4e930e}

可选。

## 默认 {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## 示例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```

