---
description: 通过创建自定义CSS，可以为eCatalog搜索查看器进行所有可视化自定义和大多数行为自定义。
keywords: 响应
seo-description: 通过创建自定义CSS，可以为eCatalog搜索查看器进行所有可视化自定义和大多数行为自定义。
seo-title: 自定义eCatalog搜索查看器
solution: Experience Manager
title: 自定义eCatalog搜索查看器
uuid: a715399b-7b02-4656-8257-4c390c6f629c
feature: Dynamic Media Classic，查看器，SDK/API，电子目录搜索
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---


# 自定义eCatalog Search Viewer{#customizing-ecatalog-search-viewer}

通过创建自定义CSS，可以为eCatalog搜索查看器进行所有可视化自定义和大多数行为自定义。

建议的工作流程是为相应的查看器使用默认的CSS文件，将其复制到其他位置，对其进行自定义，并在`style=`命令中指定自定义文件的位置。

默认CSS文件位于以下位置：

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

自定义CSS文件必须包含与默认类声明相同的类声明。 如果省略类声明，则查看器无法正常工作，因为它不为用户界面元素提供内置默认样式。

提供自定义CSS规则的另一种方法是直接在网页或链接的外部CSS规则之一中使用嵌入样式。

创建自定义CSS时，请记住，查看器将`.s7ecatalogsearchviewer`类分配给其容器 DOM元素。 如果使用通过`style=`命令传递的外部CSS文件，请在CSS规则的子代选择器中使用`.s7ecatalogsearchviewer`类作为父类。 如果要在网页上执行嵌入样式，则还可以通过以下容器DOM元素的ID来限定此选择器：

`#<containerId>.s7ecatalogsearchviewer`

## 构建响应式设计的CSS {#section-c1e74f5114ad418884ca1c95f5ea5b63}

可以目标CSS中的不同设备和嵌入大小，使内容显示方式不同，具体取决于用户的设备或特定网页布局。 这包括但不限于不同的网页布局、用户界面元素大小和图稿分辨率。

查看器支持两种创建响应式设计的CSS的方法：CSS标记和标准CSS媒体查询。 您可以单独或一起使用这些方法。

**CSS标记**

为了帮助创建响应式设计的CSS，查看器支持CSS标记，这些特殊CSS类基于运行时查看器大小和当前设备上使用的输入类型动态分配给顶级查看器容器元素。

第一组CSS标记包括`.s7size_large`、`.s7size_medium`和`.s7size_small`类。 它们会根据查看器容器的运行时区域进行应用。 即，如果查看器区域等于或大于通用桌面监视器`.s7size_large`的大小；如果区域大小与通用平板电脑设备`.s7size_medium`相近，则分配该区域。 对于类似于手机屏幕的区域设置`.s7size_small`。 这些CSS标记的主要用途是为不同的屏幕和查看器大小创建不同的用户界面布局。

第二组CSS标记包括`.s7mouseinput`和`.s7touchinput`。 `.s7touchinput` is set if current device has touch input capabilities;否则， `.s7mouseinput` 将使用。这些标记旨在为不同的输入类型创建具有不同屏幕大小的用户界面输入元素，因为通常触摸输入需要较大的元素。 如果设备同时具有鼠标输入和触摸功能，则设置`.s7touchinput`，并且查看器呈现适合触摸的用户界面。

以下范例CSS将鼠标输入系统上的按钮放大大小设置为28 x 28像素，将触控设备上的缩放大小设置为56 x 56像素。 此外，如果查看器尺寸变得很小，它会完全隐藏按钮：

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

要目标像素密度不同的设备，请使用CSS媒体查询。 以下媒体查询块将包含特定于高密度屏幕的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS标记是构建响应式设计的CSS的最灵活方式，因为它不仅允许您目标设备屏幕大小，还允许显示实际的查看器大小，这对于响应式设计的页面布局非常有用。

将默认查看器CSS文件用作CSS标记方法的示例。

**CSS媒体查询**

设备传感也可以使用纯CSS媒体查询完成。 仅当在相应设备上运行给定媒体查询块时，才应用它中包含的所有内容。

应用于移动查看器时，按以下顺序使用在CSS中定义的四个CSS媒体查询:

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

1. 仅包含所有移动电话的特定规则。

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

使用媒体查询方法，您应按照如下方式通过设备传感组织CSS:

* 首先，特定于桌面的部分定义所有属性，这些属性是特定于桌面的，或是所有屏幕通用的。
* 其次，这四个媒体查询按上面定义的顺序排列，并提供特定于相应设备类型的CSS规则。

无需在每个媒体查询中重复整个查看器CSS。 只有特定于给定设备的属性在媒体查询中重新定义。

## CSS Sprite {#section-9d570f95eb2443aca74c1b02f6e89aff}

许多查看器用户界面元素使用位图图稿设置样式，并具有多个不同的可视状态。 一个不错的示例是按钮，它通常至少具有三种不同的状态：“up”、“over”和“down”。 每个状态都需要分配自己的位图图稿。

使用经典的样式方法，CSS将针对用户界面元素的每个状态对服务器上的单个图像文件单独引用。 以下是用于设置放大按钮样式的示例CSS:

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

此方法的缺点是，当元素第一次与之交互时，终端用户体验到闪烁或延迟的用户界面响应。 此操作之所以发生，是因为尚未下载新元素状态的图像图稿。 此外，由于对服务器的HTTP调用数量增加，此方法可能会对性能产生轻微的负面影响。

CSS Sprite是一种不同的方法，将所有元素状态的图像图稿组合到一个称为“Sprite”的PNG文件中。 此类“Sprite”具有给定元素的所有可视状态，这些元素会依次放置。 当用Sprite设置用户界面元素的样式时，CSS中的所有不同状态都引用了相同的Sprite图像。 此外，每个状态都使用`background-position`属性来指定使用“sprite”图像的哪一部分。 您可以以任何合适的方式构建“Sprite”图像。 查看器通常垂直堆叠。 下面是一个基于“Sprite”的示例，用于从上面设置相同的放大按钮的样式：

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

## 一般样式说明和建议{#section-95855dccbbc444e79970f1aaa3260b7b}

* 使用CSS自定义查看器用户界面时，不支持对查看器元素设置样式。 `!IMPORTANT`尤其不应使用`!IMPORTANT`规则覆盖查看器或查看器SDK提供的任何默认或运行时样式。 其原因在于，它可能会影响正确组件的行为。 相反，您应使用具有适当特异性的CSS选择器来设置本参考指南中介绍的CSS属性。
* CSS中指向外部资源的所有路径都将根据CSS位置（而非查看器HTML页面位置）进行解析。 将默认CSS复制到其他位置时，请注意此规则。 复制默认资源或更新自定义CSS中的路径。
* 位图图稿的首选格式为PNG。
* 位图图稿使用`background-image`属性分配给用户界面元素。
* 用户界面元素的`width`和`height`属性定义其逻辑大小。 传递给`background-image`的位图的大小不影响逻辑大小。
* 要使用Retina等高分辨率屏幕的高像素密度，请指定比逻辑用户界面元素大两倍的位图图稿。 然后，应用`-webkit-background-size:contain`属性，将背景缩小到逻辑用户界面元素大小。
* 要从用户界面中删除按钮，请将`display:none`添加到其CSS类。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度，请使用格式`rgba(R,G,B,A)`。 否则，可以使用格式`#RRGGBB`。

## 常用用户界面元素{#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是适用于eCatalog Search Viewer的用户界面元素引用文档：

* [“添加收藏夹”按钮](r-html5-ecatsearch-customize-addfavorite.md)
* [“关闭”按钮](r-html5-ecatsearch-customize-closebutton.md)
* [下载](r-html5-ecatsearch-customize-download.md)
* [电子邮件共享](r-html5-ecatsearch-customize-emailshare.md)
* [嵌入共享](r-html5-ecatsearch-customize-embedshare.md)
* [Facebook分享](r-html5-ecatsearch-customize-facebookshare.md)
* [收藏夹效果](r-html5-ecatsearch-customize-favoriteseffect.md)
* [收藏夹菜单](r-html5-ecatsearch-customize-favoritesmenu.md)
* [收藏夹视图](r-html5-ecatsearch-customize-favoritesview.md)
* [首页按钮](r-html5-ecatsearch-customize-firstpagebutton.md)
* [焦点突出显示](r-html5-ecatsearch-customize-focushighlight.md)
* [全屏按钮](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [图标效果](r-html5-ecatsearch-customize-iconeffect.md)
* [“信息”面板弹出窗口](r-html5-ecatsearch-customize-infopanelpopup.md)
* [图像映射效果](r-html5-ecatsearch-customize-imagemapeffect.md)
* [“大”下一页按钮](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [“大上一页”按钮](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [“最后一页”按钮](r-html5-ecatsearch-customize-lastpagebutton.md)
* [链接共享](r-html5-ecatsearch-customize-linkshare.md)
* [主控制栏](r-html5-ecatsearch-customize-maincontrolbar.md)
* [主查看器区域](r-html5-ecatsearch-customize-mainviewerarea.md)
* [“下一页”按钮](r-html5-ecatsearch-customize-nextpagebutton.md)
* [页面指示器](r-html5-ecatsearch-customize-pageindicator.md)
* [页面查看](r-html5-ecatsearch-customize-pageview.md)
* [“上一页”按钮](r-html5-ecatsearch-customize-previouspagebutton.md)
* [打印](r-html5-ecatalog-viewer-20-customize-print.md)
* [“删除收藏夹”按钮](r-html5-ecatsearch-customize-removefavorite.md)
* [搜索按钮](r-html5-ecatsearch-customize-searchbutton.md)
* [搜索效果](r-html5-ecatsearch-customize-searcheffect.md)
* [搜索结果面板](r-html5-ecatsearch-customize-searchresultspanel.md)
* [辅助控制栏](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [社交共享](r-html5-ecatsearch-customize-socialshare.md)
* [目录](r-html5-ecatsearch-customize-tableofcontents.md)
* [缩略图](r-html5-ecatsearch-customize-thumbnails.md)
* [“缩览图”按钮](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [工具提示](r-html5-ecatsearch-customize-tooltips.md)
* [Twitter分享](r-html5-ecatsearch-customize-twittershare.md)
* [视图“所有收藏夹”按钮](r-html5-ecatsearch-customize-viewallfavorites.md)
* [放大按钮](r-html5-ecatsearch-customize-zoominbutton.md)
* [缩小按钮](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [缩放重置按钮](r-html5-ecatsearch-customize-zoomresetbutton.md)

