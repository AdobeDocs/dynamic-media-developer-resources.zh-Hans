---
title: 缩放视图图标效果
description: 缩放指示器覆盖在缩放视图区域上。 当图像处于重置状态时显示它，并且它还取决于iconeffect参数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f2db0259-f1cf-41bc-86fd-97a40d01db16
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# 缩放视图图标效果{#zoom-view-icon-effect}

缩放指示器覆盖在缩放视图区域上。 当图像处于重置状态时显示它，并且它还取决于iconeffect参数。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主查看器区域的&#x200B;**CSS属性**

查看区域的外观由以下CSS类选择器控制：

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 缩放指示器图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>缩放指示器宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>缩放指示器高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>图标效果支持`media-type`属性选择器，您可以使用它在不同设备上应用不同的图标效果。 特别是，`media-type='standard'`对应于通常使用鼠标输入的桌面系统，`media-type='multitouch'`对应于具有触摸输入的设备。

示例 — 为桌面系统和触摸设备使用不同的艺术作品设置100 x 100像素缩放指示器。

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
