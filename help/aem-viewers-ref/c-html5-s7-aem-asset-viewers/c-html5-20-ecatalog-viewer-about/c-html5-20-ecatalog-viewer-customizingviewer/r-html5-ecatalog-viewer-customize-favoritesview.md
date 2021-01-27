---
description: 收藏夹视图由一列缩略图图像组成。
seo-description: 收藏夹视图由一列缩略图图像组成。
seo-title: 收藏夹视图
solution: Experience Manager
title: 收藏夹视图
topic: Dynamic Media
uuid: 6b954bec-0678-4970-b83a-c2d8fea06a25
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 2%

---


# 收藏夹视图{#favorites-view}

收藏夹视图由一列缩略图图像组成。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

“收藏夹”视图容器的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesview
```

收藏夹视图的位置和高度由视图管理；在CSS中，只能定义宽度。

**收藏夹视图的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> “收藏夹”视图的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>视图宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置宽度为100像素、半透明灰色背景的“收藏夹”视图。

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

“收藏夹”缩览图之间的间距由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**收藏夹缩略图的CSS属性**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每个缩略图周围垂直边距的大小。 实际缩略图间距等于为<span class="codeph"> .s7thumbcell </span>设置的上边距和下边距的和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置10像素间距。

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

单个缩略图的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**收藏夹缩略图的CSS属性**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>缩略图的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>缩略图的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>缩略图的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态。 特别是，`state="selected"`对应于用户最近选择的缩略图。 `state="default"` 与缩略图的其余部分相对应。`state="over"`用于鼠标悬停。

示例——要设置75 x 75像素的缩略图，请使用浅灰色默认边框和深灰色选定边框。

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

缩略图标签的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**收藏夹标签的CSS属性**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famiy  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置14像素Helvetica字体的标签。

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

