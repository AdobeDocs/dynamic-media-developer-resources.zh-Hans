---
title: 社交共享
description: 默认情况下，社交共享工具显示在左上角。 它包含一个按钮和一个面板，当用户单击或点按按钮时，该面板将展开并包含单个共享工具。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b65b8846-3287-47ae-bdb6-6cac768cece0
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# 社交共享{#social-share}

默认情况下，社交共享工具显示在左上角。 它包含一个按钮和一个面板，当用户单击或点按按钮时，该面板将展开并包含单个共享工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

社交共享工具在查看器用户界面中的位置和大小可通过以下方式进行控制：

```
.s7ecatalogviewer .s7socialshare
```

**社交共享工具的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 顶部 </span> </p> </td> 
   <td colname="col2"> <p> 与控制栏顶部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> 左侧的到下一个按钮的距离，或者如果是一行中的第一个按钮，则位于控制栏的左侧。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 社交共享工具的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>社交共享工具的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置一个社交共享工具，该工具的距离顶部四个像素，距离查看器容器右侧五个像素，其大小为28 x 28像素：

```
.s7ecatalogviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

社交共享工具按钮的外观通过以下CSS类选择器进行控制：

```
.s7ecatalogviewer .s7socialshare .s7socialbutton
```

**社交按钮的CSS属性**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置 </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>另请参阅 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 属性选择器，用于将不同的外观应用于不同的按钮状态。

按钮工具提示可进行本地化。 请参阅 [用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以了解更多信息。

示例 — 要设置一个社交共享工具按钮，该按钮会针对四个不同按钮状态中的每个状态显示一个不同的图像：

```
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

通过以下CSS类选择器控制包含各个社交共享图标的面板的外观：

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel
```

**社交共享面板的CSS属性**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>面板的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将面板设置为具有透明颜色：

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
