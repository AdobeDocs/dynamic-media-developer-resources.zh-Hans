---
title: 收藏夹视图
description: 收藏夹视图由缩略图图像列组成。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# 收藏夹视图{#favorites-view}

收藏夹视图由缩略图图像列组成。

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

收藏夹视图容器的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesview
```

收藏夹视图的位置和高度由视图管理；在CSS中，只能定义宽度。

收藏夹视图的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 收藏夹视图的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>视图的宽度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置宽度为100像素且背景为半透明的收藏夹视图：

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

收藏夹缩略图之间的间距由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

收藏夹缩略图的&#x200B;**CSS属性**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p> 每个缩略图周围的垂直边距大小。 实际缩略图间距等于为<span class="codeph"> .s7缩略图单元格</span>设置的上边距和下边距之和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置十个像素间距：

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

单个缩略图的外观可通过以下CSS类选择器进行控制：

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

收藏夹缩略图的&#x200B;**CSS属性**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>缩略图的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>缩略图的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框</span> </p> </td> 
   <td colname="col2"> <p>缩略图的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态。 特别是，`state="selected"`对应于用户最近选择的缩略图。 属性`state="default"`对应于缩略图的其余部分。 并且，鼠标悬停时使用了属性`state="over"`。

示例 — 要设置像素为75 x 75、具有浅灰色默认边框和深灰色选定边框的缩略图：

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

缩略图标签的外观可通过以下CSS类选择器进行控制：

```
.s7ecatalogviewer .s7favoritesview .s7label
```

收藏夹标签的&#x200B;**CSS属性**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famy </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置具有14像素Helvetica®字体的标签：

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
