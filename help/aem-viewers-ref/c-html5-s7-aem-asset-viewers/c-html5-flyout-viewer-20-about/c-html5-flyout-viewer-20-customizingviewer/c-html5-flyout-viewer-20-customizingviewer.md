---
description: 自定义弹出查看器
keywords: 响应式
solution: Experience Manager
title: 自定义弹出查看器
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: Developer,Business Practitioner
exl-id: b7898044-5178-4cdf-ab52-9996a61a3a35
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '1270'
ht-degree: 0%

---

# 自定义弹出查看器{#customizing-flyout-viewer}

所有可视化自定义和大多数行为自定义都是通过创建自定义CSS来完成的。

建议的工作流程是为相应的查看器获取默认的CSS文件，将其复制到其他位置，对其进行自定义，然后在`style=`命令中指定自定义文件的位置。

默认CSS文件可在以下位置找到：

`<s7_viewers_root>/html5/FlyoutViewer.css`

自定义CSS文件必须包含与默认类声明相同的类声明。 如果忽略类声明，则查看器将无法正常运行，因为它不为用户界面元素提供内置的默认样式。

提供自定义CSS规则的替代方法是，直接在网页或某个链接的外部CSS规则中使用嵌入的样式。

创建自定义CSS时，请记住，查看器会将`.s7flyoutviewer`类分配给其容器DOM元素。 如果使用通过`style=`命令传递的外部CSS文件，请在CSS规则的子选择器中使用`.s7flyoutviewer`类作为父类。 如果您在网页上执行嵌入的样式，则此外，还应使用容器DOM元素的ID来限定此选择器，如下所示：

`#<containerId>.s7flyoutviewer`

## 构建响应式设计的CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

可以定位CSS中的不同设备和嵌入大小，以使内容显示方式不同，具体取决于用户的设备或特定网页布局。 这包括但不限于不同的网页布局、用户界面元素大小和图稿分辨率。

查看器支持两种创建响应式设计CSS的方法：CSS标记和标准CSS媒体查询。 您可以单独或结合使用这些方法。

**CSS标记**

为了帮助创建响应式设计的CSS，查看器支持CSS标记，这些CSS标记基于运行时查看器大小和当前设备上使用的输入类型，动态地分配给顶级查看器容器元素的特殊CSS类。

第一组CSS标记包括`.s7size_large`、`.s7size_medium`和`.s7size_small`类。 它们基于查看器容器的运行时区域应用。 即，如果查看器面积等于或大于公共桌面监视器`.s7size_large`的大小；如果区域的大小与普通平板电脑设备`.s7size_medium`的大小接近，则会分配该区域。 对于类似于手机屏幕`.s7size_small`的区域，将进行设置。 这些CSS标记的主要用途是为不同屏幕和查看器大小创建不同的用户界面布局。

第二组CSS标记包括`.s7mouseinput`和`.s7touchinput`。 `.s7touchinput` 如果当前设备具有触控输入功能，则设置；否则， `.s7mouseinput` 将使用。这些标记旨在为不同的输入类型创建具有不同屏幕大小的用户界面输入元素，因为通常，触摸输入需要较大的元素。 如果设备同时具有鼠标输入和触摸功能，则设置`.s7touchinput`，并且查看器呈现一个触摸友好的用户界面。

以下示例CSS可将带有鼠标输入的系统上的按钮放大大小设置为28 x 28像素，将触控设备上的按钮放大大小设置为56 x 56像素。 此外，如果查看器大小变得非常小，则会完全隐藏按钮：

```
.s7flyoutviewer.s7mouseinput .s7swatches .s7thumb {  
 width: 28px; 
 height: 28px; 
} 
.s7flyoutviewer.s7touchinput .s7swatches .s7thumb {  
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer.s7size_small .s7swatches {  
 visibility: hidden; 
}
```

要定位像素密度不同的设备，请使用CSS媒体查询。 以下媒体查询块将包含特定于高密度屏幕的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS标记是构建响应式设计CSS的最灵活方式，它不仅允许您定位设备屏幕大小，还允许定位实际的查看器大小，这对于响应式设计的网页布局可能非常有用。

**CSS媒体查询**

设备感知也可以使用纯CSS媒体查询来完成。 仅当给定媒体查询块在相应设备上运行时，它所包含的所有内容才会被应用。

应用到移动设备查看器时，请按以下顺序使用四个CSS媒体查询，这些查询在CSS中定义：

1. 仅包含适用于所有触屏设备的特定规则。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. 仅包含针对具有高分辨率屏幕的平板电脑的特定规则。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. 仅包含所有手机的特定规则。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 仅包含针对具有高分辨率屏幕的移动电话的特定规则。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

使用媒体查询方法，您应按如下方式组织具有设备感知的CSS:

* 首先，特定于桌面的部分定义所有特定于桌面或对所有屏幕通用的属性。
* 其次，这四个媒体查询按上面定义的顺序运行，并提供特定于相应设备类型的CSS规则。

无需在每个媒体查询中复制整个查看器CSS。 只有特定于给定设备的属性才会在媒体查询中重新定义。

## CSS Sprite {#section-0711ece44a4740168cfd7624c9010bd1}

许多查看器用户界面元素使用位图图稿设置样式，并具有多个不同的可视状态。 一个按钮通常至少具有3种不同状态的示例很好：“up”、“over”和“down”。 每个状态都需要分配其自己的位图图稿。

通过经典的样式设置方法，CSS将针对用户界面元素的每个状态对服务器上的单个图像文件单独进行引用。 以下是用于设置滚动按钮样式的CSS示例：

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-image:url(images/v2/ScrollLeftButton_up.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-image:url(images/v2/ScrollLeftButton_down.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-image:url(images/v2/ScrollLeftButton_disabled.png);  
}
```

此方法的缺点是，当元素首次交互时，最终用户体验到闪烁或延迟的用户界面响应。 此操作是因为尚未下载新元素状态的图像图稿。 此外，由于对服务器的HTTP调用数量增加，此方法可能会对性能产生轻微的负面影响。

CSS Sprite是一种不同的方法，其中所有元素状态的图像图稿都合并到一个PNG文件中，称为“sprite”。 此类“sprite”具有给定元素的所有可视状态，这些状态会逐个放置。 为用户界面元素设置样式时，CSS中所有不同状态都会引用具有相同Sprite图像的Sprite。 此外，每个状态都使用`background-position`属性来指定“sprite”图像的哪一部分。 您可以采用任何合适的方式构建“Sprite”图像。 查看器通常会垂直堆叠查看器。 下面是一个基于“sprite”的示例，用于为上面相同的滚动按钮设置样式：

```
.s7flyoutviewer .s7scrollleftbutton[state]  { 
    background-image: url(images/v2/ScrollLeftButton_light_sprite.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-position: -56px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-position: -0px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-position: -56px -448px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-position: -0px -448px;  
}
```

## 一般样式说明和建议 {#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自定义查看器用户界面时，不支持使用`!IMPORTANT`规则来设置查看器元素的样式。 特别是，不应使用`!IMPORTANT`规则覆盖查看器或查看器SDK提供的任何默认或运行时样式。 其原因可能会影响正确组件的行为。 您而是应该使用具有适当特性的CSS选择器来设置本参考指南中介绍的CSS属性。
* CSS中指向外部资产的所有路径都将根据CSS位置（而不是查看器HTML页面位置）进行解析。 将默认CSS复制到其他位置时，请注意此规则。 复制默认资产或更新自定义CSS中的路径。
* 位图图稿的首选格式为PNG。
* 使用`background-image`属性将位图图稿分配给用户界面元素。
* 用户界面元素的`width`和`height`属性定义其逻辑大小。 传递到`background-image`的位图的大小不会影响逻辑大小。
* 要使用Retina等高分辨率屏幕的高像素密度，请指定比图稿大两倍于逻辑用户界面元素大小的位图图稿。 然后，应用`-webkit-background-size:contain`属性，将背景向下缩放到逻辑用户界面元素大小。
* 要从用户界面中删除按钮，请将`display:none`添加到其CSS类中。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度，请使用格式`rgba(R,G,B,A)`。 否则，可以使用格式`#RRGGBB`。

## 常用用户界面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是适用于弹出查看器的用户界面元素引用文档：

* [弹出缩放视图](r-html5-flyout-viewer-20-customize-flyoutzoomview.md)
* [焦点突出显示](r-html5-flyout-viewer-20-customize-focushighlight.md)
* [主查看器区域](r-html5-flyout-viewer-20-customize-mainviewerarea.md)
* [調色板](r-html5-flyout-viewer-20-customize-swatches.md)
* [工具提示](r-html5-flyout-viewer-20-customize-tooltips.md)
