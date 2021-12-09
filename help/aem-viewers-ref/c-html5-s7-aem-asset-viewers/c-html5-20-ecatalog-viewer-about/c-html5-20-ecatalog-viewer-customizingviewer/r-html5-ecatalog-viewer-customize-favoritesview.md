---
title: 收藏夹视图
description: “收藏夹”视图包含一列缩略图。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 2%

---

# 收藏夹视图{#favorites-view}

“收藏夹”视图包含一列缩略图。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

使用以下CSS类选择器控制“收藏夹”视图容器的外观：

```
.s7ecatalogviewer .s7favoritesview
```

收藏夹视图的位置和高度由视图管理；在CSS中，只能定义宽度。

**“收藏夹”视图的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p> “收藏夹”视图的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>视图的宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置宽度为100像素的半透明灰色背景的“收藏夹”视图，请执行以下操作：

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

通过以下CSS类选择器可控制收藏夹缩略图之间的间距：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**收藏夹缩略图的CSS属性**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每个缩略图周围垂直边距的大小。 实际缩略图间距等于为 <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置十个像素间距：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

通过以下CSS类选择器控制单个缩略图的外观：

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**收藏夹缩略图的CSS属性**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度 </span> </p> </td> 
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
>缩略图支持 `state` 属性选择器，用于将不同的外观应用到不同的缩略图状态。 特别是， `state="selected"` 对应于用户最近选择的缩略图。 属性 `state="default"` 对应于其余的缩略图。 还有，属性 `state="over"` 鼠标悬停时使用。

示例 — 要设置缩略图75 x 75像素，缩略图的默认边框为浅灰色，选定的边框为深灰色：

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

通过以下CSS类选择器控制缩略图标签的外观：

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**“收藏夹”标签的CSS属性**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小 </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置14像素Helvetica®字体的标签，请执行以下操作：

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
