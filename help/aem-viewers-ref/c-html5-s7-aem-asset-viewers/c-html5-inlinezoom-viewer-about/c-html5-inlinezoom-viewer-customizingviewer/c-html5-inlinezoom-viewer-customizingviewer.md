---
title: 自定义内联缩放查看器
description: 自定义内联缩放查看器
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 8818bee3-dcdb-4a36-bddb-14dd10d0ea52
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 0%

---

# 自定义内联缩放查看器{#customizing-inline-zoom-viewer}

所有可视化自定义和大多数行为自定义都是通过创建自定义CSS来完成的。

建议的工作流是为相应的查看器获取默认的CSS文件，将其复制到其他位置，自定义它，并在 `style=` 命令。

默认CSS文件可在以下位置找到：

`<s7_viewers_root>/html5/InlineZoomViewer.css`

自定义CSS文件必须包含与默认类声明相同的类声明。 如果忽略类声明，则查看器将无法正常运行，因为它不为用户界面元素提供内置的默认样式。

此外，由于内联缩放功能需要从默认查看器CSS中保留以下CSS声明，这一点也很重要：

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 width: 100%; 
 height: 100%; 
 left: 0; 
 top: 0; 
 border: none; 
 z-index:999; 
}
```

提供自定义CSS规则的另一种方法是，直接在网页或某个链接的外部CSS规则中使用嵌入的样式。

创建自定义CSS时，请记住查看器会分配 `.s7flyoutviewer` 类添加到其容器DOM元素。 如果您使用的是通过 `style=` 命令，使用 `.s7flyoutviewer` 类作为CSS规则的子选择器中的父类。 如果您在网页上执行嵌入样式，还应使用容器DOM元素的ID来限定此选择器，如下所示：

`#<containerId>.s7flyoutviewer`

## 构建响应式设计的CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

可以定位CSS中的不同设备和嵌入大小，以使内容显示方式不同，具体取决于用户的设备或特定网页布局。 此功能包括但不限于不同的网页布局、用户界面元素大小和图稿分辨率。

查看器支持两种创建响应式设计CSS的方法：CSS标记和标准CSS媒体查询。 您可以单独或结合使用这些方法。

**CSS标记**

为了帮助创建响应式设计的CSS，查看器支持CSS标记，这些CSS标记是特殊的CSS类动态分配给顶级查看器容器元素。 这些分配基于运行时查看器大小以及当前设备上使用的输入类型。

第一组CSS标记包括 `.s7size_large`, `.s7size_medium`和 `.s7size_small` 类。 它们基于查看器容器的运行时区域应用。 即，如果查看器区域等于或大于公共桌面显示器的大小 `.s7size_large` ，则如果区域的大小接近普通平板电脑设备 `.s7size_medium` 分配。 对于类似于手机屏幕的区域， `.s7size_small` 设置。 这些CSS标记的主要用途是为不同屏幕和查看器大小创建不同的用户界面布局。

第二组CSS标记包括 `.s7mouseinput` 和 `.s7touchinput`. 标记 `.s7touchinput` 如果当前设备具有触控输入功能，则设置；否则， `.s7mouseinput` 中，将使用。 这些标记旨在为不同的输入类型创建具有不同屏幕大小的用户界面输入元素，因为通常，触摸输入需要较大的元素。 如果设备同时具有鼠标输入和触摸功能， `.s7touchinput` 设置，且查看器会呈现触屏友好用户界面。

以下示例CSS可将带有鼠标输入的系统上的按钮放大大小设置为28 x 28像素，将触控设备上的按钮放大大小设置为56 x 56像素。 此外，如果查看器大小变小，则会完全隐藏按钮：

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

使用CSS标记是构建响应式设计CSS的最灵活方法。 它不仅可以定位设备屏幕大小，还可以定位实际查看器大小，这对于响应式设计的网页布局可能非常有用。

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

## CSS Sprite {#section-b0af39db1af74561aea9fddcc8cdc2c7}

许多查看器用户界面元素使用位图图稿设置样式，并具有多个不同的可视状态。 一个按钮通常至少具有三种不同状态，这就是一个很好的示例：“up”、“over”和“down”。 每个状态都需要分配其自己的位图图稿。

通过经典的样式设置方法，CSS将针对用户界面元素的每个状态对服务器上的单个图像文件单独进行引用。 以下是用于为滚动按钮设置样式的示例CSS:

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

CSS Sprite是一种不同的方法，其中所有元素状态的图像图稿都合并到一个PNG文件中，称为“sprite”。 此类“sprite”具有给定元素的所有可视状态，这些状态会逐个放置。 为用户界面元素设置sprite样式时，CSS中所有不同状态都会引用相同的sprite图像。 此外， `background-position` 属性用于每个状态，以指定“sprite”图像的哪个部分。 您可以采用任何合适的方式构建“Sprite”图像。 查看器通常会垂直堆叠查看器。 下面是一个基于“sprite”的示例，用于为上面相同的滚动按钮设置样式：

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

* 使用CSS自定义查看器用户界面时，使用 `!IMPORTANT` 样式查看器元素不支持规则。 特别是， `!IMPORTANT` 规则不应用于覆盖查看器或查看器SDK提供的任何默认样式或运行时样式。 其原因可能会影响正确组件的行为。 您而是应该使用具有适当特性的CSS选择器来设置本参考指南中介绍的CSS属性。
* CSS中指向外部资产的所有路径都将根据CSS位置进行解析，而不是根据查看器HTML页面位置进行解析。 将默认CSS复制到其他位置时，请注意此规则。 复制默认资产或更新自定义CSS中的路径。
* 位图图稿的首选格式为PNG。
* 位图图稿使用 `background-image` 属性。
* 的 `width` 和 `height` 用户界面元素的属性定义其逻辑大小。 传递到的位图的大小 `background-image` 不影响逻辑大小。
* 要使用Retina等高分辨率屏幕的高像素密度，请指定比图稿大两倍于逻辑用户界面元素大小的位图图稿。 然后，应用 `-webkit-background-size:contain` 属性，将背景向下缩放为逻辑用户界面元素大小。
* 要从用户界面中删除按钮，请添加 `display:none` 到其CSS类。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度，请使用格式 `rgba(R,G,B,A)`. 否则，您可以使用格式 `#RRGGBB`.

## 常用用户界面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是适用于弹出查看器的用户界面元素引用文档：
