---
title: 控件栏
description: 控制栏是一个矩形区域，其中包含并位于所有可用于视频查看器的用户界面控件后面，如播放/暂停按钮、音量控件等。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
TQID: 'https://experienceleague.adobe.com/IfJ-ukIT31IS8sE6EWSqTl7k4uav08CsDHvS4bSh-Bc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# 控件栏{#control-bar}

控制栏是一个矩形区域，其中包含并位于所有可用于视频查看器的用户界面控件后面，如播放/暂停按钮、音量控件等。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

控制栏始终采用所有可用的查看器宽度。 可以通过CSS更改其相对于视频查看器容器的颜色、高度和垂直位置。

以下CSS类选择器控制控件栏的外观：

```
.s7mixedmediaviewer .s7controlbar
```

## 控件栏的CSS属性 {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>控件栏的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>控件栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

设置一个具有30像素高的灰色控制栏的混合媒体查看器。

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
