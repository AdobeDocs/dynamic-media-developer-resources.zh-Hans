---
description: “收藏夹”菜单下拉列表显示在控件栏中。 它由按钮和一个面板组成，当用户单击或点按按钮时该面板将展开。 该面板包含各个“收藏夹”工具。
seo-description: “收藏夹”菜单下拉列表显示在控件栏中。 它由按钮和一个面板组成，当用户单击或点按按钮时该面板将展开。 该面板包含各个“收藏夹”工具。
seo-title: 收藏夹菜单
solution: Experience Manager
title: 收藏夹菜单
topic: Dynamic media
uuid: 816e614d-8253-49a8-b57e-0b57b44db535
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 收藏夹菜单{#favorites-menu}

“收藏夹”菜单下拉列表显示在控件栏中。 它由按钮和一个面板组成，当用户单击或点按按钮时该面板将展开。 该面板包含各个“收藏夹”工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

查看器用户界面中“收藏夹”菜单的位置和大小由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesmenu
```

**“收藏夹”菜单按钮的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> 与控制栏顶部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 到左侧下一个按钮的距离；如果这是一行中的第一个按钮，则距控件栏左侧的距离。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置一个“收藏夹”菜单，该菜单从控件栏顶部放置四个像素，从最近的按钮向左放置十个像素，大小为28 x 28像素。

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

“收藏夹”菜单按钮的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**“收藏夹”按钮的CSS属性**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中定位（如果使用CSS Sprite）。 </p> <p>另请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持属 `state` 性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关 [详细信息，请参阅用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例——设置一个“收藏夹”菜单按钮，该按钮为四个不同的按钮状态中的每一个状态显示不同的图像。

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

包含各个“收藏夹”图标的面板的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**“收藏夹”菜单面板的CSS属性**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>面板的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置一个面板，使其具有透明颜色。

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

