---
title: 页面查看
description: 主视图由目录图像组成。 它可以滑动以转到其他页面或缩放。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d3368115-15e7-4d9d-a417-a3c82c9a8a64
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 2%

---

# 页面查看{#page-view}

主视图由目录图像组成。 它可以滑动以转到其他页面或缩放。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

主查看器区域的&#x200B;**CSS属性**

查看区域的外观由以下CSS类选择器控制：

```
.s7ecatalogviewer .s7pageview
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
   <td colname="col2"> <p> 主视图的背景颜色（十六进制格式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">游标</span> </p> </td> 
   <td colname="col2"> <p>显示在主视图上的光标。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主视图透明。

```
.s7ecatalogviewer .s7pageview { 
 background-color: transparent; 
}
```

在桌面系统上，组件支持可应用于`cursortype`类的`.s7pageview`属性选择器，并根据组件状态和用户操作控制游标类型。 支持以下`cursortype`值：

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">默认</span> </p> </td> 
   <td colname="col2"> <p>由于图像分辨率低、组件设置或两者同时存在而导致图像无法缩放时显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">放大</span> </p> </td> 
   <td colname="col2"> <p>在可以放大图像时显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">重置</span> </p> </td> 
   <td colname="col2"> <p>当图像处于最大缩放级别时显示，并且可以重置为初始状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">拖动</span> </p> </td> 
   <td colname="col2"> <p>当用户平移处于缩放状态的图像时显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">张幻灯片</span> </p> </td> 
   <td colname="col2"> <p>当用户通过执行水平轻扫或轻扫执行图像交换时显示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可通过以下CSS类选择器控制用于视觉上分隔目录跨页左页和右页的页面分隔符：

`.s7ecatalogviewer .s7pageview .s7pagedivider`

<table id="table_77EBC9A77BF14CF4974F8F43C709A207"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 页面分隔符的宽度。 设置为<span class="codeph"> 0 </span>像素，以完全隐藏分隔符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>要用作页面分隔符的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 具有40像素宽分页符和半透明图像。

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>当`frametransition`修饰符设置为`turn`或`auto`（在桌面系统上）时，通过`pageturnstyle`修饰符控制页面分隔符的外观，并忽略`.s7pagedivider` CSS类。

可以在主查看器区域上配置自定义鼠标游标的显示。 此功能通过应用于`.s7ecatalogviewer .s7pageview` CSS类的其他属性选择器进行控制：

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">默认</span> </p> </td> 
   <td colname="col2"> <p> 通常为箭头，对于不可缩放的图像显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">放大</span> </p> </td> 
   <td colname="col2"> <p> 显示何时可以放大图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">重置</span> </p> </td> 
   <td colname="col2"> <p>显示图像何时达到最大缩放并可重置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">拖动</span> </p> </td> 
   <td colname="col2"> <p>显示用户何时对放大图像执行拖动操作 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">张幻灯片</span> </p> </td> 
   <td colname="col2"> <p>显示用户何时使用幻灯片手势执行图像交换 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 每种类型的组件状态都有不同的鼠标游标。

```
.s7ecatalogviewer .s7pageview[cursortype="default"] { 
cursor:auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="zoomin"] { 
cursor:url(images/zoomin_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="reset"] { 
cursor:url(images/zoomout_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview [cursortype="slide"] { 
cursor:url(images/slide_cursor.cur), auto; 
} 
.s7ecatalogviewer .s7pageview[cursortype="drag"] { 
cursor:url(images/drag_cursor.cur), auto; 
}
```
