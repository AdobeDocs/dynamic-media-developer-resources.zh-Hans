---
title: 弹出缩放视图
description: 在内联缩放模式下，主视图由静态图像组成。 此外，它还包括显示在静态图像的弹出视图中的缩放图像，以及显示在静态图像顶部的提示消息。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# 弹出缩放视图{#flyout-zoom-view}

在内联缩放模式下，主视图由静态图像组成。 此外，它还包括显示在静态图像的弹出视图中的缩放图像，以及显示在静态图像顶部的提示消息。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主查看器区域的&#x200B;**CSS属性**

主视图的外观由以下CSS类选择器控制：

```
.s7mixedmediaviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 主视图的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主视图透明：

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

使用以下CSS类选择器来控制提示消息的外观：

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

可以通过CSS配置字体样式、大小外观和垂直偏移。 但是，水平对齐是由查看器逻辑管理的。 不支持使用`left`或`right`属性通过CSS覆盖它。

提示消息的&#x200B;**CSS属性**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>消息背景填充颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框半径</span> </p> </td> 
   <td colname="col2"> <p> 邮件背景边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p> 从主视图底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>提示文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">不透明度</span> </p> </td> 
   <td colname="col2"> <p> 消息后台不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p> 在消息文本周围填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可对提示消息进行本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

示例 — 要设置具有白色Arial® 12-px字体、距主视图底部50像素偏移量、内边距和圆角边框的半透明提示消息：

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
