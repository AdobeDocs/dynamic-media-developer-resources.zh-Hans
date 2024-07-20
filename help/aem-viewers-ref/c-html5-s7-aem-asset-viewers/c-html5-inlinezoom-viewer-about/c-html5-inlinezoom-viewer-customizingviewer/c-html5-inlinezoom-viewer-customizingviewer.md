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
source-wordcount: '1287'
ht-degree: 0%

---

# 自定义内联缩放查看器{#customizing-inline-zoom-viewer}

所有可视自定义和大多数行为自定义均通过创建自定义CSS来完成。

建议的工作流是获取相应查看器的默认CSS文件，将其复制到其他位置，对其进行自定义，然后在`style=`命令中指定自定义文件的位置。

可以在以下位置找到默认CSS文件：

`<s7_viewers_root>/html5/InlineZoomViewer.css`

自定义CSS文件必须包含与默认文件相同的类声明。 如果忽略类声明，则查看器将无法正常运行，因为它没有为用户界面元素提供内置的默认样式。

此外，由于内联缩放功能需要，因此保留默认查看器CSS中的以下CSS声明也很重要：

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

提供自定义CSS规则的替代方法是直接在网页或其中一个链接的外部CSS规则中使用嵌入样式。

创建自定义CSS时，请记住，查看器将`.s7flyoutviewer`类分配给其容器DOM元素。 如果您使用通过`style=`命令传递的外部CSS文件，请将`.s7flyoutviewer`类用作CSS规则的后代选择器中的父类。 如果您在网页上执行嵌入样式，则还可以使用容器DOM元素的ID限定此选择器，如下所示：

`#<containerId>.s7flyoutviewer`

## 构建响应式设计的CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

可以在CSS中定位不同的设备和嵌入大小，以使内容的显示有所不同，具体取决于用户的设备或特定网页布局。 此功能包括但不限于，不同的网页布局、用户界面元素大小和图稿分辨率。

查看器支持两种创建响应式设计CSS的方法： CSS标记和标准CSS媒体查询。 您可以单独或同时使用这些方法。

**CSS标记**

为了帮助创建响应式设计CSS，查看器支持CSS标记，这些标记是动态分配给顶级查看器容器元素的特殊CSS类。 分配基于运行时查看器大小和当前设备上使用的输入类型。

第一组CSS标记包括`.s7size_large`、`.s7size_medium`和`.s7size_small`类。 它们根据查看器容器的运行时区域应用。 即，如果查看器区域等于或大于使用普通桌面监视器`.s7size_large`的大小；如果该区域的大小接近普通平板电脑设备`.s7size_medium`，则分配该区域。 对于类似于手机屏幕的区域，设置`.s7size_small`。 这些CSS标记的主要用途是为不同的屏幕和查看器大小创建不同的用户界面布局。

第二组CSS标记包括`.s7mouseinput`和`.s7touchinput`。 如果当前设备具有触摸输入功能，则设置标记`.s7touchinput`；否则，使用`.s7mouseinput`。 这些标记旨在为不同的输入类型创建具有不同屏幕大小的用户界面输入元素，因为通常触摸输入需要更大的元素。 如果设备同时具有鼠标输入和触摸功能，则设置`.s7touchinput`，并且查看器呈现触摸友好的用户界面。

以下示例CSS将放大按钮大小设置为在输入鼠标的系统上为28 x 28像素，在触摸设备上为56 x 56像素。 此外，如果查看器变小，它将完全隐藏按钮：

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

要定位具有不同像素密度的设备，请使用CSS媒体查询。 以下媒体查询块将包含特定于高密度屏幕的CSS：

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS标记是构建响应式设计CSS的最灵活方式。 它不仅允许目标设备屏幕大小，还允许目标实际查看器大小，这对于设计响应式网页布局可能很有用。

**CSS媒体查询**

设备感知也可以使用纯CSS媒体查询来完成。 给定媒体查询块中包含的所有内容，仅在相应设备上运行时适用。

应用于移动设备查看器时，使用四个CSS媒体查询，它们在CSS中按以下顺序定义：

1. 仅包含特定于所有触控设备的规则。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. 仅包含特定于具有高分辨率屏幕的平板电脑的规则。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. 仅包含特定于所有手机的规则。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 仅包含特定于高分辨率屏幕手机的规则。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

使用媒体查询方法，您应该使用设备感知来组织CSS，如下所示：

* 首先，特定于桌面的部分定义了特定于桌面或所有屏幕通用的所有属性。
* 其次，四个媒体查询按照以上定义的顺序进行，并提供特定于相应设备类型的CSS规则。

无需在每个媒体查询中复制整个查看器CSS。 只有特定于给定设备的属性才能在媒体查询中重新定义。

## CSS脚本 {#section-b0af39db1af74561aea9fddcc8cdc2c7}

许多查看器用户界面元素使用位图图进行样式设置，并具有多个不同的可视状态。 一个很好的示例是一个按钮，该按钮通常至少具有三种不同的状态：“up”、“over”和“down”。 每个状态都需要为其指定自己的位图图稿。

使用经典样式设置方法时，对于用户界面元素的每个状态，CSS将对服务器上的单个图像文件进行单独的引用。 以下是设置滚动按钮样式的CSS示例：

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

此方法的一个缺点是最终用户在首次与元素交互时体验到用户界面响应闪烁或延迟。 发生此操作是因为尚未下载新元素状态的图像图稿。 此外，由于对服务器的HTTP调用数量增加，此方法可能会对性能产生轻微的负面影响。

CSS sprite是一种不同的方法，所有元素状态的图像图稿都合并到称为“sprite”的单个PNG文件中。 此类“sprite”具有给定元素的所有视觉状态，它们彼此相邻。 使用拼写设置用户界面元素的样式时，同一个sprite图像将针对CSS中的所有不同状态引用。 此外，`background-position`属性用于每个状态，以指定使用“sprite”图像的哪个部分。 您可以以任何适当的方式构建“Sprite”图像。 查看器通常将其垂直栈叠。 下面是基于“sprite”的示例，用于从上面为同一滚动按钮设置样式：

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

## 常规样式注释和建议 {#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自定义查看器用户界面时，样式查看器元素不支持使用`!IMPORTANT`规则。 特别是，`!IMPORTANT`规则不应用于覆盖查看器或查看器SDK提供的任何默认样式或运行时样式。 原因是它可能会影响正确组件的行为。 您应该使用具有适当特定性的CSS选择器来设置本参考指南中记录的CSS属性。
* 指向CSS内外部资产的所有路径都是针对CSS位置解析的，而不是针对查看器HTML页面位置解析的。 将默认CSS复制到其他位置时，请注意此规则。 复制默认资产或更新自定义CSS中的路径。
* 位图图稿的首选格式为PNG。
* 使用`background-image`属性将位图图稿分配给用户界面元素。
* 用户界面元素的`width`和`height`属性定义其逻辑大小。 传递到`background-image`的位图的大小不会影响逻辑大小。
* 若要使用高分辨率屏幕（如Retina）的高像素密度，请指定两倍于逻辑用户界面元素大小的位图图案。 然后，应用`-webkit-background-size:contain`属性将后台缩小到逻辑用户界面元素大小。
* 要从用户界面中删除按钮，请将`display:none`添加到其CSS类。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度，请使用格式`rgba(R,G,B,A)`。 否则，您可以使用格式`#RRGGBB`。

## 常见用户界面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是适用于弹出查看器的用户界面元素参考文档：
