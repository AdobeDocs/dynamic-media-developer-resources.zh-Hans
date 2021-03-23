---
description: 主视图由目录图像组成。 可以轻扫以转到其他页面或缩放。
seo-description: 主视图由目录图像组成。 可以轻扫以转到其他页面或缩放。
seo-title: 页面查看
solution: Experience Manager
title: 页面查看
uuid: 5e247f56-f0da-487b-8e03-587b9d36aa39
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 4%

---


# 页面查看{#page-view}

主视图由目录图像组成。 可以轻扫以转到其他页面或缩放。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

使用以下CSS类选择器控制查看区域的外观：

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> 主视图的背景颜色（十六进制格式）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 光标  </span> </p> </td> 
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

在桌面系统上，组件支持`cursortype`属性选择器，该选择器可应用于`.s7pageview`类，并基于组件状态和用户操作控制游标的类型。 支持以下`cursortype`值：

<table id="table_45B83F6CCDE84C36B0E087CA9144BFE6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>值 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 默认 </span> </p> </td> 
   <td colname="col2"> <p>当图像因图像分辨率小、组件设置或两者兼有而无法缩放时显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 卓敏  </span> </p> </td> 
   <td colname="col2"> <p>当图像可放大时显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重置 </span> </p> </td> 
   <td colname="col2"> <p>当图像处于最大缩放级别时显示，并可重置为初始状态。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖动 </span> </p> </td> 
   <td colname="col2"> <p>当用户平移处于缩放状态的图像时显示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻灯片  </span> </p> </td> 
   <td colname="col2"> <p>当用户通过水平轻扫或轻扫执行图像交换时显示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

通过以下CSS类选择器控制以可视方式分隔目录跨页的左和右页的页面分隔条：

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 页面分隔条的宽度。 设置为<span class="codeph"> 0 </span> px可完全隐藏分隔线。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>要用作页面分隔条的图像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使用半透明图像具有40像素宽的页面分隔条。

```
.s7ecatalogviewer .s7pageview .s7pagedivider { 
 width:40px; 
 background-image:url(images/sdk/divider.png); 
}
```

>[!NOTE]
>
>当`frametransition`修饰符设置为`turn`或`auto`（在桌面系统上）时，使用`pageturnstyle`修饰符控制页面分隔符的外观，并忽略`.s7pagedivider` CSS类。

可以在主查看器区域上配置自定义鼠标光标的显示。 通过应用于`.s7ecatalogviewer .s7pageview` CSS类的其他属性选择器来控制：

<table id="table_908164DECF9347A19A9696A23BBDB1A2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 默认 </span> </p> </td> 
   <td colname="col2"> <p> 通常，对于不可缩放的图像显示箭头。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 卓敏  </span> </p> </td> 
   <td colname="col2"> <p> 显示何时可以放大图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 重置 </span> </p> </td> 
   <td colname="col2"> <p>显示图像何时处于最大缩放并可重置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 拖动 </span> </p> </td> 
   <td colname="col2"> <p>显示用户对图像中的缩放执行拖动操作时间 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幻灯片  </span> </p> </td> 
   <td colname="col2"> <p>显示用户何时使用幻灯片手势执行图像交换 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 对于每种类型的组件状态有不同的鼠标光标。

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

