---
description: 查看器在主视图上显示热点图标，这些位置是在AEM Assets的Dynamic Media中最初创作的热点 — 点播。
seo-description: 查看器在主视图上显示热点图标，这些位置是在AEM Assets的Dynamic Media中最初创作的热点 — 点播。
seo-title: 热点和图像映射
solution: Experience Manager
title: 热点和图像映射
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 1%

---


# 热点和图像映射{#hotspots-and-image-maps}

查看器在主视图上显示热点图标，这些位置是在AEM Assets的Dynamic Media中最初创作的热点 — 点播。

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
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>热点图标图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>如果使用CSS Sprite，则在图稿Sprite中定位。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
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

示例 — 设置一个56 x 56像素的热点图标，该图标可针对两种不同的图标状态中的每一个显示不同的图像：

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
   <td colname="col1"> <p> <span class="codeph"> 背景  </span> </p> </td> 
   <td colname="col2"> <p>图像映射区域填充颜色。 </p> <p>以<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB(R，G，B)</span>或<span class="codeph"> RGBA(R，G，B，A)</span>格式指定此颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>图像映射区域填充颜色。 </p> <p>以<span class="codeph"> #RRGGBB </span>、<span class="codeph"> RGB(R，G，B)</span>或<span class="codeph"> RGBA(R，G，B，A)</span>格式指定此颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 图像映射区域边框样式。 应指定为" <span class="codeph">宽度</span> <span class="codeph">纯色</span>"，其中<span class="codeph">宽度</span>以像素表示，<span class="codeph">颜色</span>设置为<span class="codeph">#RRGGBB </span>,<span class="codeph"> RGB(R，G，B)</span>或<span class="codeph"> RGBA(R，G，B，A)</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置一个具有一个像素黑色边框的透明图像映射区域：

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

