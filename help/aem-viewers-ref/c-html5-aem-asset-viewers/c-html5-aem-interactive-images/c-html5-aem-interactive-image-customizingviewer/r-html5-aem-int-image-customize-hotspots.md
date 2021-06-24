---
description: 在热点最初是在AEM AssetsDynamic Media中创作的地方，查看器会在主视图上显示热点图标 — 按需。
solution: Experience Manager
title: 热点
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: Developer,Business Practitioner
exl-id: ec1d9a91-e189-470a-abe2-4f33686905e7
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# 热点{#hotspots}

在热点最初是在AEM AssetsDynamic Media中创作的地方，查看器会在主视图上显示热点图标 — 按需。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

通过以下CSS类选择器控制热点图标的外观：

```
.s7interactiveimage .s7imagemapeffect .s7icon
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>热点图标图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>在图稿快照集内放置（如果使用CSS快照）。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>热点图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>热点图标高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个56 x 56像素的热点图标，该图标针对两种不同的图标状态中的每一个状态显示不同的图像：

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```
