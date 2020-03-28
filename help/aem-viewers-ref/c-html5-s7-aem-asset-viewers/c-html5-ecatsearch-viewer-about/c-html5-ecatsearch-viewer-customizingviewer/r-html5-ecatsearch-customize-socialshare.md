---
description: 默认情况下，社交共享工具显示在左上角。 它由按钮和面板组成，当用户单击或点按按钮时该面板展开并包含各个共享工具。
seo-description: 默认情况下，社交共享工具显示在左上角。 它由按钮和面板组成，当用户单击或点按按钮时该面板展开并包含各个共享工具。
seo-title: 社交共享
solution: Experience Manager
title: 社交共享
topic: Dynamic media
uuid: 6d463eb1-c6bf-4f1c-90e4-b5ef1e5a1538
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 社交共享{#social-share}

默认情况下，社交共享工具显示在左上角。 它由按钮和面板组成，当用户单击或点按按钮时该面板展开并包含各个共享工具。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

社交共享工具在查看器用户界面中的位置和大小通过以下方式进行控制：

```
.s7ecatalogsearchviewer .s7socialshare
```

**社交共享工具的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> 与控制栏顶部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> 到左侧下一个按钮的距离；如果这是一行中的第一个按钮，则距控件栏左侧的距离。 </p> </td> 
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

示例——设置一个社交共享工具，该工具距查看器容器顶部有四个像素，距右侧有五个像素，大小为28 x 28像素。

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

社交共享工具按钮的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
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
   <td colname="col2"> <p> 在图稿Sprite中定位（如果使用CSS Sprite）。 </p> <p>另请参 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> 阅CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持属 `state` 性选择器，该选择器可用于将不同的外观应用于不同的按钮状态。

按钮工具提示可以本地化。 有关 [详细信息，请参阅用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

示例——设置一个社交共享工具按钮，该按钮为四个不同的按钮状态中的每个状态显示一个不同的图像。

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

包含各个社交共享图标的面板的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
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

示例——设置一个具有透明颜色的面板：

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

