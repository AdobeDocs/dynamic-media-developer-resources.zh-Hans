---
title: facebook共享
description: facebook共享工具包含一个添加到“社交共享”面板的按钮。 选择该按钮后，用户将被重定向到社交服务提供的一个共享对话框。 按钮的位置完全由社交共享工具管理。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 792d53de-5561-48bb-85d7-fbf3b6377673
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---

# facebook共享{#facebook-share}

facebook共享工具包含一个添加到“社交共享”面板的按钮。 选择该按钮后，用户将被重定向到社交服务提供的一个共享对话框。 按钮的位置完全由社交共享工具管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

facebook共享按钮的外观由以下CSS类选择器控制：

```
.s7ecatalogsearchviewer .s7facebookshare
```

**facebook共享工具的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite内。 </p> <p>另请参阅 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS脚本 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 属性选择器，可用于将不同的外观应用于不同的按钮状态。

可以通过设置从Social共享面板中删除按钮 `display:none` CSS属性的CSS类。

可对按钮工具提示进行本地化。 参见 [用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 了解更多信息。

示例 — 设置一个28 x 28像素的Facebook共享按钮，并为四种不同的按钮状态分别显示不同的图像：

```
.s7ecatalogsearchviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
