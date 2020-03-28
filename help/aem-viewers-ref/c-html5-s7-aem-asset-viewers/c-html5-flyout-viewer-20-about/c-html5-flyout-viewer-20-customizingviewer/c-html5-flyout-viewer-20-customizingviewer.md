---
description: 'null'
keywords: responsive
seo-description: 'null'
seo-title: 自定义弹出查看器
solution: Experience Manager
title: 自定义弹出查看器
topic: Dynamic media
uuid: 10b5caa4-5298-43fa-af86-4f0b77be967b
translation-type: tm+mt
source-git-commit: 8d7fdab78c5d23d0e541effa9b9c470921bd144b

---


# 自定义弹出查看器{#customizing-flyout-viewer}

所有可视自定义和大多数行为自定义都是通过创建自定义CSS完成的。

建议的工作流程是为相应的查看器使用默认的CSS文件，将其复制到其他位置，对其进行自定义，并在命令中指定自定义文件的位 `style=` 置。

默认CSS文件位于以下位置：

`<s7_viewers_root>/html5/FlyoutViewer.css`

自定义CSS文件必须包含与默认类声明相同的类声明。 如果忽略类声明，则查看器无法正常工作，因为它不为用户界面元素提供内置的默认样式。

提供自定义CSS规则的替代方法是直接在网页或链接的外部CSS规则之一中使用嵌入样式。

创建自定义CSS时，请记住查看器将 `.s7flyoutviewer` 类分配给其容器DOM元素。 如果使用与命令一起传递的外部CSS `style=` 文件，请在 `.s7flyoutviewer` CSS规则的子代选择器中使用类作为父类。 如果要在网页上执行嵌入样式，则还可以按如下方式将此选择器限定为容器DOM元素的ID:

`#<containerId>.s7flyoutviewer`

## 构建响应式设计的CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

可以在CSS中目标不同的设备和嵌入大小，使内容显示方式不同，具体取决于用户的设备或特定网页布局。 这包括但不限于不同的网页布局、用户界面元素大小和图稿分辨率。

查看器支持两种创建响应式设计的CSS的方法：CSS标记和标准CSS媒体查询。 您可以单独或一起使用这些方法。

**CSS标记**

为了帮助创建响应式设计的CSS，查看器支持CSS标记，这些特殊的CSS类基于运行时查看器大小和当前设备上使用的输入类型动态分配给顶级查看器容器元素。

第一组CSS标记包括 `.s7size_large`、 `.s7size_medium`和 `.s7size_small` 类。 它们根据查看器容器的运行时区域应用。 即，如果查看器面积等于或大于公共桌面显示器的尺寸，则使用 `.s7size_large` 该查看器；如果区域的大小与公用平板电脑设备相近，则会指 `.s7size_medium` 定该区域。 对于类似于手机屏幕的区 `.s7size_small` 域进行设置。 这些CSS标记的主要用途是为不同屏幕和查看器大小创建不同的用户界面布局。

第二组CSS标记包括 `.s7mouseinput` 和 `.s7touchinput`。 `.s7touchinput` is set if current device has touch input capabilities;否则， `.s7mouseinput` 将使用。 这些标记旨在为不同的输入类型创建具有不同屏幕尺寸的用户界面输入元素，因为通常触摸输入需要较大的元素。 如果设备同时具有鼠标输入和触摸功能，则设 `.s7touchinput` 置该设备，并且查看器呈现适合触控的用户界面。

以下范例CSS将鼠标输入系统上的按钮大小设置为28 x 28像素，将触控设备上的按钮大小设置为56 x 56像素。 此外，如果查看器大小变得很小，它会完全隐藏按钮：

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

要目标像素密度不同的设备，请使用CSS媒体查询。 以下媒体查询块将包含特定于高密度屏幕的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS标记是构建响应式设计的CSS的最灵活方法，它不仅允许您目标设备屏幕大小，还允许您调整实际的查看器大小，这对于响应式设计的网页布局可能非常有用。

**CSS媒体查询**

设备感测也可以使用纯CSS媒体查询来完成。 仅当在相应设备上运行时，包含在给定媒体查询块内的所有内容才被应用。

应用到移动查看器时，请使用四个CSS媒体查询，在CSS中按以下顺序定义：

1. 仅包含所有触控设备的特定规则。

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

使用媒体查询方法，您应按照如下方式使用设备感知组织CSS:

* 首先，特定于桌面的部分定义所有特定于桌面或所有屏幕通用的所有属性。
* 其次，四个媒体查询按上面定义的顺序排列，并提供特定于相应设备类型的CSS规则。

无需在每个媒体重复中查询整个查看器CSS。 只有特定于给定设备的属性在媒体查询中重新定义。

## CSS Sprite {#section-0711ece44a4740168cfd7624c9010bd1}

许多查看器用户界面元素使用位图图稿设置样式，并具有多个不同的可视状态。 一个不错的示例是通常至少具有3种不同状态的按钮：“up”、“over”和“down”。 每个状态都需要分配自己的位图图稿。

使用经典的样式设计方法，CSS将针对用户界面元素的每个状态单独引用服务器上的单个图像文件。 以下是样式滚动按钮的示例CSS:

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

这种方法的缺点是当元素首次与之交互时，最终用户体验到闪烁或延迟的用户界面响应。 执行此操作是因为尚未下载新元素状态的图像图稿。 此外，由于对服务器的HTTP调用数量增加，此方法可能对性能产生轻微的负面影响。

CSS Sprite是一种不同的方法，它将所有元素状态的图像图稿组合到称为“Sprite”的单个PNG文件中。 此类“Sprite”具有给定元素的所有可视状态，这些元素一个接一个地定位。 当使用Sprite设置用户界面元素的样式时，CSS中所有不同状态都会引用相同的Sprite图像。 此外，该 `background-position` 属性用于每个状态，以指定使用“Sprite”图像的哪一部分。 您可以以任何合适的方式构建“Sprite”图像。 查看器通常将其垂直堆叠。 下面是一个基于“Sprite”的示例，用于从上面设置相同滚动按钮的样式：

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

* 使用CSS自定义查看器用户界面时，不支持 `!IMPORTANT` 对查看器元素进行样式设置。 特别是， `!IMPORTANT` 不应使用规则覆盖查看器或查看器SDK提供的任何默认或运行时样式。 其原因在于，它可能会影响正确组件的行为。 相反，您应该使用具有适当特异性的CSS选择器来设置本参考指南中介绍的CSS属性。
* CSS中指向外部资源的所有路径都会根据CSS位置而不是查看器HTML页面位置解析。 将默认CSS复制到其他位置时，请注意此规则。 复制默认资源或更新自定义CSS中的路径。
* 位图图稿的首选格式是PNG。
* 位图图稿使用属性分配给用户界面 `background-image` 元素。
* 用户界面 `width` 元素 `height` 的属性和属性定义其逻辑大小。 传递给的位图的大小不 `background-image` 影响逻辑大小。
* 要使用Retina等高分辨率屏幕的高像素密度，请指定位图图稿的两倍于逻辑用户界面元素大小。 然后，应用该 `-webkit-background-size:contain` 属性，将背景缩小到逻辑用户界面元素大小。
* 要从用户界面中删除按钮，请将其 `display:none` 添加到其CSS类。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度，请使用格式 `rgba(R,G,B,A)`。 否则，您可以使用格式 `#RRGGBB`。

## 通用用户界面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是适用于弹出查看器的用户界面元素引用文档：

* [弹出缩放视图](r-html5-flyout-viewer-20-customize-flyoutzoomview.md)
* [焦点突出显示](r-html5-flyout-viewer-20-customize-focushighlight.md)
* [主查看器区域](r-html5-flyout-viewer-20-customize-mainviewerarea.md)
* [調色板](r-html5-flyout-viewer-20-customize-swatches.md)
* [工具提示](r-html5-flyout-viewer-20-customize-tooltips.md)
