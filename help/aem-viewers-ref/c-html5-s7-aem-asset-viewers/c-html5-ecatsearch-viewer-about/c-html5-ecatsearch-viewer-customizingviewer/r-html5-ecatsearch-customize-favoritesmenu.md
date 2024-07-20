---
title: 收藏夹菜单
description: “收藏夹”菜单下拉列表显示在控制栏中。 它由一个按钮和一个面板组成，当用户单击或点按按钮时，该面板会展开。 该面板包含单个收藏夹工具。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 129a8451-f634-44ad-adb1-f30d2621cb29
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# 收藏夹菜单{#favorites-menu}

“收藏夹”菜单下拉列表显示在控制栏中。 它由一个按钮和一个面板组成，当用户单击或点按按钮时，该面板会展开。 该面板包含单个收藏夹工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

查看器用户界面中“收藏夹”菜单的位置和大小由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7favoritesmenu
```

“收藏夹”菜单按钮的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上边距</span> </p> </td> 
   <td colname="col2"> <p> 从控件栏顶部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左边距</span> </p> </td> 
   <td colname="col2"> <p> 与左侧的下一个按钮或控制栏左侧的距离（如果该按钮是行中的第一个按钮）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按钮的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置收藏夹菜单，该菜单位于控件栏顶部的4个像素和最接近按钮左侧的10个像素的位置，大小为28 x 28像素。

```
.s7ecatalogsearchviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

收藏夹菜单按钮的外观可通过以下CSS类选择器来控制：

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton
```

收藏夹按钮的&#x200B;**CSS属性**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置收藏夹菜单按钮，该按钮为四种不同的按钮状态中的每种状态显示不同的图像。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

包含各个“收藏夹”图标的面板的外观可通过以下CSS类选择器进行控制：

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel
```

收藏夹菜单面板的&#x200B;**CSS属性**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>面板的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置具有透明颜色的面板。

```
.s7ecatalogsearchviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
