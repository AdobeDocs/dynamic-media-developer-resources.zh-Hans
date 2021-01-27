---
description: 查看器在主视图上显示“收藏夹”图标，位于用户最初添加该图标的位置。
seo-description: 查看器在主视图上显示“收藏夹”图标，位于用户最初添加该图标的位置。
seo-title: 收藏夹效果
solution: Experience Manager
title: 收藏夹效果
topic: Dynamic Media
uuid: 5fbfe299-1fae-427f-8ade-e12cd168b8a7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# 收藏夹效果{#favorites-effect}

查看器在主视图上显示“收藏夹”图标，位于用户最初添加该图标的位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

“收藏夹”图标的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**“收藏夹”图标的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为图标显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置位置（如果使用CSS Sprite）。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>图标的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>图标的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置36 x 36像素“收藏夹”图标。

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

在桌面系统上，该组件支持`cursortype`属性选择器，您可以将该选择器应用于`.s7favoriteseffect`类，并根据所选用户操作控制游标的类型。 支持以下`cursortype`值：

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>显示的用户正在添加新的“收藏夹”图标。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>显示的用户正在删除现有的“收藏夹”图标。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_视图  </span> </p> </td> 
   <td colname="col2"> <p>当收藏夹编辑不活动时，以正常操作模式显示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——每种类型的组件状态有不同的鼠标光标。

```
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```

