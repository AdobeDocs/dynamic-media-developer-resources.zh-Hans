---
description: 查看器在最初在AEM资产的Dynamic Media —— 点播中创作热点的地方，在主视图上显示热点图标。
seo-description: 查看器在最初在AEM资产的Dynamic Media —— 点播中创作热点的地方，在主视图上显示热点图标。
seo-title: 热点和图像映射
solution: Experience Manager
title: 热点和图像映射
topic: Dynamic media
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 热点和图像映射{#hotspots-and-image-maps}

查看器在最初在AEM资产的Dynamic Media —— 点播中创作热点的地方，在主视图上显示热点图标。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

热点图标的外观由以下CSS类选择器控制：

```
.s7carouselviewer .s7imagemapeffect .s7icon
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
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p>热点图标图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p>如果使用CSS Sprite，则在图稿Sprite中定位。 </p> <p>请参 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
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

示例——设置56 x 56像素热点图标，该图标为两个不同的图标状态中的每一个状态显示不同的图像：

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

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**图像映射区域的CSS属性**

图像映射区域的外观由以下CSS类选择器控制：

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 </span> </p> </td> 
   <td colname="col2"> <p>图像映射区域填充颜色。 </p> <p>以 <span class="codeph"> #RRGGBB </span>、 <span class="codeph"> RGB(R,G,B)或 </span>RGBA(R,G,B,A)格式指定此颜色 <span class="codeph"></span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>图像映射区域填充颜色。 </p> <p>以 <span class="codeph"> #RRGGBB </span>、 <span class="codeph"> RGB(R,G,B)或 </span>RGBA(R,G,B,A)格式指定此颜色 <span class="codeph"></span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 图像映射区域边框样式。 应指定为宽度实色 <span class="codeph"></span> "，其中以像素表示，宽度表示为 <span class="codeph"> "R,G, </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span>B,R,G,B,A"，以像素表示，宽度表示为RGB(R,G,B,A)，或RGBA(R,G,B,A); </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置一个带有一个像素黑色边框的透明图像映射区域：

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

