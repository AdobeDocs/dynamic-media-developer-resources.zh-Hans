---
description: 根据模式参数的值，查看器在最初在Scene7出版系统中创作地图的位置，在主视图上显示图像地图图标，或呈现与原始图像地图的形状匹配的精确区域。
seo-description: 根据模式参数的值，查看器在最初在Scene7出版系统中创作地图的位置，在主视图上显示图像地图图标，或呈现与原始图像地图的形状匹配的精确区域。
seo-title: 图像映射效果
solution: Experience Manager
title: 图像映射效果
topic: Dynamic Media
uuid: 8bafaec3-500c-4a1f-b511-bff125daab7f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---


# 图像映射效果{#image-map-effect}

根据模式参数的值，查看器在最初在Scene7出版系统中创作地图的位置，在主视图上显示图像地图图标，或呈现与原始图像地图的形状匹配的精确区域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

图像映射图标的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>过去用于设置图像映射图标样式的`s7mapoverlay` CSS类现已弃用；请改用`s7icon`。

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
   <td colname="col2"> <p>图像映射图标图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置位置（如果使用CSS Sprite）。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>图像映射图标宽度（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>图像映射图标高度（以像素为单位）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>图像映射图标支持`state`属性选择器，您可以使用该选择器将不同的外观应用于`default`和`active`的图标状态。

示例——设置一个28 x 28像素的图像映射图标，该图标针对两个不同的图标状态中的每一个显示不同的图像。

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogsearchviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

另请参阅[图像映射支持](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a)。

图像映射区域的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景  </span> </p> </td> 
   <td colname="col2"> <p> 图像映射区域填充颜色。 </p> <p>以#RRGGBB、RGB(R,G,B)或RGBA(R,G,B,A)格式指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> 图像映射区域填充颜色。 </p> <p>以#RRGGBB、RGB(R,G,B)或RGBA(R,G,B,A)格式指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 图像映射区域边框样式。 </p> <p>指定为<span class="codeph"> <span class="varname">宽度</span>实色<span class="varname"> </span> </span>，其中<span class="codeph"> <span class="varname">宽度</span> </span>以像素表示，<span class="codeph"> <span class="varname">颜色</span> </span>设置为#RRGGBB, RGB(R,G,B)或RGBA(R,G,B,A)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置具有`1`像素黑色边框的透明图像映射区域：

```
.s7ecatalogsearchviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

