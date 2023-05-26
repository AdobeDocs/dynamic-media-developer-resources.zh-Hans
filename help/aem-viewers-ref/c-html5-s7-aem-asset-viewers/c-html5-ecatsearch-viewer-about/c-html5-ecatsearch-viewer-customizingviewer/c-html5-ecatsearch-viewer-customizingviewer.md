---
title: 自定义eCatalog搜索查看器
description: eCatalog搜索查看器的所有可视化自定义项和大多数行为自定义项均通过创建自定义CSS来完成。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 0%

---

# 自定义eCatalog搜索查看器{#customizing-ecatalog-search-viewer}

eCatalog搜索查看器的所有可视化自定义项和大多数行为自定义项均通过创建自定义CSS来完成。

建议的工作流程是获取相应查看器的默认CSS文件，将其复制到其他位置，对其进行自定义，然后在 `style=` 命令。

可以在以下位置找到默认CSS文件：

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

自定义CSS文件必须包含与默认文件相同的类声明。 如果省略类声明，则查看器将无法正常运行，因为它没有为用户界面元素提供内置的默认样式。

提供自定义CSS规则的另一种方法是直接在网页上或某个链接的外部CSS规则中使用嵌入样式。

创建自定义CSS时，请记住，查看器分配 `.s7ecatalogsearchviewer` 类到其容器DOM元素。 如果您使用的是随传递的外部CSS文件 `style=` 命令，使用 `.s7ecatalogsearchviewer` 类作为CSS规则的后代选择器中的父类。 如果您在网页上执行嵌入样式，则还应该使用容器DOM元素的ID限定此选择器，如下所示：

`#<containerId>.s7ecatalogsearchviewer`

## 构建响应式设计的CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

可以根据用户的设备或特定网页布局，在CSS中定位不同的设备和嵌入大小，以使内容以不同的方式显示。 此定位包括但不限于不同的网页布局、用户界面元素大小和图稿分辨率。

查看器支持两种创建响应式设计CSS的方法： CSS标记和标准CSS媒体查询。 您可以单独或同时使用这些方法。

**CSS标记**

要创建响应式设计CSS，查看器支持CSS标记，这些标记的特殊CSS类根据运行时查看器大小和当前设备上的输入类型动态分配给顶级查看器容器元素。

第一组CSS标记包括 `.s7size_large`， `.s7size_medium`、和 `.s7size_small` 类。 它们根据查看器容器的运行时区域应用。 即，如果查看器区域等于或大于普通台式机显示器的大小 `.s7size_large` 使用；如果该区域的大小与普通平板电脑设备接近 `.s7size_medium` 已分配。 适用于与移动电话屏幕类似的区域。 标记 `.s7size_small` 设置。 这些CSS标记的主要用途是为不同的屏幕和查看器大小创建不同的用户界面布局。

第二组CSS标记包括 `.s7mouseinput` 和 `.s7touchinput`. 标记 `.s7touchinput` 如果当前设备具有触摸输入功能，则设置为；否则， `.s7mouseinput` 已使用。 这些标记旨在为不同的输入类型创建具有不同屏幕大小的用户界面输入元素，因为通常触摸输入需要更大的元素。 如果设备同时具有鼠标输入和触摸功能， `.s7touchinput` 已设置，并且查看器呈现一个触屏友好的用户界面。

以下示例CSS将放大按钮大小设置为28 x 28像素（在具有鼠标输入的系统上）和56 x 56像素（在触控设备上）。 此外，如果查看器大小变得太小，则会完全隐藏按钮：

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

要定位具有不同像素密度的设备，请使用CSS媒体查询。 以下媒体查询块将包含特定于高密度屏幕的CSS：

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS标记是构建响应式设计CSS的最灵活方法。 通过它，您不仅可以定位设备屏幕大小，还可以定位实际查看器大小，这对于响应式设计页面布局非常有用。

使用默认查看器CSS文件作为CSS标记方法示例。

**CSS媒体查询**

也可以使用纯CSS媒体查询完成设备感知。 给定媒体查询块中包含的所有内容仅在其在对应的设备上运行时适用。

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

## CSS脚本 {#section-9d570f95eb2443aca74c1b02f6e89aff}

许多查看器用户界面元素使用位图图进行样式设置，并具有多个不同的可视状态。 一个很好的示例是一个按钮，该按钮通常至少具有三种不同的状态：“up”、“over”和“down”。 每个状态都需要为其指定自己的位图图稿。

使用经典样式设置方法时，对于用户界面元素的每个状态，CSS将对服务器上的单个图像文件进行单独引用。 以下是缩放按钮样式的CSS示例：

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

这种方法的一个缺点是当元素首次交互时，最终用户会遇到用户界面响应闪烁或延迟的情况。 发生此操作是因为尚未下载新元素状态的图像图稿。 此外，由于对服务器的HTTP调用数量增加，此方法可能会对性能产生轻微的负面影响。

CSS sprite是一种不同的方法，其中所有元素状态的图像图稿都合并到名为“sprite”的单个PNG文件中。 此类“sprite”具有依次定位的给定元素的所有可视状态。 在样式化带有拼写的用户界面元素时，同一个sprite图像会引用到CSS中的所有不同状态。 此外， `background-position` 属性用于每个状态，以指定使用“sprite”图像的哪个部分。 您可以以任何适当的方式构建“sprite”图像。 查看器通常将其垂直栈叠。 下面是基于“sprite”的示例，用于从上面为同一放大按钮设置样式：

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## 一般样式注释和建议 {#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自定义查看器用户界面时，使用 `!IMPORTANT` 样式查看器元素不支持规则。 特别是， `!IMPORTANT` 规则不应用于覆盖查看器或查看器SDK提供的任何默认样式或运行时样式。 原因是它可能会影响适当组件的行为。 您应该改用具有适当特定性的CSS选择器来设置本参考指南中记录的CSS属性。
* 指向CSS内外部资源的所有路径都是针对CSS位置解析的，而不是针对查看器HTML页面位置解析的。 将默认CSS复制到其他位置时，请注意此规则。 复制默认资产或更新自定义CSS中的路径。
* 位图图稿的首选格式为PNG。
* 位图图稿使用指定给用户界面元素 `background-image` 属性。
* 此 `width` 和 `height` 用户界面元素的属性定义其逻辑大小。 传递到的位图的大小 `background-image` 不会影响逻辑大小。
* 要使用高分辨率屏幕（如Retina）的高像素密度，请指定两倍于逻辑用户界面元素大小的位图图图案。 然后，应用 `-webkit-background-size:contain` 属性，用于将后台缩小到逻辑用户界面元素大小。
* 要从用户界面删除按钮，请添加 `display:none` 到其CSS类。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度，请使用格式 `rgba(R,G,B,A)`. 否则，可以使用格式 `#RRGGBB`.

## 常见用户界面元素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是适用于eCatalog搜索查看器的用户界面元素参考文档：

* [“添加收藏夹”按钮](r-html5-ecatsearch-customize-addfavorite.md)
* [“关闭”按钮](r-html5-ecatsearch-customize-closebutton.md)
* [下载](r-html5-ecatsearch-customize-download.md)
* [电子邮件共享](r-html5-ecatsearch-customize-emailshare.md)
* [嵌入共享](r-html5-ecatsearch-customize-embedshare.md)
* [facebook共享](r-html5-ecatsearch-customize-facebookshare.md)
* [收藏夹效果](r-html5-ecatsearch-customize-favoriteseffect.md)
* [收藏夹菜单](r-html5-ecatsearch-customize-favoritesmenu.md)
* [收藏夹视图](r-html5-ecatsearch-customize-favoritesview.md)
* [“第一页”按钮](r-html5-ecatsearch-customize-firstpagebutton.md)
* [焦点高亮](r-html5-ecatsearch-customize-focushighlight.md)
* [全屏按钮](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [图标效果](r-html5-ecatsearch-customize-iconeffect.md)
* [信息面板弹出窗口](r-html5-ecatsearch-customize-infopanelpopup.md)
* [图像映射效果](r-html5-ecatsearch-customize-imagemapeffect.md)
* [“大下一页”按钮](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [“上一页”按钮很大](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [“最后一页”按钮](r-html5-ecatsearch-customize-lastpagebutton.md)
* [链接共享](r-html5-ecatsearch-customize-linkshare.md)
* [主控制栏](r-html5-ecatsearch-customize-maincontrolbar.md)
* [主查看器区域](r-html5-ecatsearch-customize-mainviewerarea.md)
* [“下一页”按钮](r-html5-ecatsearch-customize-nextpagebutton.md)
* [页面指示器](r-html5-ecatsearch-customize-pageindicator.md)
* [页面查看](r-html5-ecatsearch-customize-pageview.md)
* [“上一页”按钮](r-html5-ecatsearch-customize-previouspagebutton.md)
* [打印](r-html5-ecatsearch-customize-print.md)
* [“删除收藏夹”按钮](r-html5-ecatsearch-customize-removefavorite.md)
* [“搜索”按钮](r-html5-ecatsearch-customize-searchbutton.md)
* [搜索效果](r-html5-ecatsearch-customize-searcheffect.md)
* [搜索结果面板](r-html5-ecatsearch-customize-searchresultspanel.md)
* [辅助控制栏](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [社交共享](r-html5-ecatsearch-customize-socialshare.md)
* [目录](r-html5-ecatsearch-customize-tableofcontents.md)
* [缩略图](r-html5-ecatsearch-customize-thumbnails.md)
* [“缩略图”按钮](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [工具提示](r-html5-ecatsearch-customize-tooltips.md)
* [twitter共享](r-html5-ecatsearch-customize-twittershare.md)
* [“查看所有收藏夹”按钮](r-html5-ecatsearch-customize-viewallfavorites.md)
* [放大按钮](r-html5-ecatsearch-customize-zoominbutton.md)
* [缩小按钮](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [缩放重置按钮](r-html5-ecatsearch-customize-zoomresetbutton.md)
