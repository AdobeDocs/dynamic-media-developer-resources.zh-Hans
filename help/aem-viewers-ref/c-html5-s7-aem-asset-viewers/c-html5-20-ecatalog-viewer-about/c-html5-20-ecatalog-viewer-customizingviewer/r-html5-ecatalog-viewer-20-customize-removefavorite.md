---
title: “删除收藏夹”按钮
description: “删除收藏夹”按钮的位置由“收藏夹”菜单完全管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 9654ee6c-3b47-4a96-b6f0-87a0facf4523
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# “删除收藏夹”按钮{#remove-favorite-button}

“删除收藏夹”按钮的位置由“收藏夹”菜单完全管理。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

使用以下CSS类选择器可控制“删除收藏夹”按钮的外观：

```
.s7ecatalogviewer .s7removefavoritebutton
```

“删除收藏夹”按钮的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>另请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
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

>[!NOTE]
>
>此按钮同时支持`state`和`selected`属性选择器，它们可用于将不同的外观应用于不同的按钮状态。 特别是，`selected='true'`对应于用户通过单击或点按可添加新“收藏”图标的状态。 属性`selected='false'`对应于用户可以缩放、平移和交换页面的正常操作模式。

按钮工具提示可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例 — 设置一个28 x 28像素的“删除收藏夹”按钮，并在选中或未选中时，为四种不同的按钮状态中的每种状态显示不同的图像。

```
.s7ecatalogviewer .s7removefavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_up.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_down.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7removefavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
}
```
