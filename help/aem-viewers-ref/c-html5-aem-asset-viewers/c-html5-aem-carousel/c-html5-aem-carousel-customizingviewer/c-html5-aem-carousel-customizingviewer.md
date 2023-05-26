---
title: 自定义轮播查看器
description: 轮播查看器的所有可视化自定义和大多数行为自定义均通过创建自定义CSS来完成。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f392d830-5c75-45dd-bab8-29a38218790d
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 0%

---

# 自定义轮播查看器{#customizing-carousel-viewer}

轮播查看器的所有可视化自定义和大多数行为自定义均通过创建自定义CSS来完成。

建议的工作流程是获取相应查看器的默认CSS文件，将其复制到其他位置，对其进行自定义，然后在 `style=` 命令。

可以在以下位置找到默认CSS文件：

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

为查看器提供了四个现成的CSS文件，用于数字和点状设置指示符，每个都采用“浅色”和“深色”颜色方案。 默认情况下使用“点状光源”版本，但通过使用不同的标准CSS并设置 `SetIndicator.mode` 参数。 其他标准CSS可在以下位置找到：

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

自定义CSS文件必须包含与默认文件相同的类声明。 如果省略类声明，则查看器将无法正常运行，因为它没有为用户界面元素提供内置的默认样式。

提供自定义CSS规则的另一种方法是直接在网页或其中一个链接的外部CSS规则中使用嵌入样式。

创建自定义CSS时，请记住，查看器分配 `.s7carouselviewer` 类到其容器DOM元素。 如果您使用的是随一起传递的外部CSS文件 `style=` 命令，使用 `.s7carouselviewer` 类作为CSS规则的后代选择器中的父类。 如果您在网页上添加嵌入样式，还可以使用容器DOM元素的ID限定此选择器，如下所示：

`#<containerId>.s7carouselviewer`

## 构建响应式设计的CSS {#section-0bb49aca42d242d9b01879d5ba59d33b}

可以根据用户的设备或特定网页布局，在CSS中定位不同的设备和嵌入大小，以使内容以不同的方式显示。 此技术包括但不限于不同的布局、用户界面元素大小和图稿分辨率。

查看器支持两种创建响应式设计CSS的机制： CSS标记和标准CSS媒体查询。 可以单独或一起使用这两种机制。

**CSS标记**

为了帮助创建响应式设计的CSS，查看器支持CSS标记。 这些标记是动态分配给顶级查看器容器元素的特殊CSS类。 它们基于运行时查看器大小和当前设备上使用的输入类型。

第一组CSS标记包含 `.s7size_large`， `.s7size_medium`、和 `.s7size_small` 类。 它们根据查看器容器的运行时区域应用。 例如，如果查看器区域等于或大于常用桌面监视器的大小，请使用 `.s7size_large`. 如果该区域靠近普通平板电脑设备，则指定 `.s7size_medium`. 对于与移动电话屏幕类似的区域，请使用 `.s7size_small`. 这些CSS标记的主要用途是为不同的屏幕和查看器大小创建不同的用户界面布局。

第二组CSS标记包含 `.s7mouseinput` 和 `.s7touchinput`. CSS标记 `.s7touchinput` 如果当前设备是触摸输入，则设置为。 否则， `.s7mouseinput` 已使用。 这些标记主要用于为不同的输入类型创建具有不同屏幕大小的用户界面输入元素，因为通常触摸输入需要更大的元素。

以下示例CSS将鼠标输入系统的放大按钮大小设置为28 x 28像素，将触摸输入设备的放大按钮大小设置为56 x 56像素。 如果查看器的大小更小，则设置为20 x 20像素。

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

要定位具有不同像素密度的设备，必须使用CSS媒体查询。 以下媒体查询块将包含特定于高密度屏幕的CSS：

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS标记是构建响应式设计CSS的最灵活方式，因为它允许您不仅定向设备屏幕大小，而且定向实际查看器大小，这对于响应式设计布局非常有用。

您可以使用默认查看器CSS文件作为CSS标记方法示例。

**CSS媒体查询**

您还可以使用纯CSS媒体查询完成设备感知。 给定媒体查询块中包含的所有内容仅在其在对应的设备上运行时适用。

应用到移动设备查看器时，会按照以下列出的顺序，使用四个CSS媒体查询（在CSS中定义）：

1. 仅包含特定于所有触控设备的规则。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
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

1. 仅包含特定于具有高分辨率屏幕的手机的规则。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

使用媒体查询方法，您应该使用设备感知来组织CSS，如下所示：

* 首先，特定于桌面的部分定义了特定于桌面或所有屏幕通用的所有属性。
* 其次，这四个媒体查询按照上面定义的顺序进行，并提供特定于相应设备类型的CSS规则。

无需在每个媒体查询中复制整个查看器CSS。 只有特定于给定设备的属性才会在媒体查询中重新定义。

## CSS脚本 {#section-9b6d8d601cb441d08214dada7bb4eddc}

许多查看器用户界面元素使用位图图进行样式设置，并具有多个不同的可视状态。 一个很好的示例是通常至少具有三种不同状态的按钮： `up`， `over`、和 `down`. 每个状态都需要为其指定自己的位图图稿。

使用经典样式设置方法时，对于用户界面元素的每个状态，CSS将对服务器上的单个图像文件进行单独引用。 以下是缩放按钮样式的CSS示例：

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

这种方法的一个缺点是当元素首次交互时，最终用户会遇到用户界面响应闪烁或延迟的情况。 发生此操作是因为尚未下载新元素状态的图像图稿。 此外，由于对服务器的HTTP调用数量增加，此方法可能会对性能产生轻微的负面影响。

CSS sprite是一种不同的方法，其中所有元素状态的图像图稿都合并到名为“sprite”的单个PNG文件中。 此类“sprite”具有依次定位的给定元素的所有可视状态。 在样式化带有拼写的用户界面元素时，同一个sprite图像会引用到CSS中的所有不同状态。 此外， `background-position` 属性用于每个状态，以指定使用“sprite”图像的哪个部分。 您可以以任何适当的方式构建“sprite”图像。 查看器通常将其垂直栈叠。

以下是一个基于“sprite”的示例，用于设置同一热点图标的样式：

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## 一般样式注释和建议 {#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自定义查看器用户界面时，使用 `!IMPORTANT` 样式查看器元素不支持规则。 特别是， `!IMPORTANT` 规则不应用于覆盖查看器或查看器SDK提供的任何默认样式或运行时样式。 原因在于，它可能会影响适当组件的行为。 您应该改用具有适当特定性的CSS选择器来设置此查看器参考指南中记录的CSS属性。
* 指向CSS内外部资源的所有路径都是针对CSS位置解析的，而不是针对查看器HTML页面位置解析的。 将默认CSS复制到其他位置时，请注意此规则。 同时复制默认资产或更新自定义CSS中的所有路径。
* 位图图稿的首选格式为PNG。
* 位图图稿使用指定给用户界面元素 `background-image` 属性。
* 此 `width` 和 `height` 用户界面元素的属性定义其逻辑大小。 传递到的位图的大小 `background-image` 不影响其逻辑大小。
* 要使用高分辨率屏幕（如Retina）的高像素密度，请指定两倍于逻辑用户界面元素大小的位图图图案。 然后，应用 `-webkit-background-size:contain` 属性，用于将后台缩小到逻辑用户界面元素大小。
* 要从用户界面删除按钮，请添加 `display:none` 到其CSS类。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度，请使用格式 `rgba(R,G,B,A)`. 否则，可以使用格式 `#RRGGBB`.

## 常见用户界面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是适用于视频图像查看器的用户界面元素参考文档：
